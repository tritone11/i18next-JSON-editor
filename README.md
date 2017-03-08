# ies18n - extended tool to edit your i18next JSON files
This tool let upload, edit, download your language files of i18next for translation.  
  
[WORKING DEMO](http://cerati.org/ies18n/)  

You can only read, every write option is not allowed in the demo to prevent troll edit
 
  
## Features  
- v0.01 supports only one level of nested objects.   
Example of supported JSON file:  

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
  Example of unsupported JSON file (to be supported in v0.02):  
  
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
- Create new languages files  
- Create new category  
- Create attributes and values in selected category  
- Delete categories  
- Delete attributes  
- Delete languages
- Live attributes and value edit  
- Quick translation suggest Google Translate  
- Yandex translation API for automatic translation  
- Match languages  
Match 2 languages to find missing categories, missing attributes and missing translations  

# Getting started  
  
## Make your Firebase project  
ies18 is based on a Google Firebase Database. Soon I will implement a nodejs server to make this tool totally standalone, for now you can easily create a totally free Firebase project at https://firebase.google.com/  
Get started and name your project. Once created and you're in the console, click on "Add your Firebase to your web app" and you will find the snippet to paste in the config.js file.  
  
## Set authorizations  
Enable authentication with Google on the authentication tab in the Firebase console, and the domains allowed to comunicate with your Firebase Database.  
In the database tab, set this rules:  

```
{
  "rules": {
    ".read": "true",
    ".write": "((auth.email == 'marty@gmail.com')||(auth.email == 'jennifer@gmail.com'))"
  }
}
```  
Put the Gmail or Google Apps email addreses allowed to write on your database. '.read' is set as true to allow a quick download of the JSON files, but you can set it as false if you need to keep your files not readable from thirds.  

## Ready to start  
You can now paste your Firebase snippet in the config.js file, where you can also set the default language, the default colors ...  
Note that in order to work, the quick Google Translate suggestion needs that you name your languages with the standard TAGS (en, fr, de ,us ecc..)  
Open your index.html on your website, your Firebase hosting or a software like hfs and you can start creating your language files or editing the ones you already have.  
Clicking on the logo make a full backup that you can import anytime in the Firebase Console  
  
[WORKING DEMO](http://cerati.org/ies18n/)  

You can only read, every write option is not allowed in the demo to prevent troll edit
  
# Important notes  
  
## Browser compatibility  
This tool makes extended use of the apex backtick ` which is supported only by browser supporting ECMAScript 6  
To enable automatic translation with Yandex, add your API key in the index.html file at line 1144




