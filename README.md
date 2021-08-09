# Whole-Circle-Bearing-From-Coordinates
# Creating a user-defined function that takes horizontal coordinates of two points and gives the whole circle bearing of a line connecting that two points as an output.
# Sample Code and Output

# Code
# input coordinates of 2 points
x1=as.numeric(readline(prompt='Enter x coordinate of point 1: '))
y1=as.numeric(readline(prompt='Enter y coordinate of point 1: '))
x2=as.numeric(readline(prompt='Enter x coordinate of point 2: '))
y2=as.numeric(readline(prompt='Enter y coordinate of point 2: '))
# function
wcb=function(x1,y1,x2,y2){
  x=x2-x1
  y=y2-y1
  angle=atan(x/y)*(180/pi)
  # condition check
  if(x>0 & y>0){
    angle=angle
    print(paste('The whole circle bearing: ',angle, sep=''))
  }else if(x>0 & y<0){
    angle=angle+180
    print(paste('The whole circle bearing: ',angle, sep=''))
  }else if(x<0 & y>0){
    angle=angle+360
    print(paste('The whole circle bearing: ',angle, sep=''))
  }else{
    angle=angle+180
    print(paste('The whole circle bearing: ',angle, sep=''))
  }
}
# function call
wcb(x1,y1,x2,y2)

# Output
> # input coordinates of 2 points
> x1=as.numeric(readline(prompt='Enter x coordinate of point 1: '))
Enter x coordinate of point 1: 123456
> y1=as.numeric(readline(prompt='Enter y coordinate of point 1: '))
Enter y coordinate of point 1: 2543659
> x2=as.numeric(readline(prompt='Enter x coordinate of point 2: '))
Enter x coordinate of point 2: 123499
> y2=as.numeric(readline(prompt='Enter y coordinate of point 2: '))
Enter y coordinate of point 2: -2544987
> # function
> wcb=function(x1,y1,x2,y2){
+   x=x2-x1
+   y=y2-y1
+   angle=atan(x/y)*(180/pi)
+   # condition check
+   if(x>0 & y>0){
+     angle=angle
+     print(paste('The whole circle bearing: ',angle, sep=''))
+   }else if(x>0 & y<0){
+     angle=angle+180
+     print(paste('The whole circle bearing: ',angle, sep=''))
+   }else if(x<0 & y>0){
+     angle=angle+360
+     print(paste('The whole circle bearing: ',angle, sep=''))
+   }else{
+     angle=angle+180
+     print(paste('The whole circle bearing: ',angle, sep=''))
+   }
+ }
> # function call
> wcb(x1,y1,x2,y2)
[1] "The whole circle bearing: 179.999515840065"
> 


