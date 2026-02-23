Name: Alyssa O'Keefe
Date: 23/02/2026
Reflection for Part 1 of Quiz 1

1) When you type inside the <textarea>, the character counter updates automatically. Why?

Answer: The character counter updates instantly since the charCounter() method from app.js is directly called in index.html. As a result, v-model(stickie.txt) is able to create two-way data binding between <textarea> and the char counter. As the user continues to type the bound data property changes and is immediately rendered on the screen due to Vue reactivity.  

2) Explain what deep: true does and what would stop working if we removed it

Answer: deep: true specifies where in memory the contents should be stored. This is important for developing a wsebsite that keeps changes made to and doesn't automatically start over when the refresh button is pressed. 

3) localStorage questions
    a) What type of data does localStorage store? 
    
    Answer: localStorage stores data as key-value pairs to allow for information input by the user to be saved after the browser is closed.

    b) Why do we use JSON.stringify() when saving?

    Answer: Because localStorage only stores strings, JSON.stringify() converts JavaScript objects into a string format so they can be saved properly.

    c) What would happen if we forgot JSON.parse() when loading?

    Answer: When loading sorted data, if JSON.parse() is not specified then the data will string be a string datatype and not an array(stickies[]), which prevents it from used access properly by any of the app.js methods.

4) 
    a) What does .filter() return?

    Answer: .filter() returns an array of any of the items in stickies[] that match the specified condition. 

    b) Why assign the result back to this.stickies? Why !== and not ===? (I combined both because the answer flowed well together)

    Answer: By setting the parameter as (s=> s.id !== id), it creates an array of all the items that don't match the sticky id, and since the specified id is the one that is meant to be deleted, the new filtered list is an array with all the items that dont't have that id value. This is benefiticial for time complexities and simplifiying how to take away the correct value.

5) Why is saving implemented in a separate method (saveToStorage) instead of writing localStorage code directly in the watcher?

Answer: A separate saveToStorage() method to save data in order to keep the watcher simple and focused on updating changes. This makes the code easier to read, reuse, and update without cluttering the watcher with storage logic.

