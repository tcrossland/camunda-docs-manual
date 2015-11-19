---

title: 'Live Editing of Decision Tables'
weight: 55

menu:
  main:
    identifier: "user-guide-cockpit-live-editing"
    parent: "user-guide-cockpit"

---

* EE ONLY!!
* Screenshot of the modal dialog
* How to get there:
  * Decision Definition page, edit button
  * Deployment page: edit button on decision definition
* What what you can change:
  * Everything of the table - be careful!
  * Gray cells display technical information like variable names, changing them might lead to incompatability with existing definitions

* Download feature: You can download the changes you have made in this modal dialog without deploying them immediately. Not available in Internet Explorer
* Upload feature: You can upload a local dmn file to seed the table editor - you can then perform additional changes to the uploaded table before deploying it - not available in Internet Explorer 9

* Confirmation:
  * before changing the table, confirmation is needed
  * Changing a dmn table will create a new deployment containing the new dmn file as only resource. You can provide the name of the new deployment
  * New deployment will also have cockpit as deployment source
  * Change is live immediately - all process and case definitions which use the latest version of the decision definition now will use the new version
