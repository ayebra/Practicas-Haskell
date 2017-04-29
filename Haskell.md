# Ejercicios con Haskell
### Programación Lógica y Funcional
##### Martínez Yebra Beatriz Andrea #13490929
The following exercises are available at the following address: https://wiki.haskell.org/99_questions.

- - -

### **1.- Exercise 1**
Find the last element of a list.
- **Example in Haskell:**

	``` Prelude> myLast [1,2,3,4] ```
   ``` 4 ```
	``` Prelude> myLast ['x','y','z'] ```
	``` z ```
- **Solution:**
<img src="http://i63.tinypic.com/30v278z.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **2.- Exercise 2**
Find the penultimate element of a list.

- **Example in Haskell:**
``` Prelude> myButLast [1,2,3,4] ```
``` 3 ```
``` Prelude> myButLast ['a'..'z'] ```
``` 'y' ```
- **Solution:**
<img src="http://i66.tinypic.com/212zivl.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **4- Exercise 4**
Find the number of items in a list.

- **Example in Haskell:**

    ``` Prelude> myLength [123, 456, 789] ```
	``` 3 ```
	``` Prelude> myLength "Hello, world!" ```
	``` 13 ```
- **Solution:**
<img src="http://i65.tinypic.com/e8annm.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **8.- Exercise 8**
Delete consecutive duplicates of list items. If a list contains repeated elements, it must be replaced with a copy of the element. The order of the elements should not be changed.

- **Example:**

	``` (compress '(a a a a b c c a a d e e e e)) ```
	``` (A B C A D E) ```

- **Example in Haskell:**

	``` > compress "aaaabccaadeeee" ```
	``` "abcade" ```
- **Solution:**
<img src="http://i67.tinypic.com/awoupz.png" border="0" alt="Image and video hosting by TinyPic">

- - -



### **9.- Exercise 9**
Consecutive duplicate packages of list items in sublists. If a list contains repeated elements, they must be placed in separate sublists.

- **Example:**

	``` (pack '(a a a a b c c a a d e e e e)) ```
	``` ((A A A A) (B) (C C) (A A) (D) (E E E E)) ```

- **Example in Haskell:**

	``` *Main> pack ['a', 'a', 'a', 'a', 'b', 'c', 'c', 'a', 'a', 'd', 'e', 'e', 'e', 'e'] ```
	``` ["aaaa","b","cc","aa","d","eeee"] ```
- **Solution:**
<img src="http://i64.tinypic.com/jutqvp.png" border="0" alt="Image and video hosting by TinyPic">

- - -



### **10.- Exercise 10**
Coding the execution length of a list. Use the result of problem P09 to implement. The so-called run-length encoding data compression method. Consecutive duplicates of elements are coded as lists (N E) where N is the number of duplicates of element E.

- **Example:**

	``` (encode '(a a a a b c c a a d e e e e)) ```
	``` ((4 A) (1 B) (2 C) (2 A) (1 D)(4 E)) ```

- **Example in Haskell:**

	``` encode "aaaabccaadeeee" ```
	``` [(4,'a'),(1,'b'),(2,'c'),(2,'a'),(1,'d'),(4,'e')] ```
- **Solution:**
<img src="http://i68.tinypic.com/6t3edf.png" border="0" alt="Image and video hosting by TinyPic">

- - -



### **2.- Exercise 12**
Decode a coded run length list.
Given a list of generated runtime codes as specified in Problem 11. Build your uncompressed version.

- **Example in Haskell:**

	``` P12> decodeModified ```
	 ```[Multiple 4 'a',Single 'b',Multiple 2 'c', ```
	 ``` Multiple 2 'a',Single 'd',Multiple 4 'e'] ```
	``` "aaaabccaadeeee" ```

- **Solution:**
<img src="http://i66.tinypic.com/10p0xag.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **3.- Exercise 13**
Coding of execution length of a list (direct solution).
Directly implement the data compression method of run-length encoding. That is to say. Do not explicitly create sublists that contain duplicates, as in Problem 9, but only count them. As in Problem P11, simplify the list of results by substituting singleton lists (1 X) for X.

