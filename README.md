# Ass-13-5-22
Assignment-1
import math
n=int(input("Enter the n:"))
seive = [True for i in range(n+1)]
seive[0]=seive[1]=False
x=int(math.sqrt(n))
for i in range(2,x+1):
    if seive[i]:
        for j in range(i*i,n+1,i):
            seive[j]=False

ct=[i for i in seive if i==True]
return len(ct)
