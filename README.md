# random_story_generator
Creates a story by replacing placeholder words such as &lt;noun> by looking for a random word of that type

## Main Classes

<b>GladLibs</b> Program to tell a random story. Contains the following methods:
* <b>GladLibs</b> - constructor used to initialize the following private variables:
  * *map* - a HashMap<String, ArrayList<String>> used to store all of the ArrayLists of words that will be used to randomly generated the story. Cleared upon initailization, then populated when <b>initializeFromSource</b> is called.
  * *catMap* - a HashMap<String, String> used to track words by category. Cleared upon initialization.
  * *seenWords* - an ArraList<String> used to track words that have been used already. Populated when <b>initializeFromSource</b> is called.
  * *myRandom* -a Random() used to generate random Integers.
  * *dataSourceURL* - a url directory that holds txt files used to populate the various ArrayLists of words.
  * *dataSourceDirectory* - directory that holds txt files used to populate the various ArrayLists of words.
  * calls <b>initializeFromSource</b> to populate *map* with the following ArrayList<String>:
    * *adjectiveList* - an ArrayList<String> of adjectives.
    * *nounList* - an ArrayList<String> of nouns.
    * *colorList* - an ArrayList<String> of colors.
    * *countryList* - an ArrayList<String> of countries.
    * *nameList* - an ArrayList<String> of names.
    * *animalList* - an ArrayList<String> of animals.
    * *timeframeList* - an ArrayList<String> of times.
    * *verbList* - an ArrayList<String> of verbs.
    * *fruitList* - an ArrayList<String> of fruits.
* <b>initializeFromSource</b> - populates *map* with the above ArrayList<String>
* <b>getSubstitute</b> - replaces all the if statements that use category labels with one call to <b>randomFrom</b> that passes the appropriate ArrayList from *map*.
* <b>processWord</b> - takes in a <word> as a String, then uses <b>getSubstitute</b> to find and return a replacement word. 
* <b>printOut</b>
* <b>fromTemplate</b>
* <b>readIt</b>
* <b>totalWordsInMap</b>
* <b>totalWordsConsidered</b>
* <b>makeStory</b>

## Conceptual Classes

<b>WordFrequencies</b> - program to determine the word that occurs the most often in a file. Contains the following methods:
* <b>WordFrequencies</b> - constructor used to initialize the following private variables:
  * *myWords* - ArrayList of type String to store unique words from a file
  * *myFreqs* - ArrayList of type Integer. The kth position in *myFreqs* represents the number of times the kth word in myWords occurs in the file.
* <b>findUnique</b> - first clears both *myWords* and *myFreqs*, using the .clear() method. Then it selects a file and then iterates over every word in the file, putting the unique words found into *myWords*. For each word in the kth position of *myWords*, it puts the count of how many times that word occurs from the selected file into the kth position of *myFreqs*.
* <b>findIndexOfMax</b> - returns an int that is the index location of the largest value in *myFreqs*. If there is a tie, then return the first such value.
* <b>tester</b> - calls findUnique, then prints out the number of unique words, and for each unique word, print the frequency of each word and the word. Uses <b>findIndexOfMax</b> to determine and print the word that occurs the most often in a selected file and how many times it occurs.

<b>CharactersInPlay</b> - Program to determine character with most speaking parts in a play. Contains the following methods:
* <b>CharactersInPlay</b> - constructor used to initialize the following private variables:
  * *myWords* - ArrayList of type String to store unique words from a file
  * *myFreqs* - ArrayList of type Integer. The kth position in *myFreqs* represents the number of times the kth word in *myWords* occurs in the file.
* <b>update</b> - has one String parameter named person. This method updates the two ArrayLists, adding the character’s name if it is not already there, and counting this line as one speaking part for this person.
* <b>findAllCharacters</b> - opens a file, and reads the file line-by-line. For each line, if there is a period on the line, extracts the possible name of the speaking part, and calls <b>update</b> to count it as an occurrence for this person.
* <b>charactersWithNumParts</b> - has two int parameters named num1 and num2, where you can assume num1 should be less than or equal to num2. This method prints out the names of all those characters that have exactly number speaking parts, where number is greater than or equal to num1 and less than or equal to num2. 
* <b>tester</b> - used to test the class, finding the character with the highest frueqency of speaking parts
* <b>testRange</b> - used to find all characters with speaking part frequencies between a minimum and maximum threshold.

Link to exercise: https://www.coursera.org/learn/java-programming-arrays-lists-data/supplement/AbpYj/programming-exercise-telling-a-random-story
