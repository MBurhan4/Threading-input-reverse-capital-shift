# Threading-input-reverse-capital-shift

You have to create four threads other than main thread. 
1. Input thread 
2. Reverse thread 
3. Capital thread 
4. Shift thread 
Input thread will take string input from user, reverse thread will reverse the string and output it, 
capital thread will capitalize the characters of string and output it and shift thread will shift each 
characters of the string two time (e.g. a will become c) and output it. All the threads wait for input 
thread when input thread finishes his task all the waiting thread start their work simultaneously. 
You also have to handle the exceptions of input thread. Also take care the state of each thread. Do 
not waste your memory resources.

# Python code;
#used to run multiple threads (tasks, function calls) at the same time
import threading

It allows functionality like getting the current time, pausing the Program from executing, etc. So before starting with this module we need to import it

import time

Here it takes input from the user

def input_function():

    print("Your string is:  ",string)
    
 the reverse fuction returns a reversed object or iterator of the input string
 
def reverse_function():

    print("reverse string:  ",string[::-1])
    
It returns a string where the first character is upper case, and the rest is lower case.

def capitalize_function():

    print("capitalize  string:  ",string.capitalize())
    
 It represents the number of shifts to be made over the desired axis
 
def shift_function():

    data=[]
    
    for i in string:
    
        if i.strip() and i in strs:
        
            data.append(strs[(strs.index(i) + 2) % 26])
            
        elif i.strip() and i in STRS:
        
            data.append(STRS[(STRS.index(i) + 2) % 26])
            
        else:
        
            data.append(i)
            
    output=''.join(data)
    
    print("shifting character:  ",output)

string=input("ENTER THE STRING:   ")

strs='zyxwvutsrqponmlkjihgfedcba'

STRS='ZYXWVUTSRQPONMLKJIHGFEDCBA'

input_function()

reverse_function()

capitalize_function()

shift_function()

t1 = threading.Thread(target=input_function, name='t1')

t2 = threading.Thread(target=reverse_function, name='t2')

t3 = threading.Thread(target=capitalize_function, name='t3')

t4 = threading.Thread(target=shift_function, name='t4')

Output;

![ioi](https://user-images.githubusercontent.com/92621862/210607670-f47bcb26-83e3-43e6-8237-8b34e4e1c5a4.PNG)
