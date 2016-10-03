#Puts and Gets
*You know, if you say puts and gets fast enough, it'll sound like you're beatboxing*		

In order to build an interactive command line program, you'll need a way to take in information from your user. Ruby makes this very easy by using **`puts` and `gets`**.

## `puts`
`puts` is a method that works very much like `print`. We have used it in previous labs as it helps to present things to a user through the terminal. We use `puts` because it adds a new line after whatever it prints, unlike `print`. This makes whatever you're presenting to the user much easier to read.

	puts "Hello world!"
	puts "It's a beautiful day"
		>> "Hello world!"
		>> "It's a beautiful day"

If we used print here, it would look slightly different:

	print "Hello world!"
	print "It's a beautiful day"
		>> "Hello world!It's a beautiful day"

Not as nice on the eyes.

## `gets`

While `puts` presents information to the user, `gets` retrieves information. Say we wanted to learn our user's favorite food.

	puts "What is your favorite food?"
	food = gets

Whatever our user types will be saved in the variable `food`. This is great! Now we have a way of retrieving and saving our user data to a variable.

Unfortunately, Ruby adds a new line to the end of the user input. 		
Let's say our user types in `"pizza"`, which means `food = "pizza"`. Now let's use this variable in a sentence using interpolation.

	print "Your favorite food is #{food}? So is mine!"
		>>Your favorite food is pizza
			? So is mine!

Ruby automatically added a new line after our variable, which is tough when we want to use it in a long sentence. However, we can chain on the `.chomp` method to remove the newline character at the end of the string. `gets.chomp` will take the user input, and then cut off the new line at the end.

	puts "What is your favorite food?"
	food = gets.chomp
	print "Your favorite food is #{food}? So is mine!"

If our user types "pizza" again, this time we'll print

	>>Your favorite food is pizza? So is mine!

Muuuuch better.   


In this lab, you'll create a basic chatbot of your own! Follow the instructions in the comments.
