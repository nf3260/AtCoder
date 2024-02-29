# AtCoder

#DailyTrainingEasy15:30(1/30)

A,B,C,D,E=map(int,input().split())
m=[A,B,C,D,E]
m1=set(m)
print(len(m1))

N=int(input())
S=list(map(str,input()))
m=[]
for i in S:
  for _ in range(2):
    m.append(i)
print(''.join(m))

N,M=map(int,input().split())
A=list(map(int,input().split()))
B=list(map(int,input().split()))
A.sort()
B.sort()
for i in B:
  if i in A:
    A.remove(i)
    if i==B[-1]:
      ans="Yes"
    else:
      pass
  else:
    ans="No"
    break
print(ans)


#DailyTrainingEasy16:30(2/1)

def base_number(num):
      remainders = []
      while True:
          remainder = num % 2
          remainders.append(str(remainder))
          num //= 2
          if num == 0:
              remainders.reverse()
              binary = "".join(remainders)
              return binary
              break
            
A,B=map(int,input().split())
a=base_number(A)
b=base_number(B)

c=[]

if len(a)>len(b):
  for i in range(len(a)-len(b)):
    c.append(a[i])
  for j in range(len(b)):
    if a[j+i+1]==b[j]:
      c.append("0")
    else:
      c.append("1")
elif len(a)<len(b):
  for i in range(len(b)-len(a)):
    c.append(b[i])
  for j in range(len(a)):
    if a[j]==b[j+i+1]:
      c.append("0")
    else:
      c.append("1")
else:
  for j in range(len(a)):
    if a[j]==b[j]:
      c.append("0")
    else:
      c.append("1")
print(int(''.join(c),2))




#DailyTrainingEasy15:30(2/6)

N=int(input())
H=list(map(int,input().split()))
max=max(H)
if N==1:
    ans=1
else:
  for i in range(N):
    if H[i]==max:
      ans=i+1
    else:
      pass
print(ans)

#DailyTrainingEasy15:30(2/13)

L,R=map(int,input().split())
A=["a","t","c","o","d","e","r"]
k=[]
for i in range(L,R+1):
  k.append(A[i-1])
print(''.join(k))

S=list(map(str,input()))
a,b=map(int,input().split())
F=S[a-1]
S[a-1]=S[b-1]
S[b-1]=F
print(''.join(S))

#DailyTrainingEasy16:30(2/15)

S=map(str,input())
k=[]
for i in S:
  if i!="a" and i!="e" and i!="i" and i!="o" and i!="u":
    k.append(i)
  else:
    pass
print(''.join(k))


#DailyTrainingEasy16:30(2/22)

N=int(input())
S=list(map(str,input()))
A=[]
if "x" in S:
  ans="No"
else:
  for i in range(N):
    A.append(S[i])
    if "o" in A:
      ans="Yes"
    else:
      ans="No"
print(ans)

N=int(input())
A=["L","n","g"]
for i in range(N):
  A.insert(1,"o")
print(''.join(A))

#DailyTrainingEasy20:30(2/29)

x1,y1=map(int,input().split())
x2,y2=map(int,input().split())
x3,y3=map(int,input().split())
if x1==x2:
  x4=x3
elif x2==x3:
  x4=x1
else:
  x4=x2
if y1==y2:
  y4=y3
elif y2==y3:
  y4=y1
else:
  y4=y2
  
print(x4,y4)

x=int(input())
if x<40:
  ans=40-x
elif 39<x<70:
  ans=70-x
elif 69<x<90:
  ans=90-x
else:
  ans="expert"
  
print(ans)