- **Example:**

	 ```* (encode-direct '(a a a a b c c a a d e e e e))```
	``` ((4 A) B (2 C) (2 A) D (4 E)) ```

- **Ejemplo en Haskell:**

	 ``` P13> encodeDirect "aaaabccaadeeee" ```
	 ``` [Multiple 4 'a',Single 'b',Multiple 2 'c', ```
	 ``` Multiple 2 'a',Single 'd',Multiple 4 'e'] ```
- **Solution:**
<img src="http://i64.tinypic.com/2ztm34m.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **4.- Exercise 14**
Duplicate items in a list.

- **Example:**

	 ``` * (dupli '(a b c c d)) ```
	 ``` (A A B B C C C C D D) ```

- **Ejemplo en Haskell:**

	 ``` > dupli [1, 2, 3] ```
	 ``` [1,1,2,2,3,3] ```

- **Solution:**
<img src="http://i66.tinypic.com/2ivk2gz.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **5.- Exercise 15**
Repeat items in a list a certain number of times.

- **Example:**

	 ``` (repli '(a b c) 3) ```
	``` (A A A B B B C C C) ```

- **Example in Haskell:**

	``` > repli "abc" 3 ```
 ``` "aaabbbccc" ```

- **Solution:**
<img src="http://i67.tinypic.com/282i7i0.jpg" border="0" alt="Image and video hosting by TinyPic">

- - -


### **6.- Exercise 16**
Delete each N'th element from a list.

- **Example:**

	 ``` (drop '(a b c d e f g h i k) 3) ```
	 ```(A B D E G H K) ```

- **Example in Haskell:**

	``` *Main> dropEvery "abcdefghik" 3 ```
	``` "abdeghk" ```

- **Solution:**
<img src="http://i64.tinypic.com/358dxrd.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **7.- Exercise 17**
Split a list into two parts; The length of the first part is given.
Do not use predefined predicates.

- **Example:**

	 ``` (split '(a b c d e f g h i k) 3) ```
	 ``` ( (A B C) (D E F G H I K)) ```

- **Example in Haskell:**

	 ``` *Main> split "abcdefghik" 3 ```
	``` ("abc", "defghik") ```

- **Solution:**
<img src="http://i64.tinypic.com/2vux24w.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **8.- Exercise 18**
Extract a portion of a list.
Given two indexes, i and k, the slice is the list that contains the elements between the i'th and k'th element of the original list (both boundaries included). Begin by counting items with 1.

- **Example:**

	``` (slice '(a b c d e f g h i k) 3 7) ```
	 ``` (C D E F G) ```

- **Example in Haskell:**

	 ```*Main> slice ['a','b','c','d','e','f','g','h','i','k'] 3 7 ```
	``` "cdefg" ```
- **Solution:**
<img src="http://i64.tinypic.com/23w4p5e.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **9.- Exercise 18**
Rotate a ** N ** list to the left.
Tip: Use the length of the predefined functions and (++).

- **Example:**

	 ``` (rotate '(a b c d e f g h) 3) ```
	 ``` (D E F G H A B C) ```
	 ``` (rotate '(a b c d e f g h) -2) ```
	 ``` (G H A B C D E F) ```

- **Example in Haskell:**

 	``` *Main> rotate ['a','b','c','d','e','f','g','h'] 3 ```
	 ``` "defghabc" ```
	``` *Main> rotate ['a','b','c','d','e','f','g','h'] (-2) ```
	``` "ghabcdef" ```

- **Solution:**
<img src="http://i64.tinypic.com/23w4p5e.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **10.- Exercise 18**
Remove the K'th element from a list.

- **Example in Prolog:**

	```  ?- remove_at(X,[a,b,c,d],2,R). ```
	``` X = b ```
	``` R = [a,c,d] ```

Prolog also returns the deleted element.

