# random_story_generator
Creates a story by replacing placeholder words such as &lt;noun> by looking for a random word of that type

## Telling a Random Story

<b>WordFrequencies</b> - program to determine the word that occurs the most often in a file. Contains the following methods:
* <b>WordFrequencies</b> - constructor used to initialize the following private variables:
  * myWords - ArrayList of type String to store unique words from a file
  * myFreqs - ArrayList of type Integer. The kth position in myFreqs represents the number of times the kth word in myWords occurs in the file.
* <b>findUnique</b> - first clears both myWords and myFreqs, using the .clear() method. Then it selects a file and then iterates over every word in the file, putting the unique words found into myWords. For each word in the kth position of myWords, it puts the count of how many times that word occurs from the selected file into the kth position of myFreqs.
* <b>findIndexOfMax</b> - returns an int that is the index location of the largest value in myFreqs. If there is a tie, then return the first such value.
* <b>tester</b> - calls findUnique, then prints out the number of unique words, and for each unique word, print the frequency of each word and the word. Uses findIndexOfMax to determine and print the word that occurs the most often in a selected file and how many times it occurs.

<b>CharactersInPlay</b> - Program to determine character with most speaking parts in a play. Contains the following methods:
* <b>CharactersInPlay</b> - constructor used to initialize the following private variables:
  * myWords - ArrayList of type String to store unique words from a file
  * myFreqs - ArrayList of type Integer. The kth position in myFreqs represents the number of times the kth word in myWords occurs in the file.
* <b>update</b> - has one String parameter named person. This method updates the two ArrayLists, adding the character’s name if it is not already there, and counting this line as one speaking part for this person.
* <b>findAllCharacters</b> - opens a file, and reads the file line-by-line. For each line, if there is a period on the line, extracts the possible name of the speaking part, and calls <b>update</b> to count it as an occurrence for this person.
* <b>charactersWithNumParts</b> - has two int parameters named num1 and num2, where you can assume num1 should be less than or equal to num2. This method prints out the names of all those characters that have exactly number speaking parts, where number is greater than or equal to num1 and less than or equal to num2. 

Link to exercise: https://www.coursera.org/learn/java-programming-arrays-lists-data/supplement/AbpYj/programming-exercise-telling-a-random-story
