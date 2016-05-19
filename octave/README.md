# Octave/Matlab book

## Resources
* [Octave doc](https://www.gnu.org/software/octave/doc/interpreter/)

## Comments with %

```matlab
% line comment
```

## Basic operators

```matlab
2+4
10-5
6/4
43*19
2^10 %pow
```

## Variables

```matlab
s = 10; % ; non verbose
```

## Display

```matlab
disp('Hello world')
```

###Format

```matlab
disp(sprintf('%0.2f', 1.2345)) % 1.23
```

## Matrix operations

### Intialization

```matlab
A = [1,2,3; 2,3,4; 5,6,7]
A = [1:0.5:10] % a,step,b all inclusive
A = [1:10] % a,b stepsize of 1
A = ones(N) ; NxN mat of 1's
A = ones(M, N) ; MxN mat of 1's
A = zeros(N) ; NxN mat of 0's
A = zeros(M, N) ; MxN mat of 0's
A = eye(N) % NxN identity
```

### Dimensions

```matlab
size(A) % [len i, len j]
size(A, 1) % [len i]
length(A) % len of largest
```

### Vector ops

```matlab
log(A) % [log(A)], etc
A' % transpose
```

### Element wise ops

```matlab
A.+2 % mult each elem by 10
A.*10 % mult each elem by 10
```

## Matrix indexing

```matlab
%indexing starts at 1
A(i,j) % elem i,j
A(i,:) % get i row
A(:,j) % get j col
A(:,j) = [1,2,3]' % replace column
A(1:5, :) %submatrix
A = [A, [1,2,3]] % append matrix
```

## Plotting

### 2D

basic

```matlab
x = linspace(-10, 10, 50); % 50 samples from -10, 10
y1 = sin(x);
y2 = cos(x);
plot(x, y1);
hold on;  % holds sin to put also cos
plot(x, y2);
xlabel('time');
ylabel('value');
legend('sin','cos');
title('sin vs cos');
```

### 3D

```
%process grid
x = linspace(0,10, 30);
y = linspace(0,10, 30);
z = sin(x)
[xx,yy] = meshgrid(x,y);
zz = meshgrid(z);
%plot
mesh(xx, yy, zz) % 3d
meshc(xx,yy,zz) % 3d with contour
contour(xx,yy,zz) %contour plots
```

## Data

### Status

```
who % info variables short
whos %info variables long
```

### Load

```matlab
load 'data.mat' % loads in 'data' var
```

### Save

```matlab
save 'data.mat' data % save 'data' var in 'data.mat' file
```

## Flow control and looping

```matlab
i=0
if i == 0
  %something
elseif
  %something
else
  %something
end
```

```matlab
for i=1:10
  %something
end
```

```matlab
i=0
while i < 10
  %something
  i++
end
```

## Functions

in foo.m

```matlab
function [retval1, retval2] = foo(param1, param2)
	%somecode
  retval1 = 10*param1
  retval2 = 50*param2
```

in main file

```matlab
[x,y] = foo(10, 30) % autoloads foo.m
```

## misc functions

```matlab
mean(A) % mean
sum(A) % sums all elems
sum(A, D) % sums elems of D dimension
std(X) % standard deviation
imagesc(A)
pinv(A) % pseudo inverse
max(A) %max elem
min(A) %min elem
floor(A) 
ceil(A)
rand(M,N) % MxN matrix of rand elems from 0,1
```

## Command line

same commands as any linux

```
doc ls % help on command [command]
ls
cd
pwd
```

## Packages

```
pkg install
pkg load <pkg_name>
```