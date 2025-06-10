---
fields:
  - name: progress
    type: Formula
    options:
      autoUpdate: true
      formula: Math.round((current.file.tasks.where(t => t.completed).length / current.file.tasks.length) * 100)
    path: ""
    id: mJ8sNg
version: "2.2"
limit: 20
mapWithTag: false
icon: package
tagNames: 
filesPaths: 
bookmarksGroups: 
excludes: 
extends: 
savedViews: []
favoriteView: 
fieldsOrder:
  - mJ8sNg
---
