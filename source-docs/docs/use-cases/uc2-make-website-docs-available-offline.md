---
title: UC2 Make Your Website Docs Available Offline
weight: 2
layout: docs
---

* Do you use some of the Jamstack Static Site Generators (SSG) - Jekyll, Hugo, Next.js, Gatsby etc?
* Do you you think is cool to make your wesite content available offline?

If answers are: __yes, yes__ respectively, you are at the right place.

In this section we will explain the workflow on how you can keep using your favorite SSG and still make your website content available offline. 
The workflow is outlined in the following UML diagram:

<!---
@startuml

skinparam sequence {
ArrowColor DodgerBlue
ActorBorderColor DodgerBlue
LifeLineBorderColor blue
LifeLineBackgroundColor DodgerBlue

ParticipantBorderColor DodgerBlue
ParticipantBackgroundColor DodgerBlue
ParticipantFontName Sans
ParticipantFontSize 17
ParticipantFontColor #A9DCDF

ActorBackgroundColor DodgerBlue
ActorFontColor DodgerBlue
ActorFontSize 17
ActorFontName Sans

}
title Make Your Website Docs Available Offline
autonumber
actor "Git User" as user
database "PuzzlesCloud" as saas
database "Git Project" as repo
group Git User workflow
   user -> saas : register
  user -> saas : import Git SSG project (Jekyll, Hugo, Next.js, Gatsby)
  saas -> repo : import Git SSG project (Jekyll, Hugo, Next.js, Gatsby)
   user -> saas : upload corporate DOCX template
   user -> saas : save and push
   saas -> saas : autogenerate the DOCX structure from SSG repo

  saas -> repo : push DOCX Template
  saas -> repo : push DOCX Table of Content
  saas -> repo : push updated DOCX and PDF
  alt if using git for updates
   alt if updating content
   user -> repo : commit new documentation version
   repo -> saas : your repo notifies us about the new version
   saas -> saas : autogenerate updated DOCX and PDF
   saas -> repo : push updated DOCX and PDF
   else if changing DOCX template
   user -> repo : commit your new DOCX template
   repo -> saas : your repo notifies us about the new template
   saas -> saas : autogenerate updated DOCX and PDF
   saas -> repo : push updated DOCX and PDF
   else if changing Content Structure (add/remove chapters, change order/heading level)
   user -> repo : commit your new SSG project structure
   repo -> saas : your repo notifies us about the new ToC
   saas -> saas : autogenerate updated DOCX and PDF
   saas -> repo : push updated DOCX and PDF
   end
  else if using PuzzlesCloud for updates (in development)
   alt if updating content
   user -> saas : update documents
   user -> saas : save and push
   saas -> repo : push updated DOCX and PDF
   else if changing DOCX template
   user -> saas : upload your new DOCX template
   user -> saas : save and push
   saas -> repo : push DOCX Template
   saas -> repo : push updated DOCX and PDF
   else if changing Content Structure (add/remove chapters-docs, change order/heading level)
   user -> saas : Update Content Structure
   user -> saas : save and push
   saas -> repo : push updated Content 
   end
  end
@enduml


preview: https://www.planttext.com/
-->

![Work in GIT and produce DOCX & PDF](/images/make-website-docs-available-offline.png "Work in GIT and produce DOCX & PDF")

1. Register (if not already done) and login to our application
2. Import a Git project where you have MarkDown based documentation.
3. Our application will connect to your repo and import it.
4. Upload your DOCX corporate template. For more details how to do it please check [Create DOCX Template](create-docx-template.html "Create DOCX Template").
5. Save your new doc in our application and push it to your Git repo.
6. Our App will autogenerate the DOCX structure from the SSG repo
7. Our App will push to your Git project uploaded DOCX template.
8. Our App will push to your Git project created DOCX structure (Table of Content).
9. Our App will push to your Git project new updated DOCX and PDF documents.
10. **[If Using Git for Updates][If Updating the Content]** You can update the content and commit the change to your repo.
11. Your repo through webhook service will notify our App about the change.
12. Our App will autogenerate updated DOCX and PDF.
13. Our App will push to your Git project new updated DOCX and PDF documents.
14. **[If Changing DOCX Template]** You can update the DOCX Template and commit the change to your repo.
15. Your repo through webhook service will notify our App about the new Template.
16. Our App will autogenerate updated DOCX and PDF.
17. Our App will push to your Git project new updated DOCX and PDF documents.
18. **[If Changing Table of Content]** You can update the Content structure and commit the change to your repo. There are different possibilities: add/remove chapters/ .md docs, change order/heading level 
19. Your repo through webhook service will notify our App about the new Table of Content.
20. Our App will autogenerate updated DOCX and PDF.
21. Our App will push to your Git project new updated DOCX and PDF documents.

  **If using PuzzlesCloud for Updates**

This option is still in development, coming soon. 