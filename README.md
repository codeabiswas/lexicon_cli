# lexicon (v1.0.0)
```lexicon``` is a simple yet powerful English dictionary combining the powers of command-line and internet to vanquish any questions you may have regarding a word, all on your terminal window.

---
## Usage
```shell
echo "usage: lexicon [word1,word2,word3,...] args"
echo
echo "Options and arguments:"
echo
echo "[word1,word2,word3,...]:"
echo "To find the definition(s) of a word, put the word in a square bracket and simply hit Return."
echo "To find the definition(s) of multiple words, put the words in a square bracket and seperate the words"
echo "using a comma and NO spaces."
echo 
echo "args:"
echo "-ps, --partOfSpeech       : Part of Speech"
echo "-s, --synonym             : Synonyms"
echo "-a, --antoynm             : Antonyms"
echo "-e, --example             : An example sentence"
echo
echo "Any of the arguments can be -h or --help. This will show the above information on how to use lexicon."
echo "Simply typing the command itself will also bring these instructions up."
```

### Examples
_Input:_
```shell
lexicon [bike] -ps -s -a -e
```
_Output:_
```shell
=================================================================================================================

Definition(s) of bike:

[1] ride a bicycle

    Part of Speech: verb

    Example: not given

    Its synonym(s) are:
      - bicycle
      - cycle
      - pedal
      - wheel

[2] a motor vehicle with two wheels and a strong frame

    Part of Speech: noun

    Example: not given

    Its synonym(s) are:
      - motorcycle

[3] a wheeled vehicle that has two wheels and is moved by foot pedals

    Part of Speech: noun

    Example: not given

    Its synonym(s) are:
      - bicycle
      - cycle
      - wheel

Its antonym(s) are: none

=================================================================================================================
```
_Input:_
```shell
lexicon [night,hike] -e
```
_Output:_
```shell
=================================================================================================================

Definition(s) of night:

[1] the time after sunset and before sunrise while it is dark outside

    Example: not given

[2] Roman goddess of night; daughter of Erebus; counterpart of Greek Nyx

    Example: not given

[3] a period of ignorance or backwardness or gloom

    Example: not given

[4] a shortening of nightfall

    Example: they worked from morning to night

[5] darkness

    Example: it vanished into the night

[6] the dark part of the diurnal cycle considered a time unit

    Example: three nights later he collapsed

[7] the period spent sleeping

    Example: I had a restless night

[8] the time between sunset and midnight

    Example: he watched television every night

=================================================================================================================

Definition(s) of hike:

[1] an increase in cost

    Example: not given

[2] the amount a salary is increased

    Example: he got a wage hike

[3] increase

    Example: The landlord hiked up the rents

[4] a long walk usually for exercise or pleasure

    Example: she enjoys a hike in her spare time

[5] walk a long way, as for pleasure or physical exercise

    Example: hike the Rockies

=================================================================================================================
```
_Input: (This is to test how it handles a nonexistent English word)_
```shell
lexicon [awjefioajwief] -ps -s -a -e
```
_Output:_
```shell
=================================================================================================================
The word does not exist in the dictionary
=================================================================================================================
```

---
## Installation

**Note:** _This has only been tried and tested on Debian and MacOS. This installation guide may not work on other operating systems._

### Prerequisites
Install [jq](https://stedolan.github.io/jq/download/)

1. Clone this repository.
2. Unless you have one already, create a folder in your root directory called ```bin/```.
```script
cd ~
mkdir bin/ 
```
3. Add the absolute path of the ```bin/``` directory to the ```.bashrc``` or ```.bash_profile```.
    * In your ```bin/```, do a ```pwd``` command. The output of that command will be your absolute path to ```bin/```.
    * Open your ```.bashrc```. On the top of the file, add this line
    ```script
    export PATH=$PATH:<OUTPUT-OF-pwd>
    ```
4. Copy the ```lexicon``` script from the repository to the ```~/bin/``` folder.
```script
cp lexicon ~/bin/
```
5. Set ```lexicon``` as an executable in the ```~/bin/``` directory.
```script
cd ~/bin/
chmod +x lexicon
```
6. Type ```lexicon``` and hit the ```Return``` key to see the result.

_Input_:
```script
lexicon
```
_Output:_
```script
A simple yet powerful dictionary at your fingertips using the command-line.

usage: lexicon [word1,word2,word3,...] args

Options and arguments:

[word1,word2,word3,...]:
To find the definition(s) of a word, put the word in a square bracket and simply hit Return.
To find the definition(s) of multiple words, put the words in a square bracket and seperate the words
using a comma and NO spaces.

args:
-ps, --partOfSpeech       : Part of Speech
-s, --synonym             : Synonyms
-a, --antoynm             : Antonyms
-e, --example             : An example sentence

Any of the arguments can be -h or --help. This will show the above information on how to use lexicon.
Simply typing the command itself will also bring these instructions up.
```

---
## Acknowledgements
* ```lexicon``` is powered by [WordsAPI](https://www.wordsapi.com).

---
## Contributors
- Andrei Biswas <axb6972@rit.edu>

---
## License
```lexicon``` is under the [MIT License](https://github.com/codeabiswas/lexicon_cli/blob/master/LICENSE).