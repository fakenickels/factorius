## JavaScript

```javascript

	// Non-recursive
	function factorial( number ){
		var final = 1;
		for( var i = 1; i <= number; i++ ){
			final *= i;
		}

		return final;
	}

	// Recursive
	function factorial( number ){
		return number === 1 ? 1 : number * factorial( number - 1 );
	}

	// Recursive using a auxiliar var
	function factorial(number, f){
		return number === 1 ? f : factorial( number - 1, number * f );
	}

	// Recursive using continuation
	// inspired in http://lambda-the-ultimate.org/node/643 and @robotlolita
	function factorial(number, final, cc){
		n === 1? cc(final) : factorial(number - 1, final * number, cc)
	}
```

## Ruby
```ruby
	# Non-recursive
	def factorial( number )
		final = 1

		number.downto(1) {|i| 
			final *= i
		}

		final
	end

	# Recursive
	def factorial( number )
		number == 1 ? 1 : number * factorial( number - 1 )
	end
```