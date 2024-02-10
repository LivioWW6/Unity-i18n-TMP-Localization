# Unity 2024 i18n-TMP-Localization
This is basically the original Daniel Erdmann version that updated Text objects to a specific language based on a key added to each text game object (textbox, button text, etc.). However, since the Textbox and Button etc. have become legacy items, it was necessary to add a script to deal with the new Text Mesh Pro (TMP) versions.
You can use this updated version with both the legacy and new TMP controls.

TMP Text Objects:
1 For new Text Mesh Pro Text objects add the ’l8nTMPTranslator.cs’ script to the text object from the list in the Inspector.
![tmp1](https://github.com/LivioWW6/i18n-TMP-Localization/assets/6105026/cc4ada51-534c-4eb6-8fdf-32e938a7118f)
2. Add a keyword in the’ TextId’ field. This will be the key for the Language Translation files in the Resource folder (see folder for examples).
The key must exist in each language file. Each key in the language file must be unique.
The translation happens while the scene is loading. You need to re-load the scene if you change the language in game play (see ‘LanguagePicker.cs’ script for an example with a drop-box of languages).
You can also add the script with the ‘Add Component’ button in the Inspector for each game object.
![legacy2](https://github.com/LivioWW6/i18n-TMP-Localization/assets/6105026/62a43c75-b168-4e0a-9432-9a959c76e612)
Legacy Text Objects:

1 For Legacy Text objects add the ‘I18nTextTranslator.cs’ script to the text object from the list in the Inspector.
![legacy1](https://github.com/LivioWW6/i18n-TMP-Localization/assets/6105026/cb0b36c7-675d-4973-9103-d25c656ec62e)

2 Or Click ‘Add Component’ in the Game object ‘Add Component’ button then enter the name in Inspector and select the ‘I18nTextTranslator.cs’ script.
Add a key as above.
Note that the key can be reused in multiple and different game objects. But it must be unique in each language file.

More information:

See ‘I18n.cs’ for Daniel Erdmann notes.

Sample Language Files
These are located in the Resources folder. A file must exist for each language used.
The ‘\n’ text is a linefeed

Sample English File
ButtonTxt=Translated Button
ButtonTMP=Translated TMP Button
LanguageLegacy=English\nThis example scene uses both the Legacy button and text box, plus an optional dropbox picker.
LanguageTMP=English\nThis example scene uses both the new TMP button and text box, plus an optional dropbox picker.

Sample Italian File
ButtonTxt=Pulsante tradotto
ButtonTMP=Pulsante TMP tradotto
LanguageLegacy=Italian\nQuesta scena di esempio utilizza sia il pulsante Legacy che la casella di testo, oltre a un selettore dropbox opzionale.
LanguageTMP=Italian\nQuesta scena di esempio utilizza sia il nuovo pulsante TMP che la casella di testo, oltre a un selettore dropbox opzionale.

