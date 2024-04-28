import numpy as np
c1 = [1, 1, 1, 1]
c2 = [1, - 1, 1, - 1]
c3 = [1, 1, - 1, - 1]
c4 = [1, - 1, - 1, 1] 
rc =[]
print("Enter the bits")
d1= int(input("Enter D1: "))
d2 =int(input("Enter D2: "))
d3 =int(input("Enter D3: "))
d4 =int(input("Enter 04: "))
r1= np.multiply(c1, d1)
r2= np.multiply(c2, d2)
r3=np.multiply(c3, d3)
r4=np.multiply(c4, d4)
res_Channel=r1+r2+r3+r4
print("Resultant Channel: ", res_Channel)
Channel=int(input("Enter the station to listen: "))
if Channel ==1:
  rc =c1
elif Channel==2: 
  rc =c2
elif Channel== 3: 
  rc =c3
elif Channel ==4:
   rc= c4
inner_product = np.multiply(res_Channel, rc)
print("Inner product", inner_product) 
res1 =sum(inner_product)
data= res1/len(inner_product)
print("Data bit that was sent is: ", data)