- **Example in Haskell:**

	``` *Main> removeAt 2 "abcd" ```
	``` ('b',"acd") ```
- **Solution:**
<img src="http://i64.tinypic.com/23w4p5e.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **1.- Exercise 21**
Insert an item in a certain position in a list.

- **Example:**

	``` (insert-at 'alfa '(a b c d) 2) ```
	```(A ALFA B C D) ```

- **Example in Haskell:**

	``` P21> insertAt 'X' "abcd" 2 ```
	``` "aXbcd" ```
- **Solution:**
<img src="http://i64.tinypic.com/35lc0ue.jpg" border="0" alt="Image and video hosting by TinyPic">

- - -


### **2.- Exercise 22**
Create a list that contains all integers within a given range.

- **Example:**

	``` (range 4 9) ```
	``` (4 5 6 7 8 9) ```

- **Example in Haskell:**

	``` Prelude> range 4 9 ```
	``` [4,5,6,7,8,9] ```

- **Solution:**
<img src="http://i68.tinypic.com/55pc01.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **3.- Exercise 23**
Extract a given number of randomly selected items from a list.

- **Example:**

	``` (rnd-select '(a b c d e f g h) 3) ```
	``` (E D A) ```

- **Ejemplo en Haskell:**

	``` Prelude System.Random>rnd_select "abcdefgh" 3 >>= putStrLneda ```

- **Solution:**

- - -
### **4.- Exercise 24**
Draw N different random numbers from 1..M.

- **Example:**

	``` (rnd-select 6 49) ```
	``` (23 1 17 33 21 37) ```

- **Example in Haskell:**

	``` Prelude System.Random>diff_select 6 49 ```
	``` Prelude System.Random>[23,1,17,33,21,37] ```

- **Solution:**

- - -
### **5.- Exercise 25**
Generate a random permutation of items in a list.

- **Example:**

	``` (rnd-permu '(a b c d e f)) ```
 	``` (B A D C E F) ```

- **Example in Haskell:*

	``` Prelude System.Random>rnd_permu "abcdef" ```
	``` Prelude System.Random>"badcef" ```

- **Solution:**

- - -
### **6.- Exercise 26**
Generate the combinations of K different objects chosen from the N elements of a list. In how many ways can a committee of 3 be elected from a group of 12 people? We all know that there are C (12.3) = 220 possibilities (C (N, K) denotes the well known binomial coefficients). For pure mathematicians, this result can be great. But we really want to generate all the possibilities in a list.

- **Example:**

    ```(combinations 3 '(a b c d e f)) ```
	``` ((A B C) (A B D) (A B E) ... ) ```

- **Example in Haskell:**

	``` > combinations 3 "abcdef" ```
	``` ["abc","abd","abe",...] ```

- **Solution:**

- - -
### **2.- Exercise 31**
Determine if a given integer is prime.

- **Example:**

	 ``` (is-prime 7) ```
	 ``` T ```

- **Example in Haskell:**

	``` P31> isPrime 7 ```
	``` True ```

- **Solution:**
<img src="http://i66.tinypic.com/9jfa4k.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **3.- Exercise 32**
Determine the greatest common divisor of two positive integers. Use Euclid's algorithm.

- **Example:**

	``` (gcd 36 63) ```
	``` 9 ```

- **Example in Haskell:**

	``` [myGCD 36 63, myGCD (-3) (-6), myGCD (-3) 6] ```
	``` [9,3,3] ```

- **Solution:**
<img src="http://i66.tinypic.com/bg8xux.jpg" border="0" alt="Image and video hosting by TinyPic">

- - -


### **4.- Exercise 33**
Determine if two positive integers are coprime. Two numbers are coprime if their greatest common divisor is equal to 1.

- **Example:**

 ``` (coprime 35 64) ```
	``` T ```

- **Example in Haskell:**

	``` coprime 35 64 ```
    ``` True ```

- **Solution:**
<img src="http://i66.tinypic.com/2upbfiq.jpg" border="0" alt="Image and video hosting by TinyPic">

