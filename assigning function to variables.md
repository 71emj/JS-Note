# The difference between: 
<b>var myVariable = Myfunction;</b><br>
<b><em>v.s.</em></b><br>
<b>var myVariable = Myfunction();</b>

<br>

<strong><em>For example: </em></strong> 
<pre>
	function Myfunction() {
		// do somerandom stuff
		var x = 10;
		return x;
	}	

	var unRelated_X = Myfunction();

	console.log(unRelated_X); // x
</pre><br>

What javascript did on the example above is assigning the value of x inside the function to a variable unRelated_X, to simplify the process the snippets is doing something like this: 

<br>
<pre>
	var unRelated_X = x;
	// assigning the <em>return </em>value of the function is the same as assigning a literal value to a variable.
</pre> 

<br>

#In JS function call is follow by a parenthesis: Myfunction();

<em>by simply calling a function name without a parenthesis: Myfunction;</em><br>
<em>it's the same as calling a variable in an empty place: myVariable;</em><br>

<strong>without a parenthesis, <em><b>Myfunction is just another variable holding the functionality you defined in a function declaration</b></em></strong>
<br>

#So, var myVariable = Myfunction; is actually assigning the Myfunction to myVariable
<br>

#same with function expression// var MyAnotherfunction = function() { ... };

<br><strong>So to sum up: </strong><br>

<em>var Variable_1 = "some value";</em> is the same as: <br>
<pre>
	function AnotherFunction() { return "some value"; }

	var Variable_2 = AnotherFunction(); 
	
	console.log(Variable_1); // "some variable"
	consoel.log(Variable_2); // "some variable"
</pre>

<br>both the variables will return the same value in the console

<br>however:
<pre>
	var Variable_3 = AnotherFunction;

	console.log(Variable_3); // function() { ... }
</pre> <br>

Variable_3 is assigned with the function <em>AnotherFunction</em>, instead of the value return by the function.<br>

so if we console.log( <b>Variable_3()</b> ) it will return the same result as we console.log( <b>AnotherFunction()</b> ) <br>
<pre>
	console.log(Variable_3); // function() { ... }
	console.log(AnotherFunction); // function() { ... }
	
	console.log( Variable_3() ) // "some variable"
	console.log( AnotherFunction() ) // "some variable"
</pre>



