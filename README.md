# ies18n - extended tool to edit your i18next JSON files
This tool let upload, edit, download your language files of i18next for translation.

## Features
-v0.01 supports only one level of nested objects. 
  ###### Example of supported JSON file:
  ```
  {
    "common":{
      "hello" : "ciao",
      "welcome" : "benvenuto",
      "goodbye" : "arrivederci
    },
    "company":{
      "name" : "ies18",
      "street" : "Portobello Road, 14"
    }
  }
  ```
  ###### Example of unsupported JSON file (to be supported in v0.02):
  ```
  {
    "common":{ 
      "greetings:{
        "hello" : "ciao",
        "welcome" : "benvenuto",
        "goodbye" : "arrivederci
      }
    },
    "company":{
      "info":{
        "name" : "ies18",
        "street" : "Portobello Road, 14"
      }
    }
  }
  ```
-Create new languages files
-
