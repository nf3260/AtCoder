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
