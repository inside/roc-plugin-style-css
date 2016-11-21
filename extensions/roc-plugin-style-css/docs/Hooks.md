# Hooks for `roc-plugin-style-css`

## Hooks
* [roc](#roc)
  * [update-settings](#update-settings)
* [roc-plugin-style-css](#roc-plugin-style-css)
  * [add-style](#add-style)

## roc

### update-settings

Expected to return new settings that should be merged with the existing ones.

Makes it possible to modify the settings object before a command is started and after potential arguments from the command line and configuration file have been parsed. This is a good point to default to some value if no was given or modify something in the settings.

__Initial value:__ _Nothing_  
__Expected return value:__ `Object()`

#### Arguments

| Name        | Description                                                                  | Type       | Required | Can be empty |
| ----------- | ---------------------------------------------------------------------------- | ---------- | -------- | ------------ |
| getSettings | A function that returns the settings after the context has been initialized. | `Function` | No       |              |

## roc-plugin-style-css

### add-style

Used for adding additional style loaders.

Important that the _actions_ return an object matching the following:

`{ extensions: String/[String], loaders: String/[String] }`

__Initial value:__ _Nothing_  
__Expected return value:__ `Object(String / Array(String))`
