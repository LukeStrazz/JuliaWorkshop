# Carson, Irvin, Strazzera - CSC321 Julia Programming Workshop

# Assign the value 10 to the variable x
x = 10

# Doing math with x's value
x + 1
11

# Reassign x's value
x = 1 + 1
2

# You can assign values of other types, like strings of text
x = "Hello World!"

# A “Char” value represents a single character: it is just a 32-bit primitive type
c = 'x'

typeof(c)
# Output is: Char

# A string literals are delimited by double quotes or triple double quotes 
str = "Hello, world!"

str = """Hello again, world!"""

# You can extract a substring using range indexing
str[4:9]
# Output is: "lo, wo"

# The :: operator can be used to attach type annotations
x::Int = 10
# Output is: 10


function sinc(x)::Float64
    if x == 0
        return 1
    end
    return sin(pi*x)/(pi*x)
end

typeof(sinc)
# Output is: Float64


# Using dictionaries, the "=>" syntax knows to declare a value to an element
myphonebook = Dict("Will" => "123-4567", "Irvin" => "098-7654")

# Adding to dictionary
myphonebook["Luke"] = "123-0987"

# Outputting dictionary
myphonebook
# WIll output values declared, ex: "Will" => "123-4567"

# Removing from the dictionary
pop!(myphonebook, "Will")

#Using tuples, elements are ordered, autmatically made
myfavoriteteams = ("yankees", "mets", "giants")

# NOTE: In Julia, the positioning for all containers starts at position 1, not 0!
# Finding a value in spot 1:
myfavoriteteams[1]
# Output is: "yankees"

# Arrays are declared with the "[]"
names = ["will", "Irvin", "Luke"]
# Finding in location 2:
names[2]
#Output is: "Irvin"

# In Julia, arrays are mutable, so we can reassign values in a position:
names[2] = "Matt"
names[2]
#Output is: "Matt"

# Using a while loop to output names:
i = 1
while 1<= length(names)
    name = names[i]
    println("Name found: $name")
    i += 1
end
# Output is:
# Name found: Will
# Name found: Matt
# Name found: Luke

# Using a for-loop to output names:
for name in names
    println("Name found: $name")
end
# Output is:
# Name found: Will
# Name found: Matt
# Name found: Luke

# Matrix initializeation:
m, n = 5,5 #rows and columns
A = zeros(m, n) # This will initialze the matrix will zeros in every position

# Using a for-loop to add values to the matrix:
for i in 1:m
    for j in 1:n
        A[i, j] = i + j
    end
end

# To output, call "A":
A
# This will output the matric with Float64 types

# To declare a function in Julia, using the "function" notation:
function f(x,y)
    x + y
end

# Using the function:
f(2,3)
# Output is: 5

# Using the Type argument "::" we can declare a type to a function, method or variable:
f(x::Float64, y::Float64) = 2x + y

f(2.0, 3.0)
# Output is: 7.0

typeof(f)
# Output is: Float64

# When overloadding a method, we can use the "methods" function to see the types used:
f(x::Number, y::Number) = 2x - y
f(2.0, 3)
# Output is: 1.0

#Calling "methods(f):
methods(f)
# Output is: 
# 2 methods for generic function "f" from Main:
# [1] f(x::Float64, y::Float64)
# @ none:1
#[2] f(x::Number, y::Number)
# @ none:1


# Example using array, dictionaries and the Plots package to create a visual graph of f(x^2)
using Plots

x = -3:0.1:3
f(x) = x^2
y = f.(x)

gr()
plot(x,y, label = "line")
scatter!(x,y, label = "points")