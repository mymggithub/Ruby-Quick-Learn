#Ruby Quick Sheet

#/*----------  Primitive Data Types  ----------*/
=begin
Strings: A string is a sequence of characters. Strings are denoted by enclosing double ("") or single ('') quotation marks. "dog", "3 logs", and "the brown dog jumped over the 3 logs" are all strings. Strings can be of any length. "" is an empty string (a string of length zero). Remember to wrap strings in quotation marks. Otherwise Ruby will misinterpret the code.+

Numbers: In Ruby, we call any whole number—positive or negative (including 0)—an integer. 9 and -4 are both integers. Fractional numbers (with decimal points) such as 3.1415 are called floats or floating point numbers. Some mathematical operations in Ruby function differently depending on whether the number is a float or an integer. By the way, don't use include commas in integers. Writing 4,000 instead of 4000 will confuse Ruby.
Booleans: There are only two boolean values: true and false. Booleans provide the core logic of computer programs. 4 > 5 is false, and 4 < 5 is true. Note that booleans are case sensitive. true is a boolean, True is not. And "true" is a string, not a boolean.
Nil: Ruby represents nothingness with the keyword nil. Sometimes the absence of data is as important as data itself.
=end

#/*----------  Hello, world  ----------*/
puts "Hello, world"


#Variable
a = true
b = "dog"
b = a
a = 7.5


#/*----------  A Comment on Comments  ----------*/
# my favorite dessert!
fave_dessert = "pie"

=begin
Guess how many pies I can eat in one sitting.
You ready?
=end

num_pies = 3.14 # :)

#/*----------  Arithmetic Operators  ----------*/
2 + 3
2 - 3
2 * 3
2 / 3
2 ** 3

#/*----------  use floats  ----------*/
5.0 / 2.0 #=> 2.5
4.0 / 2.0 #=> 2.0
5 / 2.0 #=> 2.5
4.0 / 2 #=> 2.0

#/*----------  modulo operator  ----------*/
#/*----------  returns the remainder of division  ----------*/
5 % 2 #=> 1
5.0 % 2.0 #=> 1.0
4 % 2 #=> 0
4.0 % 2.0 #=> 0.0

#/*----------  Numerical Methods  ----------*/
#absolute value
-4.abs #=> 4
-2.5.abs #=> 2.5
4.abs #=> 4
2.5.abs #=> 2.5

#even and odd
2.even? #=> true
3.even? #=> false

2.odd? #=> false
3.odd? #=> true


#/*----------  Type Conversion  ----------*/
2.9.floor #=> 2
2.5.floor #=> 2

2.1.ceil #=> 3
2.5.ceil #=> 3

2.51.round #=> 3
2.49.round #=> 2
2.5.round #=> 3

#int
2.9.to_i #=> 2
"1".to_i #=> 1


#string
2.9.to_s #=> "2.9"
3.to_s #=> "3"
true.to_s #=> "true"
nil.to_s #=> ""

#float
"1.0".to_f #=> 1.0
"1".to_f #=> 1.0
"1.9".to_i #=> 1
3.to_f #=> 3.0


#/*----------  LCM and GCD  ----------*/
#The least common multiple (LCM) of two numbers is the smallest nonzero number that is a multiple of both.
9.lcm(3) #=> 9
3.lcm(9) #=> 9

#The greatest common divisor (GCD) is the largest positive integer that is a divisor of both numbers.
9.gcd(3) #=> 3
3.gcd(9) #=> 3


#/*----------  Introduction to Methods  ----------*/
#/*----------  Method Definition  ----------*/
def add_two_numbers(num_one, num_two)
  num_one + num_two
end

add_two_numbers(1, 2)



def add_two_numbers(num_one, num_two)
  return num_one + num_two
end

add_two_numbers(1,2)

#/*----------  Returning from a Method  ----------*/
def whacky_returns(num_one, num_two)
  return num_one + num_two
  num_one = num_one + 1    #unreachable code
  return num_one - num_two #unreachable code
end

whacky_returns(1,2) #=> 3

#/*----------  Helper Methods  ----------*/
def add_two_numbers_and_return(num_one, num_two)
  num_one + num_two
end

x = add_two_numbers_and_return(1, 2) # x is 3
puts "X:"
puts x

add_two_numbers_and_return(1,2) - 1 # => 2


