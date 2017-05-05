# Counting-Project
#math

from random import shuffle, randint

trees = ['M' , 'M' , 'M' , 'O' , 'O' , 'O' , 'O' , 'B' , 'B' , 'B' , 'B' , 'B']

faliures = 0
trials = 10

for i in range(trials):
    
#No more than 2 birch trees next to each other
    shuffle(trees)
    print(trees)
    for j in range(9):
        if trees[j] + trees[j+1] + trees[j+2] + trees [j+3] == 'BBBB':
            faliures+=1
            break

print((trials-faliures)/trials*100, '%')
