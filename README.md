# OpenProcessing-i18n
This project includes OpenProcessing translation and internationalization files. Feel free to contribute to add your own language or make changes.

## Rules of Conduct
[To be defined]

## How It Works
Users can change their preferred language under user profile settings. The website loads and uses lang.json file to look up translations of phrases used on the website. Default language is English (en). 

## How to Contribute
All the phrases from the website are being added to lang.json. You can follow this repo to get any updates on the master branch.
To contribute,
- Create a branch first.
- Make your additions.
- Test it live by going to the related page on OpenProcessing and run the code below in native browser console to use your own branch. This will load lang.json from your own branch. 
```
	//format: OP.setLanguage([language],[branch title]);
	OP.setLanguage('ja','my-branch')
```
- If things look right, make a pull request. Your changes will be reviewed by language maintainers and will be merged if approved.

## lang.json Format
This file contains the phrases used on the website, grouped by sections, in the format below:
```
"sectionName": {
	"phraseLabel": {
		"implemented": false, //if website support not implemented yet.
		"description": "Tab", 
		"en": "Sketches",
		"ja": "モード"
	}
}
```
### Read-only Values
Values below should only be set by super-admins. These are created or changed as new phrases are added and implemented to the website.
- "SectionName" usually refers to the page it refers to. (CamelCase) 
- "PhraseLabel" is used for looking up the phrase. (CamelCase)
- "Implemented" exists and set to false if the website doesn't support this yet. This is used for phrases that are in the lang.json file as a placeholder, and its implementation on the website is pending. Once implementation is ready, "Implemented" is removed (instead of setting it to true) to keep the file size small. ** You will not be able to see your changes with OP.setLanguage function for these phrases **
- "Description" is there to help you find where and when the phrase is displayed.
- "en" is the official English translation of the phrase. All other translations must follow this English version.

### Translation Values
Translations are added with the format "languageShort": "Value":
```
"ja": "ユーザー",
"es": "usuario",
"fr": "utilisateur",
...
```




