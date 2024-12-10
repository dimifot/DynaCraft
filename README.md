# DynaCraft

# Data Types

Βασική σύνταξη και δομές

```c
string a = "test";
int b = 6;
float c = 4.5;
float d = 2; // error
```
#Polymorfism

```c
def point2d() {
  object o = object();
  float o.x = 0.0;
  float o.y = 0.0;
  return o;
  }
def point2d(float x, float y) {
  object o = object();
  float o.x = x;
  float o.y = y;
  return o;
  }
def point2d(int x, int y) {
  object o = object();
  int o.x = x;
  int o.y = y;
  return o;
  }
point2d a = point2d();
point2d b = point2d(2.0, 3.0);
point2d c = point2d(2, 3);

```

#Access function member
```c
float a = test().result //1
float b = test(2.0, 3.0).result // 5
float c = test(2,3).result // 6
```
#Downcasting


```c
def vector() {
  object o = object();
  return o;
  }
def vector2d(float x, float y) {
  vector o = vector();
  float o.x = x;
  float o.y = y;
  return o;
  }
def vector3d(float x, float y, float z) {
  vector2d o = vector2d(x, y);
  o.x = o.x + 1; // we can do that
  float o.z = z;
  return o;
  }

vector3d c = vector3d(1, 2, 3);
vector a = vector3d(1, 2, 3);
vector b = vector2d(1, 2);

print(a.z); // error by static checks, not by interpreter
a.z = a.z+1; // error by static checks, not by interpreter

def norm(vector2d a) { // give access again to private fields
return a.x+a.y;
}
def norm(vector3d a) {
return a.x+a.y+a.z;
}
norm(a); // 6
norm(b); // 3

```

#Loops

If statement
```c
int x = 1;
if x>0:
{print("positive");}
else:
{print("negative");}
```

While Loop
```c
while b<=8: {b = b+1; print(“variable incremented”);}

```
