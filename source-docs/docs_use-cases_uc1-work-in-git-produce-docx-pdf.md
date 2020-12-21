---
title: UC1 Work in GIT and Produce DOCX & PDF
weight: 1
layout: docs
---

* Do you work in Git?
* Do you like current DOCX editors?
* Do you need to produce high quality DOCX?

If answers are: __yes, no, yes__ respectively, you are at the right place.

In this section we will explain the workflow on how you can work in Git and still produce high quality DOCX and PDF using our solution (very convenient for DevOps and Agile teams). This concept is known as docs-as-code, or we like to call it docx-as-code.
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
title Work in Git and Produce High Quality DOCX and PDF
autonumber
actor "Git User" as user
database "PuzzlesCloud" as saas
database "Git Project" as repo
group Git User workflow
   user -> saas : register
   user -> saas : import Git project (simple .md)
   saas -> repo : import Git project (simple .md)
   user -> saas : upload corporate DOCX template
   user -> saas : start a new document in our app
   user -> saas : create a Table of Content from Git .md docs
   user -> saas : save and push
  saas -> repo : push DOCX Template
  saas -> repo : push DOCX Table of Content
  saas -> repo : push updated DOCX and PDF
  alt if using git for updates
   alt if updating content
   user -> repo : commit new documentation version
   repo -> saas : your repo notifies us about the new version
   saas -> saas : generate updated DOCX and PDF
   saas -> repo : push updated DOCX and PDF
   else if changing DOCX template
   user -> repo : commit your new DOCX template
   repo -> saas : your repo notifies us about the new template
   saas -> saas : generate updated DOCX and PDF
   saas -> repo : push updated DOCX and PDF
   else if changing Table of Content (add/remove chapters, change order/heading level)
   user -> repo : commit your new Table of Content
   repo -> saas : your repo notifies us about the new ToC
   saas -> saas : generate updated DOCX and PDF
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
   else if changing Table of Content (add/remove chapters, change order/heading level)
   user -> saas : Update Table of Content
   user -> saas : save and push
   saas -> repo : push DOCX Table of Content
   saas -> repo : push updated DOCX and PDF
   end
end
@enduml


preview: https://www.planttext.com/
-->

![Work in GIT and produce DOCX & PDF](/images/work-in-git-produce-docx-pdf.png "Work in GIT and produce DOCX & PDF")

1. Register (if not already done) and login to our application
2. Import a Git project where you have MarkDown based documentation.
3. Our application will connect to your repo and import it.
4. Upload your DOCX corporate template. For more details how to do it please check [Create docx Template](create-docx-template "Create docx Template").
5. Start a new doc in our application.
6. Create manually the structure (Table of Content) of the new document, based on MarkDown docs in your Git repo.
7. Save your new doc in our application and push it to your Git repo.
8. Our App will push to your Git project uploaded DOCX template.
9. Our App will push to your Git project created DOCX structure (Table of Content).
10. Our App will push to your Git project new updated DOCX and PDF documents.
11. **[If Updating the Content]** You can update the content and commit the change to your repo.
12. Your repo through webhook service will notify our App about the change.
13. Our App will generate updated DOCX and PDF.
14. Our App will push to your Git project new updated DOCX and PDF documents.
15. **[If Changing DOCX Template]** You can update the DOCX Template and commit the change to your repo.
16. Your repo through webhook service will notify our App about the new Template.
17. Our App will generate updated DOCX and PDF.
18. Our App will push to your Git project new updated DOCX and PDF documents.
19. **[If Changing Table of Content]** You can update the Table of Content and commit the change to your repo. There are different possibilities: add/remove chapters/ .md docs, change order/heading level 
20. Your repo through webhook service will notify our App about the new Table of Content.
21. Our App will generate updated DOCX and PDF.
22. Our App will push to your Git project new updated DOCX and PDF documents.

  **If using PuzzlesCloud for Updates**

This option is still in development, coming soon. 
