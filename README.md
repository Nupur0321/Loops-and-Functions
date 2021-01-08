# Loops-and-Functions
This repository will help to understand the loops and functions.

######################################################## #MAKE A CSV FILE AND READ IN ########################################################
The following is code that reads a csv file into R and saved it in a data structure called data. Modify the directories in this code and then run this code
#make directory C:\Users\xxxxx\Downloads")
getwd() 
setwd("C:\\Users\\Justin.McGuinness\\Downloads") 

#read in file
data=read.csv("Book1.csv", col.names=c("a","b","c"),header=F)

######################################################## #LAB IF STATEMENT EXERCISE ########################################################
Run the following block of code and explore which lines of code execute and why they execute. Next change “hello” to “one” and run this code, then change “hello” to “two” and run the code again. Finally, try running with x=1 and then with x=2. What do you notice?
x="hello" if(x==1){
print("one") }else if(x==2){ print("two")
}else{
print("not one or two")
}

Exercise 1
You should run the following code, which was discussed in the lecture earlier:
i=1 if(i==1){
print("one") }
if(i==2){ print("two")
}
i=2 if(i==2){
print("two") }


Exercise 2
You should run the following code, which asks the user to provide their name, and their age and then prints out a sentence using this information.
my.name <- readline(prompt="Enter name: ")
my.age <- readline(prompt="Enter age: ")
# convert character into integer
my.age <- as.integer(my.age)
print(paste("Hi,", my.name, "next year you will be", my.age+1, "years old."))
Use the help function in R to investigate any functions you are unfamiliar with.

Exercise 3
You should modify the code in Exercise 1 to allow the user to provide a value similar to that in Exercise 2
Exercise 4
You should now modify the code in Exercise 3 to be an if...else if statement rather than two separate if
statements.
Exercise 5
Change the code from Exercise 4 to include not just if and else if but also an else statement which
should output “not one or two”
Exercise 6
Drug markets around the world have different requirements in terms of safe and/or therapeutic quantities of certain chemicals/drugs present. For example, the US market generally has a lower standard compared to the EU.
You should build a function called quality which gets an inputted value from a user and returns EVERYWHERE if the inputted value is between 80 and 100, EU & US MARKET if the value is greater than 60 but less than 80, US MARKET ONLY if the value is greater than 40 but less than 60, and DISCARD if the value is less than 40. The code should inform the user that they have entered an incorrect value if the number entered is not between 0 and 100.
Exercise 7
The code in Exercise 6 should be modified so that if an invalid value is entered the user gets a second chance to enter the data. Some codes that may help you are provided below in Exercise 9.
Exercise 8
Modify the code in exercise 7 so that the user is continuously prompted to enter a correct value if an invalid value is given, i.e. the user should get more than one second chance (infinite chances).

Exercise 9
Try running the following lines of code and noting the output. ###Example loop print the numbers one to ten on the screen for (i in 1:10) {
print(i) }
############
#The following define various functions. Try playing around with these functions, with different inputs, to get different outputs.
#Example function to print "Hello World on the screen" helloworld <- function(){
print("Hello World!") }
#Write a funciton to square a number squared <- function(x){
x*x }
EuToD = function(e){ e*1.174391
}
#function to convert temperature (approximately) from Celsius to Fahrenheit TOf =function(c){
c*9/5+32 }

Exercise 10
Write a line of code to assign y a random uniformly distributed number between 1 and 10 [investigate the runif() function]. Write a nested if else statement which will print the value of y and state whether it is
- Less than 2
- Between 2 and 5 (not including 5)
- Between 5 and 9 (not including 9)
- Greater than or equal to 9
The output should be something like “y is 5.535017, which is between 5 and 9” [investigate the cat() command for printing to console].

Exercise 11
Write a for loop which assigns a random number between 1 and 100 to z. The for loop should do this 200 times; each time the loop should print the number, for example “The random number is 45.658616”.

Exercise 12
Modify the above for loop to end if a random number generated is greater than 90. If this happens, the code should also print “A number >90 found – Exiting loop”

Exercise 13
Write a for loop to generate the following matrix: 𝑀 =

Exercise 14
12345 2 4 6 8 10 3 6 9 12 15 4 8 121620 [5 10 15 20 25]
Write a loop that continuously generates a random number between 0 and 100 until one greater than 95 is found. The loop should also count how many numbers are generated and state how many cycles were needed to find a number greater than 95.

Exercise 15
Load the Edu_salary.csv file into a data frame in R. Now create a smaller data set containing all data relating to observations with salaries greater than or equal 45 [investigate the subset() function for this]. Then write this smaller data set to a new .csv file called High_Salary.csv

Exercise 16
Load the brainsize.txt file into a data frame in R. Display the structure & summary statistics of the data set. Calculate the sum of all variables except the gender variable.

Exercise 17
Write code which will convert NA values in the brainsize data frame to the mean of the appropriate variable. You should write the code in a general way such that this will work no matter where the NA appears – for example the code should work on another data frame, not just specifically this one.

Exercise 18
Add an id number variable to the dataframe and give each person a unique id number.

Exercise 19
Write code which will give the details of each person with an MRI count above 1,000,000.

Exercise 20
Explore and run the following code to get a feel for functions of multiple variables – note how you can have a function do (almost) any coding operation within itself.

