# A javascript code which can be used to retrieve data from macOS Dictionary.app

You can use this code to make Automator Quick Action that retrieve definition from dictionary.app and hide original word from example sentences.


## Quick Action example
Automator - new Quick Action  
get text input from selection  
Set Value of Variable  
Get Value of Variable (You should check "ignore this action's input" on the option.)  
Run Shell Script (Write "open dict://$1" in shell script, and change Pass input to "as arguments".)  
get value of variable (You should check "ignore this action's input" on the option.)  
get definition of word (I used New Oxford American Dictionary.)  
Run Javascript (Copy and paste code from dict.js to here.)  
Set Contents of TextEdit Document  
  
Then assign shortcut to this action.
  
When you select a specific word and press shortcut, dictionary.app search result will show up, and the result will be written in new TextEdit file.  


## Limitations
- Formatting is not perfect. For example, if there are keywords like "noun" in definition of word, formatting might not act as intended. Also, places of "[with object]" kind of things might not the same as original dictionary.
- I test this code only with *New Oxford American Dictionary (English (US))*.
