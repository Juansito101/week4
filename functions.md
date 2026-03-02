Functions in Python





Create a unit conversion program using functions




1a. The user selects kilometers per liter (kpl), and the response will be provided in miles per gallon (mpg). The units must be interchangeable, so the program will ask the user whether to convert from kpl to mpg or vice versa.


# define conversion factor
conv_f = 2.35215

# conversion kpl to mpg
def kpl_to_mpg(kpl):
    return kpl * conv_f

# conversion mpg to kpl
def mpg_to_kpl(mpg):
    return mpg / conv_f


print("Fuel Converter")
print("1. KPL to MPG")
print("2. MPG to KPL")

choice = input("Choose conversion (1 or 2): ")

if choice == "1":
    kpl = float(input("What's the KPL: "))
    mpg = kpl_to_mpg(kpl)
    print(f"{kpl:.2f} KPL = {mpg:.2f} MPG")

elif choice == "2":
    mpg = float(input("What's the MPG: "))
    kpl = mpg_to_kpl(mpg)
    print(f"{mpg:.2f} MPG = {kpl:.2f} KPL")

else:
    print("Error. Not a valid choice.")






1b. How would you write a function that could take any number of unnamed arguments and print their values out in reverse order?


def print_reverse(values):
    # read list in reverse
    for value in values[::-1]: #use slicing, take the sequence and step backwards
        print(value) #then print








1c. What would be the result of changing a list or dictionary that was passed into a function as a parameter value?



The result of changing a list or dictionary into a function as a parameter value will change all the key and values and get a reference to the orignial content.






Which operations would be likely to create changes that would be visible outside the function? 


It would depend on whether the object is mutable or can modified inside a function.




What steps might you take to minimize that risk?


By making a copy can minimize the risk.



Explain the above statements with the help of code.
?????????????//








1d. Assuming that x = 5, what will be the value of x after funct_1() below executes? After funct_2() executes?

x = 5
def funct_1():
  x=3

def funct_2():
  global x
  x=2



the value of x after funct_1() is:   5










2. Troubleshooting
Correct the following code. There might be more than one correct answers. Explain your reasoning.



def my_func(a,b,**c)  #**c only accepts keyword arguments
  print(c)

my_func(1,2,3,4,5,6)



def my_func(a, b, *c):   # replace **c with **c
    print(c)

my_func(1, 2, 3, 4, 5, 6)








Using the following code, x should print 100 but it prints 10, why?

def my_func_global():
  x = 100

global x   
x = 10
my_func_global()
print(x)




It does not print 100 because global x is set to 10 so printing (x) prints only 10.
x = 100 creates a local variable inside the function and does not effect the global x and works with its own local x.







Challenges
Please describe the challenges you faced during the exercise.



# It was challenging to remember how global can effect the function inside and out
# Using slicing and remembering how to use negative numbers to reverse order
# 
#






















