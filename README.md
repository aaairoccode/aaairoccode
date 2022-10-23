Due to the requirement of anonymity, we can not share the database and model checkpoint we used, but we promise to open source if the paper is accepted.
Also, we are not allowed to . We only briefly describe the code.

(1) Write lyrics in 'lyrics.txt', one line for each song. Set the lyrics language and a chord progression for each song in 'chord.txt'. We have provided bilingual examples in the two files.

(2) Run the ROC:
  ```shell
   python lyrics_to_melody.py
   ```
For each line in 'lyrics.txt', ROC generates a midi file named as the first sentence in lyrics.

(3) Here are the arguments of the script:

|Argument|Default value|Help|
|----|----|----|
|--lyrics_path|default='lyrics.txt'|Lyrics file path|
|--chord_path|default='chord.txt'|Chord prgressions file path|
|--db_path|default='database/ROC.db'|Database path|
|--debug|action='store_true'| If true, output composition details|
|--sentiment|action='store_true'| If true, automatically set tonality by analyzing sentiment.|

Beyond given arguments, there are some functions can be extended, e.g., because ROC is language-insensitive, you can modify a few lines to support other languages. Such extensions are pointed out in comments of the code.

Other files are about constructing the database or the model so details of them are omitted here.
