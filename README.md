# hello-world
example

import sys
import random

def main():
    flag = 0
    while flag == 0:
        ds = str(random.randrange(0, 10000))
        flag = 1
        if len(set(ds)) != len(ds):
            flag = 0
    c = 1
    while flag == 1:
        gs = str(input("Please have a guess (4 digits): "))
        if len(gs) != 4:
            print("Invalid input, try again.")
            continue
        a = len([ds[i] for i in range(0, 4) if ds[i] == gs[i]])
        b = len([i for i in ds if i in gs]) - a
        if a == 4:
            flag = 0
            print("Your answer is correct, you've guessed ", c, " times")
        else:
            print("There are ", a, " cow(s), and ", b, "bull(s)")
            c += 1

if __name__ == "__main__":
    main()
