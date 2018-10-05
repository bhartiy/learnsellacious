---
title: 'Template Alterration using Plugins'
visible: true
---

**Import templates can be altered using Plugins:**
* You can create one or more Plugins to alter the templates.
* Through these plugins you can add columns or make changes in the Default templates.
* If you want to add columns apart from the Default Columns in the imported template you can create plugins.

**Through Plugins you can take care of three actions or work upon them:**

**onFetchImportColumns** : In this, by creating plugins you can add columns in an imported template. And those                                  created columns will be added to Default imported template.

**onBeforeImport** : In this, by creating plugins you can make changes before starting import. And those                                  changes will be saved.

**onAfterImport** : In this, by creating plugins you can make changes after finishing the import. And those                             changes will be saved.
 
 Through Plugin you can work on either one of the action, two of them or on all of them.
