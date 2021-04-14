---
title: How to import a Git project to PuzzlesCloud App?
weight: 2
layout: docs
---

In this section we will explain the workflow on how to import a Git project to our application.
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
title Import Git Project to PuzzlesCloud
autonumber
actor "Git User" as user
database "PuzzlesCloud" as saas
database "Git project" as repo
group Initial Git User workflow
  user -> saas : registration
  user -> saas : import Git project (simple .md, Jekyll, Hugo, Next.js, Gatsby)
  saas -> repo : import Git project (simple .md, Jekyll, Hugo, Next.js, Gatsby)
  user -> saas : upload DOCX template
  user -> saas : create a new DOCX doc
  alt If simple .md based project
  user -> saas : create a DOCX structure from .md docs
  else else if Jekyll, Hugo, Next.js, Gatsby...
  saas -> saas : autogenerate the DOCX structure from Git repo
  user -> saas : save
  saas -> repo : push DOCX Template
  saas -> repo : push DOCX ToC in txt form
  saas -> repo : push updated DOCX and PDF
end
@enduml

preview: https://www.planttext.com/
-->

![Import Git project workflow](../assets/images/import-git-project.png "Import Git project workflow")

1. Register (if not already done) and login to our application
2. Import a Git project
3. Our application will connect to your repo and import it 
4. Upload your DOCX corporate template or select existing one
5. Create manually the structure (ToC) of the new document (if imported simple MarkDown based Git project)
6. if Static Site Generator project is used (e.g Jekyll...) our application will autogenerate the Table of Content (ToC) structure
7. Save your new doc in our application and push to Git repo
8. Our application will push to your Git project uploaded DOCX template
9. Our application will push to your Git project created/autogenerated DOCX ToC structure
10. Our application will push to your Git project new updated DOCX and PDF documents
