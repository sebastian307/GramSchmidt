from scipy import integrate
from scipy.integrate import quad
import numpy as np
import math


#Defining the inner products to be used

def polynomialSP(num1, num2):
    def calculatenum1num2(x):
        sum1 = 0
        i = 0
        for n in num1:
            sum1 = sum1 + n * (x**i)
            i = i+1
        
        sum2=0
        i=0
        for n in num2:
            sum2 = sum2 + n * (x**i)
            i = i+1
        return sum1*sum2
    
    return quad(calculatenum1num2, 0, 1)[0]
def SSP(vec1, vec2):
    return np.dot(vec1, vec2)
    
#Given a function calculating the inner product and a list of numpy-Arrays representing the basis to be normalized, the following function returns an array that contains
#an orthonormalized version of these arrays

def gs(func_sp, basis):
    finished = []
    for element in basis:
        reductions = np.zeros(basis[0].shape)
        for b in finished:
            reductions = reductions - func_sp(element, b) * b
        c = element + reductions
        finished.append(c / math.sqrt(func_sp(c,c)))
    return finished
