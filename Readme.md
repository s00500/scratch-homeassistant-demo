# Simple homeassistant demo for scratch


Download scratch-vm and scratch gui repositories from github.

Place the index.js file in scratch-vm/src/extensions/homeassistant (create this directory first)
Fill in _hassHost and _hassToken.

Then edit extension-support/extension-manager.js
Add line:
```
homeassistant: () => require('../extensions/homeassistant'),
```

to the "builtinExtensions" array


Then lets go to scratch-gui repo, and add homeassistant module to src/lib/libraries/extensions/index.jsx

```
+import homeassistantIconURL from './homeassistant/homeassistant.png';
+import homeassistantInsetIconURL from './homeassistant/homeassistant-small.svg';

[...]

+{
+        name: 'HomeAssistant',
+        extensionId: 'homeassistant',
+        // collaborator: 's00500',
+        iconURL: homeassistantIconURL,
+        insetIconURL: homeassistantInsetIconURL,
+        description: (
+            <FormattedMessage
+                defaultMessage="Home Asssitant Scratch integration"
+                description="Use this to control you home from scratch"
+                id="gui.extension.test.description"
+            />
+        ),
+        featured: true,
+        disabled: false
+    },
```


create a folder named src/lib/libraries/extensions/homeassistant/

And add the two png and svg images from this repo


