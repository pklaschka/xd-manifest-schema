# xd-manifest-schema

Unofficial JSON schema for `manifest.json` files for plugins for Adobe XD CC.

You can use the schema (`schema.json`) for validation or coding assistance by your IDE (with autocompletion, linting etc.)

Please note that this is still a very early version and I'm continually refining the schema, meaning there might still be some mistakes. If you find any issues, please feel free to open an issue or a PR here on GitHub so it can get fixed ASAP :smile:

## Usage

You can either download the schema from this repo or use the (always up-to-date) version hosted at https://xdplugins.pabloklaschka.de/xsd/xd-manifest.json.

Below, you'll find some guides on how to use the schema in editors and IDEs. If you don't find your IDE in the list, but know how this can be achieved there, please open a Pull Request adding your editor/IDE of choice to the list so everyone can be as productive as possible developing plugins :wink:

#### Jetbrains WebStorm (tested in version 2018.3)
1. Go to Settings (`Ctrl+Alt+S` on Windows)
2. Go to `Languages and Frameworks`, `Schemas and DTDs`, `JSON Schema Mappings`
3. Add a new mapping with the `+` button on the left
4. Under `Schema file or URL`, either select the schema file if you have it saved locally or enter `https://xdplugins.pabloklaschka.de/xsd/xd-manifest.json`
5. Under `Schema version`, select `JSON schema version 7`
6. Below, click the `+` button (to add a mapping) and choose `Add file path pattern`
7. As a pattern, enter `manifest.json` and you should be good to go. Alternatively, you can also use `Add file` and select your manifest file manually...

#### VSCode (For Mac)
1. Go to Settings (`Cmd+,`)
2. Search for `json.schema`
3. Click on `Edit in settings.json`
4. Paste this config
```
"json.schemas": [
    {
      "fileMatch": [
        "/Adobe/*/develop/*/manifest.json"
      ],
      "url": "https://xdplugins.pabloklaschka.de/xsd/xd-manifest.json"
    }
  ]
```
**Note:** Pattern in `fileMatch` specifically target `manifest.json` file inside **Adobe** folder. (This can be changed to suit your needs)
