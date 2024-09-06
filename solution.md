# Line 109

if (guessString === rightGuessString) {
		let flag = rightGuessString + '@flare-on.com';
		toastr.options.timeOut = 0;
		toastr.options.onclick = function() {alert(flag);}
        toastr.success('You guessed right! The flag is ' + flag);

        guessesRemaining = 0
        return
    } else {
        guessesRemaining -= 1;
        currentGuess = [];
        nextLetter = 0;

        if (guessesRemaining === 0) {
            toastr.error("You've run out of guesses! Game over!")
            toastr.info('Try reverse engineering the code to discover the correct "word"!');
        }
    }

# Solution
There is no indicator that the element 57 lead we found in line 5 was changed or created as a "trapdoor". If you throw line 57 into the wordle prompt, it will appear incorrect. This is because source code starts from 1 instead of 0, which makes the correct answer "flareonisallaboutcats" from line 58.
