# Step 1

![image](https://github.com/user-attachments/assets/d43a22ea-295d-4a1e-8c25-d490a41499f7)
Here we see that the correct guess seems to be linked to line 57 from the words.js file:

![image](https://github.com/user-attachments/assets/5bd01657-7356-4775-9f74-b90b2fe2bab6)

# Step 2

Scrolling through the rest of the script, we can identify things such as a function that calls a "checkguess()" in lines 55-58:
![image](https://github.com/user-attachments/assets/12c653e1-7d4b-40c5-8ac5-16944c028bcf)

# Step 3

Next we can find the rightguess array which is located at line 109 in the script.js file. Looking into this code, we can identify that a string comparison is being used to compare user input to the correct guess. If the user inputs the correct word, the flag is also presented on the screen.
![image](https://github.com/user-attachments/assets/01550c67-217a-41a9-abf5-429fb527c561)

# Solution

There is no indicator that the element 57 lead we found in line 5 was changed or created as a "trapdoor". If you throw line 57 into the wordle prompt, it will appear incorrect. This is because source code starts from 1 instead of 0, which makes the correct answer "flareonisallaboutcats" from line 58.
