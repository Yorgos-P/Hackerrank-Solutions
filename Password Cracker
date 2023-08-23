#Does not pass all test cases due to inefficiency

#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'passwordCracker' function below.
#
# The function is expected to return a STRING.
# The function accepts following parameters:
#  1. STRING_ARRAY passwords
#  2. STRING loginAttempt
#
slope = []
def passwordCracker(passwords, loginAttempt):
    # Write your code here
    counter = 0
    if loginAttempt == '':
        return ' '.join(slope)
    for i in range(0,len(passwords)):
        if passwords[i] == loginAttempt[:len(passwords[i])]:
            slope.append(passwords[i])
            loginAttempt = loginAttempt[len(passwords[i]):]
            return passwordCracker(passwords, loginAttempt)
        else:
            counter = counter + 1
            if counter == len(passwords):
                return 'WRONG PASSWORD'
            

            
            
        

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    t = int(input().strip())

    for t_itr in range(t):
        n = int(input().strip())

        passwords = input().rstrip().split()

        loginAttempt = input()

        result = passwordCracker(passwords, loginAttempt)
        
        slope.clear()

        fptr.write(result + '\n')

    fptr.close()
