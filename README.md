# Final-Project-Guess-That-Marvel By: Taha Anwar & Mohammad Anwar

import random

marvel = ['ironman', 'thor', 'spiderman', 'blackwidow', 'captainamerica', 'wolverine', 'blackpanther', 'drstrange', 'deadpool', 'hulk', 'scarletwitch', 'antman', 'hawkeye', 'ghostrider', 'nightcrawler', 'professorx', 'thing', 'groot', 'starlord', 'rocketraccoon', 'silversurfer', 'punisher', 'pheonix', 'gambit', 'vision', 'colossus']

word = random.choice(marvel)

correct = []
wrong = []

lives = -1
tries = 5
while tries > 0:
    output = ''
    for letter in word:
        if letter in correct:
            output += letter
        else:
            output += '_ '
    if output == word:
        break
    print("Take a guess: ",output)
    print(tries," lives left")
    attempt = input()
    if attempt in correct or attempt in wrong:
        print("try again", attempt)
    elif attempt in word:
        print("Good job!")
        correct.append(attempt)
    else:
        print("Incorrect")
        lives = lives - 1
        tries = tries-1
        wrong.append(attempt)

if tries>0:
    print("Great guess, you got the word correct")
else:
    print("Sorry, Try again.")


# video url: https://www.youtube.com/watch?v=QLsZGSrT46o&ab
