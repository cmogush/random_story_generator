# random_story_generator
Creates a story by replacing placeholder words such as &lt;noun> by looking for a random word of that type

<b>WordFrequencies</b> - program to determine the word that occurs the most often in a file. Contains the following methods:
* <b>WordFrequencies</b> - constructor used to initialize the following private variables:
  * myWords - ArrayList of type String to store unique words from a file
  * myFreqs - ArrayList of type Integer. The kth position in myFreqs represents the number of times the kth word in myWords occurs in the file.
* <b>findUnique</b> - first clears both myWords and myFreqs, using the .clear() method. Then it selects a file and then iterates over every word in the file, putting the unique words found into myWords. For each word in the kth position of myWords, it puts the count of how many times that word occurs from the selected file into the kth position of myFreqs.
* <b>findIndexOfMax</b> - returns an int that is the index location of the largest value in myFreqs. If there is a tie, then return the first such value.
* <b>tester</b> - calls findUnique, then prints out the number of unique words, and for each unique word, print the frequency of each word and the word. Uses findIndexOfMax to determine and print the word that occurs the most often in a selected file and how many times it occurs.