- - -


### **6.- Exercise 36**
Determine the prime factors of a given positive integer. Construct a list that contains the prime factors and their multiplicity.

- **Example:**

	``` (prime-factors-mult 315) ```
	``` ((3 2) (5 1) (7 1)) ```

- **Example in Haskell:**

	``` *Main> prime_factors_mult 315 ```
	``` [(3,2),(5,1),(7,1)] ```

- **Solution:**
<img src="http://i65.tinypic.com/oibo5f.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **9.- Exercise 39**
(*) A list of prime numbers.
Given a range of integers by their lower and upper boundaries, construct a list of all prime numbers in that range.

- **Example in Haskell:**

	 ``` P29> primesR 10 20 ```
	``` [11,13,17,19] ```

- **Solution:**
<img src="http://i67.tinypic.com/f0p5yh.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **10.- Exercise 40**
Goldbach Conjecture.

Goldbach's conjecture says that each positive number equal to greater than 2 is the sum of two prime numbers. Example: 28 = 5 + 23. It is one of the most famous facts in numerical theory that has not been proven to be correct in the general case. It has been confirmed numerically up to very large numbers (much larger than we can go with our Prolog system). Write a predicate to find the two prime numbers that add an even integer.

- **Example:**

	``` (goldbach 28) ```
	``` (5 23) ```

- **Example in Haskell:**

	 ``` goldbach 28 ```
	``` (5, 23) ```

- **Solution:**
<img src="http://i68.tinypic.com/3599yth.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **11.- Exercise 41**
Given a range of integers by its lower and upper bound, print a list of all even numbers and their composition of Goldbach. In most cases, if an even number is written as the sum of two prime numbers, one of them is very small. Very rarely, cousins are larger than 50. Try to find out how many such cases there are in the 2..3000 range.

- **Example:**

	``` (goldbach-list 9 20) ```
	 ```  10 = 3 + 7 ```
	```   12 = 5 + 7 ```
```	  14 = 3 + 11 ```
	 ```  16 = 3 + 13 ```
 ```	  18 = 5 + 13 ```
```	  20 = 3 + 17 ```
	```  * (goldbach-list 1 2000 50)```
	```  992 = 73 + 919 ```
```	  1382 = 61 + 1321 ```
	```  1856 = 67 + 1789 ```
```	  1928 = 61 + 1867 ```

- **Example in Haskell:**

	 ``` *Exercises> goldbachList 9 20 ```
	 ``` [(3,7),(5,7),(3,11),(3,13),(5,13),(3,17)] ```
	 ``` *Exercises> goldbachList' 4 2000 50 ```
	``` [(73,919),(61,1321),(67,1789),(61,1867)] ```


- **Solution:**
<img src="http://i63.tinypic.com/2re1mq9.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **2.- Exercise 46**
Defines predicates and / 2, or / 2, nand / 2, ni / 2, xor / 2, impl / 2 and eq / 2 (for logical equivalence) that succeed or fail according to the result of their respective operations; Eg Y (A, B) will succeed, if and only if both A and B are successful.

A logical expression in two variables can be written as in the following example: y (or (A, B), nand (A, B)).

Now, write a table of predicates / 3 that prints the truth table of a given logical expression into two variables.

- **Example:**

     ``` (table A B (and A (or A B))) ```
	``` true true true ```
	``` true fail true ```
	``` fail true fail ```
	``` fail fail fail ```

- **Example in Haskell:**

	``` > table (\a b -> (and' a (or' a b))) ```
	``` True True True ```
	``` True False True ```
	 ```False True False ```
	``` False False False ```

- **Solution:**
<img src="http://i68.tinypic.com/29qoade.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **3.- Exercise 47**
Tables of truths for logical expressions (2).
Continue problem P46 by defining y / 2, or / 2, etc. as operators. This allows to write the logical expression in the most natural way, as in the example: A y (A or not B). Define the precedence of the operator as usual; As in Java.

