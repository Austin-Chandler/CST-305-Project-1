#Austin Chandler
#CST-305
#This is my own work

#The equation I am working with is throughput = inventory / time
#To simplify this I am calling inventory some constant k and time t. dx/dt is throughput
#The equation in numerical terms is dx/dt = k / t

#Importing the necessary libraires to solve the ODE
import numpy as np #importing numpy so I can define t as an linear space of numbers
from scipy.integrate import odeint #using odeint from scipy to solve the ODE
import matplotlib.pyplot as plt #importing the matplot library to plot the solution

def model(x,t,k):   # function that returns dx/dt
    dxdt = k / t    # The equation that was defined earlier
    return dxdt     # returning the result


x0 = 5 # Initial condition

t = np.linspace(1,20) # Setting the time points

# solve ODE
k = 5                               #for 5 items in inventory
x1 = odeint(model,x0,t,args=(k,))   #Calculate result and save to x1
k = 10                              #for 10 items in inventory
x2 = odeint(model,x0,t,args=(k,))   #Calculate result and save to x2
k = 20                              #for 20 items in inventory 
x3 = odeint(model,x0,t,args=(k,))   #Calculate result and save to x3

# plot results
plt.plot(t,x1,'r-',linewidth=2,label='k=5')     #ploting result at k = 5
plt.plot(t,x2,'b--',linewidth=2,label='k=10')   #ploting result at k = 10
plt.plot(t,x3,'g:',linewidth=2,label='k=20')    #ploting result at k = 20
plt.xlabel('time') #x-axis label as "time"
plt.ylabel('x(t)') #y-axis label as "x(t)"
plt.legend() #display which line is which
plt.show() #show the plot
