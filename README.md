# simple-mad-libs-variation-starter
A variation on Mad Libs

For this project, I decided to implement a naive, virtual version of "Mad Libs". "Mad Libs" is a popular 2-player word game. Typically, Player 1 chooses a story from a collection of stories. Each story is mostly complete, but there are blanks where certain parts of speech (pos) would go. Player 1 prompts Player 2 for those pos's without reading them the story. At the end, Player 1 reads the story out loud to Player 2. One funny example: https://www.youtube.com/watch?v=6iClgRjmTvc&list=PLykzf464sU98HizZQOzYfvUOjjRSm9XLA&index=7 .

In my application, Player 1 does not choose a story, but comes up with one. Then, the application prompts Player 2 for words, reconstructs the story with those words, and then Player 1 reads the story out loud. As we walk through the code, I will explain why / how the most appropriate structure to support my application is an array. More specifically, a dynamic array ADT with Python's list type.

The first part of my code just deals with getting user input. It explains directions, asks for names of the players, and offers titles for inspiration if Player 1 needs it. You can see in the above code that I entered my name, my friend's name, asked to see two rounds of potential title options, enter one of those titles, and then created my story.

The core of the application comes after the user's input, 'write' is entered, and is where I will explain the approach step-by-step. In my explanation, I will replace the user input story with some sample text for readibility and easier comprehension.

To process Player 1's input, I imported a word tokenizer from NLTK, which is a library with useful packages for NLP tasks with Python. As the name suggests, the word_tokenizer tokenizes our text into words (more specifically, it tokenizes a string into a list of substrings). NLTK tokenizer and pos-tagger instantiate a list of tuples, 'tagged' (In this explanation, I've labeled it 'sample_tagged'). The tuples that the pos tagger produce are composed of this tokenized word, and its associated part of speech. For an example of how this works, please see 'demo'.
