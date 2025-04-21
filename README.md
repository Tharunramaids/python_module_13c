# Tower of Hanoi in Python

## Aim
To implement the Tower of Hanoi problem using recursion in Python and display the steps to move disks from the source to the destination peg.

## Procedure
1. The Tower of Hanoi is a classic recursive problem where:
   - There are three rods: Source, Destination, and Auxiliary.
   - The objective is to move `n` disks from the Source rod to the Destination rod.
2. Use a recursive function:
   - Move `n-1` disks from Source to Auxiliary using Destination as temporary storage.
   - Move the nth (largest) disk from Source to Destination.
   - Move `n-1` disks from Auxiliary to Destination using Source as temporary storage.
3. Base case: When `n == 1`, move the disk directly from Source to Destination.

## Program

```python
def TowerOfHanoi(n, source, destination, auxiliary):
    if n == 1:
        print(f"Move disk from {source} to {destination}")
        return
    TowerOfHanoi(n-1, source, auxiliary, destination)
    print(f"Move disk from {source} to {destination}")
    TowerOfHanoi(n-1, auxiliary, destination, source)

# Input
n = int(input())
print("No. of disks =", n)

# Function call
TowerOfHanoi(n, 'A', 'C', 'B')
```

## output
![Screenshot 2025-04-20 212740](https://github.com/user-attachments/assets/b859742e-c6c1-4c21-ab36-cd3ee96e7efd)


## Result
The program successfully prints the steps required to move all disks from the source peg to the destination peg using the Tower of Hanoi algorithm.