- **Example:**

	 ``` (table A B (A and (A or not B))) ```
 	  ``` true true true ```
	 ``` true fail true ```
	 ``` fail true fail ```
	  ``` fail fail fail ```

- **Example in Haskell:**

	``` > table2 (\a b -> a `and'` (a `or'` not b)) ```
	``` True True True ```
	``` True False True ```
	``` False True False ```
	``` False False False ```


- **Solution:**
<img src="http://i64.tinypic.com/ja88b9.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **4.- Exercise 48**
Tables of truths for logical expressions (3).

Generalize problem P47 such that the logical expression can contain any number of logical variables. Define table / 2 in a way that table (List, Expr) prints the truth table for the Expr expression, which contains the logical variables listed in List.

- **Example:**

	``` (table (A,B,C) (A and (B or C) equ A and B or A and C)) ```
	```  true true true true ```
	 ``` true true fail true ```
	 ```  true fail true true ```
	 ```  true fail fail true ```
	```   fail true true true ```
	 ``` fail true fail true ```
	```  fail fail true true ```
	 ``` fail fail fail true ```

- **Examle in haskell:**

	 ``` > tablen 3 (\[a,b,c] -> a `and'` (b `or'` c) `equ'` a `and'` b `or'` a `and'` c) ```
	``` -- infixl 3 `equ'` ```
	``` True  True  True  True ```
	``` True  True  False True ```
	``` True  False True  True ```
	``` True  False False True ```
``` 	False True  True  True ```
```	False True  False True ```
	``` False False True  True ```
	``` False False False True ```

	``` -- infixl 7 `equ'` ```
	``` True  True  True  True ```
```	True  True  False True ```
```	True  False True  True ```
	``` True  False False False ```
	 ``` False True  True  False ```
	``` False True  False False ```
	``` False False True  False ```
	``` False False False False ```

- **Solution:**
<img src="http://i64.tinypic.com/29mr33m.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **5.- Exercise 49**
Gray codes.

An n-bit gray code is a sequence of n-bit strings constructed according to certain rules. For example,

 ``` N = 1: C (1) = ['0', '1']. ```
``` N = 2: C (2) = ['00', '01', '11', '10']. ```
``` N = 3: C (3) = ['000', '001', '011', '010', '110 ', '111', '101 ', '100']. ```

Find the construction rules and write a predicate with the following specification:

% Gray (N, C): - C is the N-bit Gray code

Can you apply the "result cache" method to make the predicate
More efficient, when it will be used repeatedly?

- **Example in Haskell:**

   ``` P49> gray 3 ```
	``` ["000","001","011","010","110","111","101","100"] ```

- **Solution:**
<img src="http://i67.tinypic.com/2sbo104.png" border="0" alt="Image and video hosting by TinyPic">

- - -


### **6.- Exercise 50**
Huffman Codes.

We assume a set of symbols with their frequencies, given as a list of Terms fr (S, F). Example: [fr (a, 45), fr (b, 13), fr (c, 12), fr (d, 16), Fr (e, 9), fr (f, 5)]. Our goal is to build a list hc (S, C) Terms, where C is the Huffman codeword for the S symbol. In our example, the result could be Hs = [hc (a, '0'), hc (b, '101'), Hc (c, '100'), hc (d, '111'), hc (e, '1101'), ... etc.]. The task will be performed by the huffman / 2 predicate defined as follows:

% Huffman (Fs, Hs): - Hs
It is the Huffman code table for the frequency table Fs.

**Example in Haskell:**
	``` *Exercises> huffman [('a',45),('b',13),('c',12),('d',16),('e',9),('f',5)]
	[('a',"0"),('b',"101"),('c',"100"),('d',"111"),('e',"1101"),('f',"1100")] ```

- **Solution:**
<img src="http://i63.tinypic.com/2edbig4.png" border="0" alt="Image and video hosting by TinyPic">

- - -

# INSTITUTO TECNOLOGICO DE MEXICALI