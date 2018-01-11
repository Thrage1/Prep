# Pry

#### Part one: intro to pry

To install Pry on your computer you would from the terminal type
pry-doc allows access to ruby's core methods
if you need to be an administrator then sudo goes in front of the installation. --no-ri and --no-rdoc are tags that can be added to the end of the line and it specifies not to install the documentation.

```
gem install pry pry-doc
```

in order to use pry all you need to do is type
```
pry
```
in the terminal

- a repl stands for read evaluate print and loop
the code is essentially

```
loop { p eval gets }
```

- irb is a repl that comes with ruby but it doesn't have the features that pry comes with.
- toggle-color is the command in pry which toggles the syntax highlighting.
- commands that give access to pry's functionality by typing help in the pry repl
- adding the -h tag to the end of a command gives specific information about the command itself
- show-doc is a method that shows the documentation about about method you are interested in

```
show-doc 'hi'.upcase
```
this shows the documentation about the upcase method when used on strings

- using show-method instead shows the method in C. Also using the -l flag will add line numbers to the code.
- using the gist method creates a shareable snippit of the code online. Example:

```
gist String#upcase
# or
a = 'apple'
gist a.upcase
```

- in pry you can also cd into and out of objects for example cd Array changes the prompt to array and allows you to use methods without typing Array.methods
- in the following case

```
pry
cd String
ls
# lists all the methods
ls -M
# lists all the instance methods
ls -m
#lists all of the class methods
```

- when using pry you can see what you wrote in the middle of a method with show-input
- and after that you will be using the amend-line #line number #what you want to change the line to
#### Using pry as a debugger

- require 'byebug' at the top of the file that you want to use
- when you are working in pry you can use the command list= to get back to the point the code is paused