#Can call the methods without an argument howdy() like howdy
def howdy
  "Howdy"
end

def partner
  howdy + ", partner!"
end

partner #=> "Howdy, partner!"


#/*----------  Array Access  ----------*/
got_characters = ["Robb", "Sansa", "Arya", "Bran", "Rickon"]
got_characters[0]  # => "Robb" # got_characters.[](0) is equivalent but uglier
got_characters[3]  # => "Bran"
got_characters[20] # => nil (nothing exists at this index)



got_characters = ["Robb", "Sansa", "Arya", "Bran", "Rickon"]
last = got_characters[-1] #=> "Rickon"
third_to_last = got_characters[-3] #=> "Arya"
last + " " + third_to_last #=> "Rickon Arya"


#Three dots indicate an exclusive range: 0...11 is equivalent to 0..10
got_characters = ["Robb", "Sansa", "Arya", "Bran", "Rickon"]
got_characters[0..2] #=> ["Robb", "Sansa", "Arya"]
got_characters[0...-1] #=> ["Robb", "Sansa", "Arya", "Bran"]

#One can also declare a range of characters (e.g., "a".."c", "A"..."D"). One can type convert a range to an array using the to_a method:
(0..3).to_a #=> [1,2,3]
("A"..."D").to_a #=> ["A", "B", "C"]

# -1 is equivalent to the array's length minus one
got_characters = ["Robb", "Sansa", "Arya", "Bran", "Rickon"]
got_characters[0...-1] == got_characters[0...(got_characters.length - 1)] #=> true


#first and last
got_characters = ["Robb", "Sansa", "Arya", "Bran", "Rickon"]
got_characters.first #=> "Robb"
got_characters.last #=> "Rickon"



#/*----------  Array Assignment  ----------*/
blasphemous_characters = ["Robb", "Sansa", "Arya", "Bran", "Rickon"]
blasphemous_characters[0] = "Rick"
blasphemous_characters #=> ["Rick", "Sansa", "Arya", "Bran", "Rickon"]
blasphemous_characters[3..-1] = "Morty", "Snuffles" # this is called multiple assignment
blasphemous_characters #=> ["Rick", "Sansa", "Arya", "Morty", "Snuffles"]


blasphemous_characters = ["Robb", "Sansa", "Arya", "Bran", "Rickon"]
# because arrays are zero-indexed, the index blasphemous_characters.length (5) doesn't have a value
blasphemous_characters[blasphemous_characters.length] = "Morty"
blasphemous_characters #=> ["Robb", "Sansa", "Arya", "Bran", "Rickon", "Morty"]
blasphemous_characters[8] = "Rick"

# The Ruby interpreter fills in the empty indices with nil
blasphemous_characters #=> ["Robb", "Sansa", "Arya", "Bran", "Rickon", "Morty", nil, nil, "Rick"]


#/*----------  Array Concatenation  ----------*/
potpourri = [false, "Snuffles", nil]
potpourri.concat(["rick", 3]) #=> [false, "Snuffles", nil, "rick", 3]

# concat modifies the original array
potpourri #=> [false, "Snuffles", nil, "rick", 3]

# using concat with an empty array as an argument is pointless
potpourri.concat([]) #=> [false, "Snuffles", nil, "rick", 3]


#/*----------  Array Concatenation - addition operator (+) ----------*/
potpourri = [false, "Snuffles", nil]
potpourri + ["rick", 3] #=> [false, "Snuffles", nil, "rick", 3]

# + does not modify the array
potpourri #=> [false, "Snuffles", nil]

# variable reassignment
potpourri = potpourri + ["rick", 3]
potpourri #=> [false, "Snuffles", nil, "rick", 3]

#/*----------  push, pop, unshift, and shift ----------*/
potpourri = [false, "Snuffles", nil, "rick", 3]
potpourri.push([]) #=> [false, "Snuffles", nil, "rick", 3, []]
potpourri #=> [false, "Snuffles", nil, "rick", 3, []] (push modified potpourri)
tail = potpourri.pop #=> []
potpourri #=> [false, "Snuffles", nil, "rick", 3] (pop modified potpourri)
tail #=> []

