Dictionary in Python
1. Creating and accessing dictionary

1a) Create dictionary of your choice of keys and values. Create dictionary size of 10 elements.
# Creating a dictionary

empty_dict = {}
my_dict = {
"111":"value 1",
"222":"value 2",
"333":"value 3",
"444":"value 4",
"555":"value 5",
"666":"value 6",
"777":"value 7",
"888":"value 8",
"999":"value 9",
"1000":"value 10"}



1b) Take inputs from a user and add them in a dictionary called my_user_dict

my_user_dict = {} #create the empty dictionary

#use the while loop to be able to add multiple entries
while True:
    # get name and social security numbers
    ssn = input("ssn: ")
    name = input("name: ")

    #store the entries in a dictionary
    my_user_dict[ssn] = {"name": name}

    # should continue?
    cont = input("Continue? (Y/N); use only capitals!")
    if cont != 'Y':
        break
#print all the user entries once everything has been entered
print(my_user_dict)


Identify how many keys you need to create a dictionary.

You can create a dictionary with zero or more keys.  Keys must be unique like numbers strings or tuples.

Values can be anything  (numbers, strings, list, dictionaries)


-----------------------------------------------------------------------------

1c)

Converting tuples into a dictionary

# List of tuples where each tuple represents a key-value pair

a = [("a", 1), ("b", 2), ("c", 3)]

# Convert the list of tuples into a dictionary

res = dict(a)

print(res)
{'a': 1, 'b': 2, 'c': 3}


ans

list_of_tuples = [("name", "Jack"), ("gender", "male"), ("sport", "football")]
my_dict = dict(list_of_tuples)
print(my_dict)

results output

{'name: Jack, 'gender' : male, 'sport': football}


1c. Based on the given tuple, create a code which checks for valid key & value pairs, and check for key duplication.


#to validate key value pair


pairs = [('Name', 'Sarah Connor'), ('Date of birth', '1 Jan 1980'),
 ('Address', '1000 Black Mountain Drive', 92126),
 ('Name', 'Jim Hawkins')]

#my_dict_pairs = dict(pairs)

#not working because "Address" has length of 3 not 2

#to detect

for item in pairs:
	if not isinstance(item, tuple) or len(item) != 2:
	   print("Invalid key-value pair:", item)

not sure about the rest to correct user error and key duplication




1d. Convert the following list into a dictionary. Automate the process by using the loop.

# this is the data
data = [
    ('Scientific Name', 'Panthera tigris'), 
    ('Common Name', 'Tiger'),
    ('Family', 'Felidae'),
    ('Genus', 'Panthera'),
    ('Native Region', 'Asia'),
    ('Subspecies Traditionally Recognised', 9),
    ('Modern Classification', 'Mainland Asian tigers and Sunda Island tigers')
]

#create a dictionary from the data using a while loop
tiger_dictionary = {}

i = 0 # start with index 0
while i < len(data): # as long as the length of the index is less than 0
    key = data[i][0] # assign to key 0 
    value = data[i][1] # the value in 1
    tiger_dictionary[key] = value 
    i += 1 # this adds 1 each time


Restrictions: Do not use functions and/or exceptions in this exercise

1e. Use the following text and count the number of words using dictionary. Remember The or the counts as 2.



The tiger (Panthera tigris) is a large cat and a member of the genus Panthera native to Asia. It has a powerful, muscular body with a large head and paws, a long tail and orange fur with black, mostly vertical stripes. It is traditionally classified into nine recent subspecies, though some recognise only two subspecies, mainland Asian tigers and the island tigers of the Sunda Islands.





text = """The tiger (Panthera tigris) is a large cat and a member of the genus Panthera native to Asia. It has a 
powerful, muscular body with a large head and paws, a long tail and orange fur with black, mostly vertical stripes. 
It is traditionally classified into nine recent subspecies, though some recognise only two subspecies, mainland Asian 
tigers and the island tigers of the Sunda Islands."""

words = []
start = 0

# For loop using range
for i in range(len(text)):
    if text[i] == " ":
        words.append(text[start:i])
        start = i + 1

# Add last word in
words.append(text[start:len(text)])

# Count words using dictionary
word_count = {}


#the if and else is used 
for word in words:
    if word in word_count:
        word_count[word] += 1
    else:
        word_count[word] = 1

print("\nWord_Count", len(words))







2. Troubleshooting


d_orig = {123:"Coconut"}
d_copy = d_orig
print(d_orig)
print(d_copy)
{123: 'Coconut'}
{123: 'Coconut'}







2a. Change the content of d_copy and make sure the content does not affect the d_orig dictionary. Verify using the code.

# Write your code here




d_orig = {123:"Coconut"}
d_copy = d_orig
print(d_orig)
print(d_copy)

#change d_copy
d_copy = {456:"Pineapple"}
print(d_copy)
print(d_orig)









2b. If it changes the content of the original dictionary, then propose how can you solve this problem.

# Write your code here


It didn't change the content of the original directory.  If i modified d_copy [456] = "Pineapple"  

it would of changed the d_orig as well.







2c. Write a code that generates the following error and explain why there is such an error.





TypeError: unhashable type: 'list'



#Dictionary keys and elements are immutable and fixed values.  



unhash = {[4,5,6]: "Numbers"} 

print(unhash)


# output would: 

TypeError: cannot use 'list' as a dict key (unhashable type: 'list')






Challenges
Please describe the challenges you faced during the exercise.




# Remembering the different between list and dictionary

# It was challenging to remember the how to validate data 

# I could not figure out 1 c

# 

# 

# 






















