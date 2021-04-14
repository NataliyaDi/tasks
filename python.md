---
Python data types

l1 = [1, 2, 3, 4, 5]
l1[1:3][0]=1000
print(l1)  #???



l2 = [1, [0, 2], 3, 4, 5]
l2[1:3][0][0]=1000
print(l2)  #???

---
Visibility

def a():
    V = 2
    print(V)
def b(V=3):
    print(V)
def c():
    print(V)

V = 1

a()  # ???
b()  # ???
c()  # ???



def func(L=[]):
    L.append(1)
    return L

print(func())    # ???
print(func())    # ???
print(func([]))  # ???
print(func())    # ???


---
Class and inheritance

class A:
    def m(self):
        print('A')

class B:
    def m(self):
        print('B')

class C(B, A):
    pass

class D(A, B):
    pass

class E(A, B):
    def m(self):
        print('E')

C().m()  # ???
D().m()  # ???
E().m()  # ???