#for the front of the array rather than the end, you can use the methods unshift and shift
potpourri = [false, "Snuffles", nil, "rick", 3]
potpourri.unshift([]) #=> [[], false, "Snuffles", nil, "rick", 3]
potpourri #=> [[], false, "Snuffles", nil, "rick", 3] (unshift modifies potpourri)
potpourri.shift #=> []
potpourri #=> [false, "Snuffles", nil, "rick", 3] (shift modified potpourri)


#/*----------  Array Concatenation - The shovel operator (<<)  ----------*/
potpourri = [false, "Snuffles", nil, "rick", 3]
potpourri << ["Jerry", "krombopulos_michael"] #=> [false, "Snuffles", nil, "rick", 3, ["Jerry", "krombopulos_michael"]]


#/*----------  Array Concatenation - join  ----------*/
[1, 2, nil, 3].join #=> "123"
[1, 2, nil, 3].join(" ") #=> "1 2  3" <-note the extra space to accommodate nil

ex = [1, 2, 3]
ex.join(" joint ") #=> "1 joint 2 joint 3"

# ex is not modified
ex #=> [1, 2, 3]

#/*----------  Other Useful Array Methods  ----------*/
[1, 2, 3, "a", "b", "c"].length #=> 6



[3, 1, 2].sort #=> [1, 2, 3]
["c", "a", "b"].sort #=> ["a", "b", "c"]
in_the_danger_zone = [3, 1, 2]
#sort has a counterpart that modifies the original array: sort!. 
#A bang (!) typically denotes methods that modify their receiver, so-called "dangerous" methods.
in_the_danger_zone.sort!
in_the_danger_zone #=> [1, 2, 3]



[nil, false, "ranger danger"].reverse #=> ["ranger danger", false, nil]
the_dangerest_rangerest = [nil, false, "ranger danger"]
#reverse has a dangerous version: reverse!.
the_dangerest_rangerest.reverse!
the_dangerest_rangerest #=> ["ranger danger", false, nil]

#include? returns a boolean value indicating whether its argument is included in the array.+
["a", "b", "c"].include?("a") #=> true
["a", "b", "c"].include?(1) #=> false


#/*----------  Introduction to Strings  ----------*/
#The only difference between array access and string access is that the first and last
# methods are unavailable to strings.
words_to_the_third = "Words, words, words."
words_to_the_third[0] #=> "W"
words_to_the_third[-1] #=> "."
words_to_the_third[2..10] #=> "rds, word"
words_to_the_third[2..-1] #=> "rds, words, words."
words_to_the_third[2..(words_to_the_third.length - 1)] #=> "rds, words, words."
words_to_the_third[99] #=> nil

scary_word = "palindromic"
scary_word[0] = "a"
scary_word #=> "aalindromic"
scary_word[1..6] = "ibohph"
scary_word[-3..-1] = "bia"
scary_word #=> "aibohphobia"


# concatenation with + does not modify the original array
broken_half_one = "we belong"
broken_half_two = "together"
broken_half_one + " " + broken_half_two #=> "we belong together"
broken_half_one #=> "we belong"

# use the assignment operator to modify broken_half_one
broken_half_one = broken_half_one + " "
broken_half_one = broken_half_one + broken_half_two
broken_half_one #=> "we belong together"

# concatenation with concat or << modifies the original array
broken_half_one = "we belong"
broken_half_two = "together"
broken_half_one.concat(" ")
broken_half_one #=> "we belong "
broken_half_one << "together"
broken_half_one #=> "we belong together"




"echo" * 4 #=> "echoechoechoecho"




#/*----------  split  ----------*/
proposition_one_point_two = "The world divides into facts."
proposition_one_point_two.split #=> ["The", "world", "divides", "into", "facts."]
proposition_one_point_two.split(' ') #=> ["The", "world", "divides", "into", "facts."]
proposition_one_point_two.split('d') #=> ["The worl", " ", "ivi", "es into facts."]
proposition_one_point_two.split('.') #=> ["The world divides into facts"]
proposition_one_point_two.split('')  #=>["T", "h", "e", " ", "w", "o", "r", "l",
                                     #    "d", " ", "d", "i", "v", "i", "d", "e",
                                     #    "s", " ", "i", "n", "t", "o", " ", "f",
                                     #    "a", "c", "t", "s", "."]

# the original string is not modified
proposition_one_point_two #=> "The world divides into facts."


#/*----------  Case Manipulation  ----------*/
"TWO-CASED STRING".downcase #=> "two-cased string"
"rOlLeR-cOaStEr StRiNg".downcase #=> "roller-coaster string"

