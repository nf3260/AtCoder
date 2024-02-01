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
