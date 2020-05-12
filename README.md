# highestWin
Code to find the number of probable wins for first array when 2 arrays are given input with desired length



n = int(input())
p = []
q = []
r = []
for i in range(n):
    z = int(input())
    p.append(input().split(' '))
    q.append(input().split(' '))
for i in range(n):
    a = p[i]
    b = q[i]
    count = 0
    h = 0
    flag = 0
    l = max(a)
    a = list(a)
    b = list(b)
    a.remove(a[-1])
    b.remove(b[-1])
    a.sort()
    b.sort()
    for j in range(len(b)):
        x = b[0]
        k = 0
        for k in range(len(a)):
            if int(a[k]) > int(x):
                count += 1
                a.remove(a[k])
                break
            else:
                h += 1
    
        b.remove(x)
    r.append(count)
for i in range(n):
    print(r[i])
    
