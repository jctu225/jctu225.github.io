Using a For Loop

	Something that plagued me that I only discovered how to do over this recent weekend was use a for loop. Some how the iterative process of a for loop eluded me. I’m going to try and explain every part of it, give examples, and explain it rather directly to try and help you understand for loops.

	Example of the loop:
			for (var i=0;i<x;i++){
				//Code
			}

	I would like to make an observation before explaining it: The for loop would make more sense (at least for new programmers) if the loop were written slightly differently. Instead of the above example if it read as follows for(i<x;i=0;i++) in ‘plain english’ this would read “For when i is less than x, on the first loop set i=0, then for every subsequent loop add one to i. If is ever greater than x, stop running.” However the real for loop places i<x in the second position instead of the first.

	As for each of the variables. i=0 the variable can be anything, and technically you could use any number or string in place of the zero, but what the zero is is determined wholly by what you need the for loop to do. Maybe you are actually looping through a string instead of a variable using charCodeAt() and fromCharCode(), or perhaps for some reason you need i to be set equal to 5 for  certain function of mathematics. i<x by technicality any variable can be placed in the spot of x and i, and the less than sign can be many more things !=, >, <=, >=, === each has its own value in the loop. Maybe when i is equal (===) to x you need the loop to stop, or maybe only if it is not equal (!=)  you need the loop to run until it is equal. i++ this variable could be removed from the loop entirely and the for loop will still run! It loses its iterative power though. You could do many things with this (+=, -=, –, *=, /=) in effect each of these do something different i += 3. i will instead iterate by 3. Similarly -= will cause I to decrease by a given number (i -= 3) and i-- will decrease i by one for each loop the for loops goes through. For review I will explain what each of the above symbols mean, intentionally taking them out of the context of a for loop so you can get an idea of what the symbol does in the greater context:

!= means Not Equals
if (x != y){
	//code
}
//executes if x isn’t equal to y

=== means Equals to.
if (x === y){
 	//code
}
//executes if x is equal to y

> Greater than.
if (x>y){
	//code
}
//executes if x is greater than y



< Less than.
if(x<y){
	//code
}
//executes if x is less than y

<= Less than or equals to.
if(x<=y){
	//code
}
//executes if x is less than or equal to y

>= Less than or equals to
if(x>=y){
	//code
}
//executes if x is less than or equal to y

+= Add the number on the left, to the number on the right and set the number on the left to the new number.
x += 4;
//x will have 4 added to it

-= Subtract the number on the left from the number on the right and set the number on the left to the new number.
x -= 4;
//x will have 4 subtracted from it

*= Multiply the number on the left by the number on the right and set the number on the left to the new number.
x *= 4;
//x will be multiplied by 4

/= Divide the number on the left by the number on the right and set the number on the left to the new number.
x /= 4;
//x will be divided by 4

x- - iterate i by -1.
for (var x=10;x>4;x--){
	//code
}
//x will decrease by 1 for each loop (until it is less than 4, or presumably 3 in this case)

x++
for (var x=0;x>4;x++){
	//code
}
//x will increase by 1 for each loop (and presumably run until it reaches the number 5)

I will show a few simple examples and explain what they do: 
			
			var  k=100
			for(var x=25; x>5; x--){
				k += 6
			}

	In this example x will decrease 20 times, while increasing k by 6. This will result in 266. If we were to say this in English it would sound like the following: 100 + (6*21) = 266.

			var amazing = 1;
			for(var y=0; y<5;y++)
				amazing = amazing * y;			
			}

The above for loop is equivalent to:

			var amazing = 1;
			for(var y=0;y<=5;y++){
				amazing *= y;
			}
	In the above two examples these will multiply the number amazing by y and set amazing equal to the result of that. As y increases the for loop will multiply y by higher and higher numbers.  The result of this will be 24. This equation would look like the following in english: 5! = 120. Factorials with a for loop! (The factorial in this case is y<=5, where 5 is the factorial!)



	There are many incredibly powerful benefits to such a loop. You can count through an number of objects, or have the loop run a specified number of times if the same number of times is always required. It can easily turn word problems into math problems.