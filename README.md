import random                                           # grants us access to random oriented methonds.

print('_'*44)                                           # a line of 44 underscore characters.
print('This is a number guessing game.')                # explain the program to the users.
print('The hidden number may be from 0 to 100.')
print('Try to find the secret number, best of luck!')
print('-'*44 )                                          # the lines make the program more visibly presentable.
secret_num = random.randint(0,100)                      # the computer chooces a random number.

while True:                                             # we iterating the guessing process.
    try:
        user_guess = int(input('Take a guess:'))        # the user is guessing a number.
                                                        # the try & except statements cover the error that occurs 
                                                        # in the case that the user does not enter a number.
                                                        # bypasses the erro, it's called "exception handling".
    except ValueError :
        print('Entry wasn\'t a number.')
        
        print('_'*22)
        continue                                        # the "continue" jumps back on the top of the loop.
                                                        # in order to ask again a number from the user.
    
    if user_guess < secret_num:                         # a condition
        print(f'The {user_guess} is too low.')
        print('_'*18)
                                                        # once the condition is true, the user guesses again.

    elif user_guess > secret_num:                       # another condition
        print(f'The {user_guess} is too high.')
        print('_'*18)
                                                        #as above, the user guesses again

    if user_guess == secret_num:                        # a finale condition
        print(f'YAY, {user_guess} is correct!')
        print('_'*18)

        break                                           # once the condition is true the user wins and the iteration stops.
    
