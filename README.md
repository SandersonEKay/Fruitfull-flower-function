# Fruitfull-flower-function
# Kayla Sanderson
# March 1st 2018
# drawing flowers


import turtle
#define turtle
polaris = turtle.Turtle()

#ask for input
flower = input("would you like to grow a flower? Y/N").strip("! ,?").upper()
if flower == "N":
  print("goodbye!")
  
if flower == "Y":
  flower_size = input("would you like that in small, medium or large?").strip("! ,?").lower()
  if flower_size == "small":
    flower_size = 20
  elif flower_size == "medium":
    flower_size = 40
  elif flower_size == "large":
    flower_size = 60

#provide more options to user
complicated = input("How complicated would you like your flower to be? easy? moderate? your girlfriends emotions(intense)?").strip("! ,?").lower()
if complicated == "easy":
  complicated = 90
elif complicated == "moderate":
  complicated = 50
elif complicated == "intense":
   complicated = 30
  
#define function
def Blue_circle(circle):
  polaris.left(complicated)
  #polaris.penup()
  #polaris.goto(3,10)
  #polaris.stamp()
  polaris.penup()
  polaris.goto(-5 ,-30)
  polaris.pendown()
  polaris.circle(i + 30)
  polaris.penup()
  polaris.color("blue")
  
#define a function that raises x to the power of y
def power(x,y):
  return x**y 
  
#use the function to continue to call larger drawings of flower
for i in range(flower_size):
  Blue_circle(power(2, i))

