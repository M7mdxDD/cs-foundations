Exercise 6:
1) Mohamed in ASCII and Binary:
M = 77 = 01001101
o = 111 = 01101111
h = 104 = 01101000
a = 97 = 01100001
m = 109 = 01101101
e = 101 = 01100101
d = 100 = 01100100

2) 01000011 01010011 = 67 83 = CS
   01100111 01101111 00100001 = 103 111 33 = go!

3) "مرحبا" has 5 Arabic letters, each is 2 bytes in UTF-8 = 10 bytes (checked with echo -n "مرحبا" | wc -c).

4) #FF8800 -> R = 255, G = 136, B = 0
   Pure blue = #0000FF
   White = #FFFFFF
   Middle gray = #808080
Exercise 7:

1) (A AND B) OR (NOT C)
A B C -> Out
0 0 0 -> 1
0 0 1 -> 0
0 1 0 -> 1
0 1 1 -> 0
1 0 0 -> 1
1 0 1 -> 0
1 1 0 -> 1
1 1 1 -> 1

2) 4-NAND XOR
A B -> T -> Out
0 0 -> 1 -> 0
0 1 -> 1 -> 1
1 0 -> 1 -> 1
1 1 -> 0 -> 0
same as XOR.

3) De Morgan: NOT(A AND B) vs (NOT A) OR (NOT B)
0 0 -> 1 and 1
0 1 -> 1 and 1
1 0 -> 1 and 1
1 1 -> 0 and 0
both give the exact same output.

4)
a) XOR
b) AND
c) OR
d) NAND

Decision Log 1:
lost track of time in terminal and binary exercises.
wanted to skip division by 2.
when stuck I just checked where I flipped the bits wrong.