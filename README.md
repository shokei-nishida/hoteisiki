# hoteisiki

from sympy import *
import math
from sympy.plotting import plot
import random
import numpy
from numpy.random import * 

import matplotlib.pyplot as plt




x = Symbol('x')
y = Symbol('y')
n = Symbol('n')
p = math.sqrt(2*math.pi)
q=1/p

h=q*exp(-(x*x)/2)

i=q*exp(-y*y/2)

g = integrate(h,(x,-oo,y))

gg=g**(n-1)
ggi=gg*i

ggyi=y*ggi*n
ggyii=integrate(ggyi,(y,-oo,oo))
ggyiii=ggyii-2.32
sol=solve(ggyii, n) # 解をsolに格納
print(sol)