"two-cased string".upcase #=> "TWO-CASED STRING"
"rOlLeR-cOaStEr StRiNg".upcase #=> "ROLLER-COASTER STRING"




"How many characters do I have?".length #=> 30

"stressed".reverse #=> "desserts"

"".empty? #=> true
"full".empty? #=> false

"".include?("f") #=> false
"full".include?("f") #=> true


#/*----------  Comparison Operators  ----------*/
3 > 2 #=> true
3 >= 2 #=> true
3 < 2 #=> false
3 <= 2 #=> false
3 == 2 #=> false
3 !=2 #=> true

#One can compare different data types only when checking for equality
[] == [] #=> true
["cat"] == ["cat"] #=> true
["cat"][0] >= ["cat"][0] #=> true #(equivalent to "cat" >= "cat")
#One can compare arrays only for equality, i.e., one array is neither greater nor less than another
["cat"] >= ["cat"] # throws an error


#/*----------  Logical Operators  ----------*/
true && true #=> true
false && true #=> false
false && false #=> false

true || true #=> true
true || false #=> true
false || false #=> false

!true #=> false
!false #=> true



#/*----------  Control Flow  ----------*/
3 < 5 && "cat" < "dog" #=> true
5 < 3 || "cat" != "cat" #=> false



2+3 #=> 5
[1,2,3,4].length #=> 4
"dog" > "cat" && 5 == 4 #=> false  



#/*----------  Conditional Statements  ----------*/
if 5 + 7 == 12
  puts "This code will be executed!"
end



if 2.odd?
  puts "Two is odd. Who knew?"
else
  puts "Two is even. All is well!"
end




if 2 == "dog"
  puts "Not executed."
elsif 2 == "cat" && 0 < 2
  puts "Not executed."
elsif "cat" == "dog" || 2 == "cat"
  puts "Not executed."
else
  puts "2, cat, and dog are not equal!"
end





if 2.odd?
  "2 is apparently odd"
elsif 2.even?
  puts "2 is even: we're in the outer elsif branch"
  if 2 > 100
    "2 is a large even number!"
  elsif 2 > 30
    "2 is a medium even number"
  else
    puts "2 is a small even number"
    puts "Then it must be true that the result of 2 + 30 is less than 60 and is even!"
    puts "I'll prove it!"
    "2 + 30 < 60 && (2 + 30).even? is " + (2 + 30 < 60 && (2 + 30).even?).to_s
    # The conditional statement evaluates to "2 + 30 < 60 && (2 + 30).even? is true"
  end
else
  "2 is apparently neither even nor odd."
end




#/*----------  Loops  ----------*/
#/*----------  While Loops  ----------*/
while 2 < 3
  2 + 3
end



counter = 0
while counter <= 10
  puts "This is iteration number " + counter.to_s + "!"
  counter = counter + 1
end





def first_num_greater_than_ten(arr_of_nums)
  index = 0
  while index < arr_of_nums.length #thereby iterating through the array
    if arr_of_nums[index] > 10
      return arr_of_nums[index]
    end
    index = index + 1 # check next index in array
  end
  # if no number meeting the criteria is found, the method implicitly returns nil
end

first_num_greater_than_ten([1,2,3,11])







i = 1 # we'll count how many numbers from 1-100 are evenly divisble by i
j = 1
while i < 6
  count = 0
  while j < 101
    # increment count of test numbers
    count += 1 if j % i == 0 # increment count if j is evenly divisible by i
    j += 1 # increment j to check next number up to 100
  end
  j = 1 # reset j so j < 101 is true for the next iteration
  puts "There are " + count.to_s + " numbers evenly divisible by " + i.to_s +  " from 1 to 100."
  i += 1 # increment i to check next number up to 5
end





# Define a method that returns a boolean indicating whether any two elements in the argument (an array) sum to 0.
def two_sum_to_zero?(arr)
  i=0
  while i<arr.length
    num_1=arr[i]
    j=i+1 
    while j<arr.length
      num_2=arr[j]
      if num_1+num_2==0
        return true
      end
      j+=1
    end
    i+=1
  end
  return false;
end

puts two_sum_to_zero?([1,-1])
puts two_sum_to_zero?([1,2,3,4])



#https://app-academy.gitbooks.io/prep-step-one/content/practice_problems.html