############################### #Some plot functions ###############################
x=1:20; y=x*2 #defining data – this could be any data par(mfrow=c(3,2)) # What does this do?? 
plotstuff=function(a,b){
plot(a,b); plot(a,log(b)); hist(a); hist(b) # you can write this as 4 sepearate lines if you prefer }

plotstuff(x,y)


...............................................................................................

Solutions
data = read.csv(file.choose())
data
View(data)

#Exercise 1
i=1
if(i==1){
  print("one")
}

if(i==2){
  print("two")
  }

i=2
if(i==2){
  print("two")
  }    

#Exercise 2

my.name <- readline(prompt="Enter name: ")
my.age <- readline(prompt="Enter age: ")
my.name
my.age

# convert character into integer
my.age <- as.integer(my.age)
print(paste("Hi,", my.name, "next year you will be", my.age+1, "years old."))


#Exercise 3
i <- readline(prompt = "enter a value to check")
i=1
if(i==1){
  print("one")
}else if(i==2){
  print("two")
}else{
  print("not one or two")
}


#Exercise 4
i=1
if(i==1){
  print("one")
 }else{
  print("two")
}

i=2
if(i==2)
{
  print("two")
}    

#Exercise 5
i=1
if(i==1){
  print("one")
 }else if(i==2){
  print("two")
}else{
  print("not one or two")
}

#Exercise 6

val<- readline(prompt = "Enter the value: ")
quality <- function(val){
  if(val>= 80 & val<=100){
    print("EVERYWHERE")
  }else if(val>=60 & val<80){
    print("EU & US MARKET")
  }else if(val>=40 & val<60){
    print("US MARKET ONLY")
  }else if(val<40){
    print("DISCARD")
  }else{
    print("entered an incorrect value")
    }
}

quality(val)

#Exercise 7
val<- readline(prompt = "Enter the value: ")
quality <- function(val){
  if(val>= 80 & val<=100){
    print("EVERYWHERE")
  }else if(val>=60 & val<80){
    print("EU & US MARKET")
  }else if(val>=40 & val<60){
    print("US MARKET ONLY")
  }else if(val<40){
    print("DISCARD")
  }else{
    print("entered an incorrect value")
    val <- readline(prompt = "Enter the correct value")
  }
}

#Exercise 8
 quality <- function(){
  val<- readline(prompt = "Enter the value: ")
  repeat{
    if(val>= 80 & val<=100){
      print("EVERYWHERE")
      break
    }else if(val>=60 & val<80){
      print("EU & US MARKET")
      break
    }else if(val>=40 & val<60){
      print("US MARKET ONLY")
      break
    }else if(val<40){
      print("DISCARD")
      break
    }else{
      print("entered an incorrect value")
      val <- readline(prompt = "Enter the correct value")
  }
}
}
 quality()
#Exercise 9
for (i in 1:10) {
  print(i) 
}
helloworld <- function(){
  print("Hello World!") 
}
helloworld()


squared <- function(x){
  x*x }
squared(5)

EuToD = function(e){ 
  e*1.174391
}

EuToD(2)

TOf =function(c){
  c*9/5+32 
}

TOf(20)


#Exercise 10 (if we write with print NULL will also come in output)
y <-  runif(n = 1, min = 1, max = 10)
y
if(y<2){
  cat("y is", y, "less than 2")
}else if(y>=2 & y<5){
  cat("y is",y, "between 2 and 5")
}else if(y>=5 & y<9){
  cat("y is", y, "between 5 and 9")
}else{
  cat("y is", y, "greater than or equal to 9")
}

#Exercise 11

for (i in 1:200) {
  z <- runif(n=1, min=1, max=100)
  z
  cat("the random number is:",z,fill=TRUE)
}

#Exercise 12

for (i in 1:200) {
  z<-runif(n=1,min=1,max=100)
  z
  if(z<90) {
  cat("The number is:",z, fill=TRUE)
  }else{
  cat("A number is>90-Exiting loop",z, fill = TRUE)
  break
  }
}

#Exercise 13
A <- c(2,3,4,5)
B <- c(2,3,4,5)
M <- matrix(nrow = length(A), ncol = length(B))
for (i in 1:length(A)) {
  for (i in 1:length(B)) {
    M[i,j] <- (A[i]*B[j])
  }
}
M

#Exercise 14
count <- 0
repeat{
  num <- runif(10,min = 0,max=100)
  cat("The random num is:", num, "\n")
  count <- count+1
  if(num>95){
    cat("A number greater than 95 is found-exiting loop", "\n", "total cycles needed to find this is", count,"\n")
    cat("Total random numbers generated is", count)
    break
  }
}


#Exercise 15
mydata <- read.csv(file.choose())
mydata
newdata <- subset(mydata, Salary >= 45)
newdata
#write.csv to write the data into new data frame
write.csv(newdata, "High_Salary")
getwd()

#Exercise 16
#delim is used to read text file
mydata <- read.delim(file.choose())
mydata
str(mydata)
summary(mydata)
sum(mydata$FSIQ)
sum(mydata$VIQ)
sum(mydata$PIQ)
sum(mydata$Weight)
sum(mydata$Height)
sum(mydata$MRI_Count)



#Exercise 17
#this code will tell the total number of NA's
sum(is.na(mydata$Weight))
#this code will tell the true means total no. of NA's and false means left data
table(is.na(mydata$Weight))

#Exercise 18
id_number <- 1:7
id_number
mydata <- cbind(mydata, id_number= c(1,2,3,4,5,6,7))
mydata
emp.data

#Exercise 19
library(dplyr)
?filter
tmp_df <- filter(mydata, MRI_Count > 1000000)
tmp_df

#Exercise 20
x=1:20; y=x*2 #defining data – this could be any data 
par(mfrow=c(3,2)) # What does this do?? 
plotstuff=function(a,b){
plot(a,b); plot(a,log(b)); hist(a); hist(b)# you can write this as 4 separate lines if you prefer 
}
plotstuff(x,y)
c <- par(mfrow=c(3,2))
c

