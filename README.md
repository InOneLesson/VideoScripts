# In One Lesson - Video Scripts

> [!NOTE]  
> Click the [Discussions](https://github.com/In-One-Lesson/VideoScripts/discussions) tab above to provide feedback or ideas on the scripts below.

Below are scripts for about 50 videos. The scripts are in order from basic to more advanced. Not sure if this will be one long video or if each script will be its own video (or both?).

Each video starts with the working title followed by a setup of the video that may explain the reasoning behind the video or an explanation of the visuals, followed by the script.

# Bits are Not On the Wire, they Are the Wire

This was by far my biggest misconception when learning how computers work. I thought bits were discrete little pulses of energy that traveled down a wire. I didn't realize that a bit exists everywhere on a wire at once and that that fact was pivotal to how computers worked.



* You've probably seen videos like this where bits move down a wire like cars on a road.
* That's not how bits works.
* The bit is the state of the whole wire, not something traveling down the wire.
* When the wire has a bit value of 1, that means the entire wire has an electric field present on it.
* When there are less electrons in the wire than protons, the electric field that is produced is considered positive.
* A positive electric field attracts negatively charged electrons
* When this wire is near a semiconductor, its electric field attracts electrons to the surface of the semiconductor.
* Those electrons collect at the top and turn that area of the semiconductor into a conductor
* That conducting channel allows a current of electrons to flow through another wire connected to the semiconductor
* If the wire above the semiconductor loses its electric field, then the electrons in the semiconductor are no longer attracted to its surface and the current through the other wire stops
* This setup, where the electric field of one wire causes the current of electrons to start or stop in a nearby wire via a semiconductor, is called a transistor
* The wire above the semiconductor may be long and be above other semiconductors as well, allowing it to control the current through more than one transistor at a time
* That's how a bus works.
* A bus allows a set of components to use a common set of wires to control electric flow in each other.
* The currents on these wires usually represent data meaning one component can send bits of data to several other components at the same time.
* An 8-wire bus, for instance, can make 8 bits of information, or 1 byte, available to every component simultaneously
* However just because every component has access to that byte doesn't mean they all use it
* Each component also has some control wires, separate from the bus, that control whether or not that component uses the bits on the bus
* The CPUs control unit sends those control signals to the component at different points in the instruction cycle depending upon what instruction its processing.
* So even though all the components attached to the bus receive that same byte, they don't actually do anything with it until the control unit tells them to.
* This setup would not be possible if a bit traveled down wires like a car on a road since that car can only be in one place at a time.
* The design of the CPU inherently relies on the simultaneous presence of a bit in multiple places at once to work.

# Thinking Outside the Wire

It's so odd to think of an electrified wire as having a value on it, like a number or a Boolean. However, due to the clever design of CPUs, they can be treated as number crunchers even though they're simply a collection of wires and transistors. I think it's important for beginners to separate the idea of bits from electrified wires so they know that we're all just pretending that the computers have 1s and 0s in them somewhere when in reality it's just a useful analogy designed into the hardware.

* An electrified wire can be thought of as a number like 1, or a logical value like true, or either side of any other binary concept
* When one electrified wire controls another electrified wire in a transistor, the value it represents can also be copied to that other wire
* These input and output wires of the transistors can then be grouped in such a way that seem to mimic an arithmetic or logical operation
* For instance, if you convert some numbers you want to add together into their binary forms and then arrange some transistors in a certain way, then you can electrify the input wires in the same pattern as your binary numbers and then see the answer in binary form on the output wires
* Transistors can be arranged in a countless number of ways so with enough time and testing, you can get a group of them to mimic all kinds of useful real-world operations
* The different arrangements of these transistors allows hardware designers to treat electrified wires as though they represent certain types of values depending upon how they arranged the transistors
* In one area of a CPU, for instance, the transistors may be arranged to mimic operations on numbers while in another they may be arranged to mimic logical operations on true/false values
* By designing these components in this way, the electrified wires that are used for their inputs and the electrified wires that are used for their outputs can be treated as though they actually have numbers on them, or other types of values
* If you treat something as though it were something else and it behaves exactly like you would expect that other thing to behave, then you can almost ignore reality and just see what you want to see
* Since each of these components has been designed to produce a result consistent with how it is treated, the designer and therefore the user can begin thinking about these components at a higher level than just their wires and transistors.

# Bits are a universal concept

We all think of computers as having a bunch of 1s and 0s in them even when each component inside may be very different from the others. So how do we maintain consistency across these components at the most basic level?

* More often than not, electrified wires in a computer are treated as numbers - 1s and 0s, binary digits, or bits for short
* This is not because all the data in a computer is always numeric
* Numbers are just a more useful metaphor to use than other binary concepts and having one primary metaphor for electrified wires proves quite useful
* Once you have a primary binary metaphor you can then map it onto other things besides electrified wires.
* For example, other components besides wires can be treated as though they can only be in one of two states, such as magnets
* Wrapping a magnet with a wire and sending electricity through it in one direction will cause the magnet to become polarized in one orientation
* Reverse the direction of the flow of electricity through the wire and you reverse the polarization of the magnet as well, the North Pole becomes the South Pole and vice versa.
* This means magnets can take on one of two states just like electrified wires, so how do you think of these two states of the magnet as compared with the wire.
* At some point, you've got to decide which polarization of the magnet is going to be treated the same as the electrified wire.
* Since we have a common binary metaphor, bits, we can just decide which polarization is the 1 and which is the 0 and then design the hardware around that magnet accordingly.
* All the components inside a computer must each have a predefined state that maps to a binary 1 and another that maps to a binary 0.
* And then when those components are connected together, they can all maintain the illusion that a certain number, like 1, is inside the computer even when it is copied from one component to another and back again.
* This universal mapping of the concept of a bit onto more than one type of physical component allows more complex hardware devices to be conceived an interconnected
* A bit value, like a 1, can now be thought of as something above and beyond the hardware that represents it
* This 1 can be thought of as moving from a wire and being stored in a magnet and then moving back on to the wire when it is retrieved
* However this 1 doesn't actually exist anywhere.
* The hardware was just designed to maintain the illusion that there's something actually moving around inside the computer when in reality there's nothing actually moving in the computer
* In fact the best analogy for data transport is not moving at all

# Computers copy data, they don't move it

I didn't realize for a long time that I had a fundamental misunderstanding of computers that hindered my learning and progress. People generally refer to data as moving around in the computer. That seems right until you start to apply that analogy to other things you're learning. Then you can get tripped up really bad without knowing why.

* Moving something and copying something are two very different paradigms with very different rules.
* If you move something, it is no longer in its original location.
* If you copy something, it can exist in multiple places at the same time.
* Information in a computer is copied, not moved.
* The source of that information, such as RAM, and multiple destinations, such as tiny memory devices in the CPU called registers, can all have access to that information at the same time.
* This makes it possible to select the intended destination for the information after it has been sent.
* The recipient could be asked to remember the information and the others could simply ignore it.
* That is how a bus works inside a computer.
* The bus is just a group of wires that are connected to multiple components.
* Each component can read the value on the bus but will only remember it when a separate control wire is electrified.
* The control unit in the CPU sends these signals to each component based on the instruction it fetched from RAM.
* If data were truly moving on the bus, then it could not exist in multiple places at the same time and the concept of the bus would not work.
* Since the electric field of a wire exists on every part of the wire at once, the bit value represented by that electric field also exists in multiple places at once.

# How the ALU Works

The ALU is used for nearly every operation in the CPU. It's important to get a basic understanding of what it is and how it works early on.

* Any electrified wire can be treated as though it has a 1 on it, or a true value, or sometimes both at the same time.
* The more cleverly designed components may be able to switch back and forth between how their wires are treated
* For instance, one of the most important components in a CPU can treat its input wires as having numbers on them or logical values depending upon what operation needs to be performed at that moment
* This component is called the Arithmetic Logic Unit and it does exactly that: arithmetical and logical operations
* For instance very simple components called logic gates arrange transistors in such a way that they mimic basic logical operations.
* An "and" logic gate, for instance, tells you if both it's first and second input wires are on because the transistors are arranged so that the output wire turns on when that is true
* "Not" logic gates have a single input wire and use transistors to change the output wire to be the opposite state of that input wire.
* And gates and not gates can then be combined into nand gates that are used to build every other type of component in the CPU including ones that mimic arithmetic
* An adder component uses logic gates to mimic binary arithmetic by arranging those logic gates such that two groups of input wires are connected to one group of output wires in such a way that the component seems to be performing addition on the input wires
* A subtraction component can also be created that is also used as a logical component that compares numbers since if the result of a subtraction is 0, then those two numbers must be the same.
* The ALU which houses these arithmetic and logical components also has control wires connected to it that tell it which operation to perform on its input wires at any one moment
* Other parts of the CPU send these control singles to the ALU along with the inputs to the ALU using the bus connected to it.
* The output of the ALU is then copied to other components using the bus as well.
* The ALU can be used over and over again to perform different types of operations depending upon the design of the program being run by the CPU

# A Program is a To-Do List

Programming truly is just writing a to-do list for computers to follow. This video introduces that idea.



* Computer memory is just like a numbered todo list where the numbers are written in pen but the items are written in pencil and can change.
* This todo list is a little unique, though.
* The todo items are tiny and can only hold 8 characters.
* The list is huge, though, so the item numbers can be very large and use way more than 8 digits.
* You fill out this to-do list and give it to the computer.
* The computer works your todo list starting at the top and then keeps going down item by item.
* Normally it does everything in order, but it can also jump out of order if you tell it.
* You can also add information to your list, not just todos.
* Like if you have a math todo item like "add two numbers", the computer needs to know what those two numbers are.
* You can put them in the list right before that todo item so the computer has them saved when it's ready to add them.
* If you want the computer to start working your list out of order, just tell it which todo item number comes next and it will start working your list from that point on.
* You can also tell the computer to check something first before it gets out of order, just to make sure that other set of todo items is needed.
* You can write anything you want on your list, but the computer only understands certain instructions.
* So you have to know what instructions your computer understands if you want it to do something useful for you.

# How Different Numbers Are the Same Count

How can "10" and "10" mean two different things? They are the same number. However, when you understand that there is an even more fundamental concept that numbers, a count, then you can understand that two numbers that look the same can represent different counts depending upon what numbering system is used.



* RAM stores data as binary numbers.
* Binary numbers are just like regular decimal numbers except they can only use two characters for each digit instead of ten.
* The counting system still works the same though.
* You start counting in the right column, move up your column index one character at a time until you reach the top.
* If the index is already at the top, you drop it back down to the bottom and then move the index in the next column up by one.
* This process continues over and over as you count up.
* Multiple columns can cascade back to zero if the indexes in those columns are already at the top.
* Because binary numbers use the same characters in each column as decimal numbers, they can both look exactly the same, even when they represent a different count.
* For this reason, numbers are often accompanied by a tiny number that tells you how many characters the columns have.
* Base 10 means that number was based on having 10 characters in each column and base 2 means that number was based on having 2 characters in each column.

# Computer Memory Has Two Lists of Numbers, Not One

This was a misconception I had for many years, I thought RAM only had data. I didn't realize each byte of data had an address, another binary number. Knowing about addresses is pivotal to knowing about pointers and how computers work in general.



* RAM stores data at specific addresses.
* That data and its address are each binary numbers.
* The binary number for the data always uses 8 bits.
* A binary number that uses 8 bits is called a byte.
* The value of the data byte can change but the value of its corresponding address cannot.
* A computer can store a lot of bytes in RAM.
* Many computers use 64 bits for each RAM address.
* Even in binary, you can count to a very high number when you have 64 digits available.
* Each of these addresses correspond to 1 data byte which means you can store a huge number of bytes in RAM.
* Even though each byte can only hold a small amount of data, there are so many bytes that it doesn't really matter.

# "Byte" Doesn't Always Mean What You Think

I didn't realize that I had been conflating these two things until recently. When someone says "byte", sometimes they mean the value of the binary number regardless of its location in RAM and sometimes they mean the location of the binary number in RAM regardless of its value. Separating these two senses of the word early for beginners who are learning programming would be very helpful to them I think.



* The term "byte" may refer to two different but related things: a value stored in RAM regardless of its location or a location in RAM regardless of its value.
* For instance, the decimal number 53 can be stored in a byte.
* We might not care where that byte is, only what its value is.
* In that sense the term byte refers just to the value.
* Or we may only care about a byte based on its location, not its value.
* For instance, there is a byte in RAM that holds the first instruction run by the computer when it starts up.
* "Byte" in that sense means a specific address in RAM, not the specific value at that address.
* These two ways of thinking about bytes, as a value or as a location, each have their own uses when programming.

# How Programs Work From Anywhere

This is an interesting one for me. Since bytes in RAM are addressed using numbers, it makes relative addressing possible. Relative addressing is critical to loading programs into memory, indexing into arrays, and all kinds of other techniques in programming. They would not be possible if something like numbers weren't used to address bytes in RAM since numbers have the concept of "next" and "previous".



* Not only do RAM addresses never change, they are always in order, starting at address 0 and increasing by one.
* This allows programmers to always be able to refer to an address relative to any other address, the 3rd address after the starting address, for instance.
* That starting address may end up being different each time a program is loaded into RAM and run, but it doesn't matter because the instructions and data for that program are always at the same location in RAM relative to the starting address.
* Since numbers have an inherent sequence to them, using numbers as the addresses in RAM gives programmers the ability to perform relative addressing like this, not just absolute addressing like web addresses.

# RAM Addresses Start at 0

This is not as big of a deal, but still interesting enough to include I think. There were a lot of times early on when I was learning programming where it confused me that the 3rd item in a list has a "2" for its index. Off-by-one errors in programming are common because of this concept which is why I wanted to teach it early.



* RAM addresses start at 0 which means the first address in RAM is 0, not 1.
* This makes all RAM addresses off by 1, often including relative addresses.
* If you have a list of items in a section of RAM, the first item in that list is often considered to have relative RAM address 0, relative to the start of that list.
* This can be difficult to get used to as a programmer because it means you're always having to translate the item number of the list to the relative address number.
* The third item has relative address 2, for instance.
* This is much like how your age works, though.
* Your first year of life, you were 0 years old.
* Your first birthday actually started your second year of life.
* Clocks work the same way.
* The second hour of the day is 1 AM.
* Addresses in RAM are no different.

# Why Hexadecimal is Useful For Coders

Rarely do you look at raw data in RAM using anything other than hexadecimal values. That tends to lead people to think that hexadecimal values are somehow pivotal to the way computers work. They're not. They just represent the 1s and 0s of computing in a more compact way, which is why they're used so often. However, it's important to understand that the computer doesn't actually use hexadecimal values in any way. They're just a way to represent binary values in a more programmer-friendly way.



* Binary numbers are often converted into decimal or even hexadecimal notation to make them easier to read.
* Hex means 6 and deci means 10 so added together that's 16 characters that can be used in each column.
* The extra 6 characters used in hexadecimal above and beyond the normal decimal numbers, are actually letters.
* It can get confusing seeing a letter represent a number but ultimately it is quite useful.
* Why? Well a byte split down the middle gives you two 4-bit segments.
* Each 4-bit segment has 16 possible values so you could use two hexadecimal digits to represent a byte instead of eight binary digits.
* Hexadecimal numbers allow you to represent the same count using fewer characters than binary.
* You'll often see this notation used in so-called hex editors which allow you to view the raw bytes in a text file, for instance.

# Text Files Don't Use Letters

This is one of the biggest lessons I would have wanted to know early on. How do text files actually store text?



* Programs are written in text files.
* When you open up a text file, each letter you see on the screen is represented by a specific pattern of colored pixels created from a font file somewhere.
* Neither the pixel pattern nor the font is encoded in the text file, though.
* Instead the bytes in the text file represent abstract concepts.
* Each concept is assigned a number by Unicode and the byte in the text file just represents that number.
* The byte used for lowercase letter "r" does not tell the computer how to draw an "r".
* It simply refers to an abstract concept that is also called "lowercase letter r."
* A font file somewhere then tells the computer how to display that concept on the screen.

# In Computers, Every Letter is a Number and Every Number is a Number

Unicode is such an interesting system. You use numbers to represent raw concepts. Those numbers can then have another layer of abstraction between the number itself and its binary representation in RAM using UTF. This is a great example of the "[fundamental theorem of software engineering](https://www.google.com/url?q=https://en.wikipedia.org/wiki/Fundamental_theorem_of_software_engineering&sa=D&source=editors&ust=1705519967335439&usg=AOvVaw0-FeoJmXUnBx-Np46K7AZ1)" where adding another layer of indirection can solve a problem in programming.



* Unicode is a list of numbers called code points where each code point represents a specific concept.
* That concept can also be represented by words like "lowercase letter 'r'".
* The code points are numbers but those numbers aren't always directly encoded in bytes as regular binary numbers.
* There are over a million possible code points in Unicode so that would mean every character would need at least 3 bytes to represent it.
* This is where Unicode Transformation Formats come into play.
* You've probably heard of UTF-8 which is a variable-length system that can use as little as 1-byte (or 8-bits, thus the "8" in the name) to represent all the code point numbers for American text characters.
* This saves space in the text file if you are using American text characters.
* If you're using characters from other languages, you'll need two, three or four bytes to encode them.
* The trick is that if the first bit in a byte, the bit on the left, is a 1, the computer knows it's not an American text character and is a part of a multi-byte group used to represent a different type of character.
* UTF-16 is similar to UTF-8 but it uses a minimum of two bytes to represent code points and can use 4 bytes when necessary.
* UTF-32 is fixed length and is exactly equal to the code point's numerical value.
* However, the first byte in UTF-32 is always full of 0s since you only need 3 bytes to represent around 1 million possible values.

# Why Bytes Travel in Packs

This is an important concept to understand I think. You can't represent a value using anything smaller than a byte (even true/false - unless you've packed multiple true/false values into one byte: often called "flags") and usually you have to move multiple bytes at the same time due to hardware constraints.



* Bytes are copied from place to place in groups of the same size to speed things up, even if there are more bytes in that group than is needed to store your data.
* On older 32-bit computers, the CPU copied data from RAM in 32-bit chunks, or 4 bytes at a time.
* Your data, though, may only need three bytes to represent it and not 4.
* Instead of squeezing in some extra data from somewhere else into that remaining byte, your data is just padded with some meaningless bits at the end to keep it aligned to the hardware.
* This seems less efficient but it speeds things up because it prevents any extra data elements from having to be constantly split out and processed separately.
* Aligning the data to the hardware keeps things clean and organized.
* This technique extends all the way out to hard drive data that is stored in large chunks called pages, usually 4,096 bytes in size.
* The data in a running program is split into sections that are aligned according to these pages so they can easily be swapped in and out to the hard drive if RAM fills up.

# Why Computers Use Horizontal Numbers

This is often called little-endian and big-endian, but those name seemed so confusing to me when I first started. I think just explaining them for what they are would have been so much more helpful.



* A number grows from right to left, but conceptually the data in RAM grows from top to bottom.
* So when storing a large number in RAM, which end do you put in RAM first?
* The little end of the number is the one with the little numbers like 10.
* The big end of the number is the one with the big numbers like 4 billion.
* If you are using a little-end computer, the little part of the number is stored first.
* If you are using a big-end computer then the big part of the number is stored first.
* Intel CPUs are little-end so they store the little end of the number first.
* Since you add up numbers starting with the little end of the number first moving toward the bigger end, little end computers can make arithmetic operations a little more efficient since the first bytes in RAM are the first that need to be processed.

# Code Does Not Run on Computers

The phrase "run the code" makes people think that the code they type into a text editor can eventually just run directly on the CPU. I don't think it's always clear that the code is really just a set of instructions for another program to interpret, the compiler (or interpreter). This lesson comes after the previous lessons explaining how text files work which build up to this lesson so people know what is actually happening when you are tying code into a text file and why that can't be directly run by the CPU.



* When programming you press keys that are stored as bytes in a text file.
* Those bytes represent Unicode code points.
* The CPU in your computer can be pointed at any byte address in RAM and treat it like an instruction.
* Every CPU manufacturer publishes a set of the various binary instructions that a specific CPU model, or family of models like Intel's x86-64, can process.
* So you could point your CPU to the first byte in your text file and it could treat it like a set of instructions.
* However, you weren't trying to write CPU instructions, you were just trying to write a text file so who knows what the CPU would do.
* In other words, when you are programming, you aren't really writing instructions for the CPU to process.
* Instead, you are writing instructions for another program to process that will create the CPU instructions for you.
* That other program is called a compiler and the set of instructions it understands is called a programming language.
* You write text files according to a programming language and then you run a compiler program and tell it where your text file is.
* It reads through your text file, code point by code point, in other words, character by character, and finds little groups of characters that go together, like words in a traditional language.
* Those words might be one character long, like a plus sign, so they are usually called tokens instead.
* Those tokens can then be grouped together in a hierarchy reflecting their relationship to one another and the compiler can then convert that hierarchy into binary instructions for the CPU.

# Why Computers Don't Care About Data Types

This is critical to understand I think. Data types don't exist anywhere in the computer. They're not necessary for writing low-level machine code. They're only used by compilers to help the programmer reduce errors when writing high-level code. Ultimately, the CPU doesn't have a concept of data types.



* Writing instructions for a compiler instead of a CPU can make programming a lot easier, but it can also change your mental model as you often have to think about how the compiler will interpret your instructions, not just the CPU.
* In fact, a lot of the instructions you give the compiler, such as data types, are never converted to CPU instructions.
* CPUs don't care about data types, only bytes.
* Data types are used to make sure the correct number of bytes are reserved for a value and so that any code that references those bytes knows how to treat them, like a number or a letter for instance.
* If the data type is a number, the size of the number you can store there is determined by how many bytes that particular data type uses.
* An integer may use 4 bytes while a short integer may only use 2.
* 2 bytes allow you to store a number anywhere from 0 to 65,535 or from -32767 to 32767 depending upon whether that data type treats the top half of its range as negative numbers.
* The top half of the range always starts with a 1 so that first digit is treated like a sign indicator telling you if the number is positive, 0, or negative, 1.
* Data types help you as a programmer catch errors in your program early since the declaration of a value and all of its uses can be checked to make sure they align.

# What is a Programming Language

Understanding that the compiler is not the programming language and that the programming language is just a set of standards that the compiler enforces on text files is important, I think. These concepts can easily be conflated in the mind of beginners I think. Explicitly separating them out is important.



* The program you write must meet the exact specifications of the language you are using.
* The language is just a set of standards and the compiler enforces those standards.
* Your compiler program needs to be able to understand exactly what you are trying to do so it can create CPU instructions for you.
* It figures that out by comparing the text of your program with the standards created for that particular programming language.
* Fundamentally all programming languages allow you to do the same things since ultimately they all have to use the exact same CPU instructions.
* This means programming languages are redundant but each may be designed to make certain types of ideas easier to express.
* This means certain languages are typically preferred by certain audiences based on what they are trying to accomplish.
* As a programmer, though, you can typically use any language available to accomplish your goal as long as you can write a program that meets the standards of that language.

# How to See Every C Program

Getting an initial grasp on the visual structure of a program is important to beginners, I think. Being able to just look at a formatted text file and just kind of have a sense of what's going on is important. This video will attempt to do that for the C programming language which so many other languages are based off of.



* Most people who create new programming languages, in other words new standards on how a compiler should treat a text file, use existing ideas from other programming languages.
* This tends to lead towards certain programming language styles with key similarities that help programmers learn new languages in that style more easily.
* C was the name of a popular programming language that inspired many of the ideas in other C-style languages like JavaScript, PHP and Swift.
* For instance, in C if you want to process something, you can make that process easily repeatable by writing your instructions separated by semicolons, wrapping them in curly braces, and giving that group of instructions a name.
* After the name, you write parentheses, potentially with more names inside for any extra data elements your instructions might need.
* Since bytes can represent any kind of data, you also tell the compiler what data type you're working with so it knows how to represent it in RAM.
* When the instructions are finished there may be a result ready which will have its own data type.
* The name of that result data type goes before the process name.
* You can also put the word void there instead if your process just does stuff and doesn't create any data as a result.
* You've just defined a function in C.
* To use it, just type its name and some parentheses, this time with values for the extra data elements, if necessary.
* If the function does not return void, you create a name for the memory location where you will keep the result.
* That result has whatever data type the function definition specifies.
* The equals sign is not a question but a command to make the new memory location equal to whatever the function result is.
* This function can be used whenever you need it just by typing its name and some parentheses along with the inputs and output if there are any.
* This style of programming is very common and something you'll see over and over again with slight variations based on the specific programming language being used.

# How Programming Functions Stack Up

This is such a cool thing to follow in my opinion, understand how functions use the stack. Since modern programs use the stack for almost everything, and function calls can become deeply nested, it's important to walk slowly through how the stack works so beginners can get a good concept of it.  



* Under the hood, functions are called using special CPU instructions that let your code continue where it left off when the function code is finished.
* The CPU has a special register called the stack pointer that keeps up with the top of a stack of data used by these unfinished functions.
* The stack pointer moves up as functions are called and moves back down when they're finished.
* The stack holds the next instruction address for each of the called but currently inactive functions along with any other data those functions will need when they become active again.
* Functions themselves can push data onto the stack and pop it off again using special CPU instructions.
* There is also a call instruction built into the CPU that pushes whatever the next instruction address after the function call is onto the stack and then jumps to the first instruction in that new function.
* That called function finishes by using the corresponding CPU instruction, return, which pops that old saved instruction address off the top of the stack and back into the next instruction address register.
* This way the code that called the function can continue where it left off.
* The stack can also hold the input data needed by a function.
* Before the call instruction may come some instructions to push data onto the stack.
* That data can then be retrieved by the called function at a specific offset from the stack pointer.
* In fact every time the function is called, the input data is always at the same offset from the stack pointer - it has to be or the function won't work.
* Actually modern CPUs now use registers to store the first 6 inputs to a function, not the stack.
* However, like legacy CPUs, they still use the stack for any extra inputs beyond the first 6, which is rare.
* Either way, these inputs are then used by the function to compute a result.
* The result from a function is then saved in another CPU register before the function finishes.
* Although functions can only return one output that one output could be a RAM address that points to a larger data structure that holds lots of values.
* A return value though, pointer or not, must fit in one register.

# How the Stack Works: (aka Doing Lists)

This concept of a "doing list" made so much sense to me as an explanation for how the stack works. It really helps you understand what the purpose of the stack is and why its so important.



* The stack is like a doing list.
* A doing  list is like a todo list but items are added to it backwards, from the bottom up, and then erased top down when they're completed.
* The doing list keeps track of all the things you're in the middle of doing and whatever you're currently doing is always at the top of the list.
* The other parts of your list tell you what to do  but the doing section tells what you're doing  right now, or were doing that you haven't finished yet.
* You can keep track of as many unfinished tasks as you like, it just matters how big the doing section of your list can get.
* If it gets too big, then you overwrite some of your todo items above the doing section
* This is called a stack overflow in programming.
* Sharing your todo list with others allows them to use the doing section of your list also.
* If you need someone else to help you do something, you add the item number of your next task to the top of the doing section
* This way you'll know what to do next when you get the list back.
* Then you give them your list and point them to the next todo item so they know where to start.
* They work your todo list starting at that instruction and you wait for them to finish.
* They can add items to the doing section as they go, erasing them when they're done.
* When they return the list back to you, you can look at the top of the doing section and know where you left off since everything they did has been erased.
* No matter how many people help you with your list or how many people help them, everyone can still keep track of everything they're doing using that same doing section  of the list.
* That's how functions use the stack.

# Understanding Variables

The basic concept of variables is important to understand as the name for an address in RAM.



* A compiler allows you to name certain addresses in RAM so you can store data at those addresses and easily refer back to them later.
* Names given to a RAM address where data is kept is usually called a variable since the value of that data can vary over time.
* The variable named "x", for instance, refers to the first of possibly several RAM addresses where the bytes represent the value of "x".
* How many bytes are used depends upon the data type of "x."
* A name can also be given to the address of the first instruction in a function.
* That function may have many instructions but the first one is always the most important since that is where the CPU jumps to when that function is called.

# How Recursion Works

This is the simplest explanation of recursion that I can think of, it's a named loop. It's implemented in assembly the exact same way as a regular loop, a jump back up to an earlier instruction in RAM over and over. It's just that recursive loops have names for the earlier instruction (the function name) and they often use the stack to keep track of data in the loop.

Stack overflows set the limit for recursive functions unless you are using tail call recursion which doesn't use the stack Tail call recursion is exactly that, the function calls itself at the tail end of the function body - meaning it's the last instruction in the function. That way return data doesn't build up in the stack since there is nothing left to do after each function call finishes.



* The name of a function is at the top of the function definition, but you may also put it inside the function definition as well.
* This inner name creates a CPU instruction that jumps back up to the first instruction in that function.
* This will cause the list of instructions in the function to run over and over in a loop forever, unless you first check some condition before calling the function again.
* When that condition is met, the function finishes and the data that was piled in the stack each time the function was called is unstacked as each call returns its data to the previous call all the way back to the first which returns one final result.
* This repetitive use of the same list of instructions is how all loops are performed in a program, except sometimes the loops aren't named.
* When they are, it's called recursion: a function calling itself.
* Sometimes the function stacks its data up with each call, but preferably not since the stack only has a limited capacity.
* If a recursive function doesn't use the stack to accumulate data, it's called tail call recursion because the function only calls itself at the tail end of its list of instructions.
* This means the result doesn't need to be processed by any previous calls of the function since they don't do anything with the result after they get it.
* When the last function call is finished, the final result is already ready so there's no reason to unwind the stack.

# How Code Libraries Work

Understanding that coding is so much more about understanding the standard libraries of the language you are using than just understanding how to write the code correctly is an important lesson I think. If you can understand the standard libraries of your language, you can get so much more accomplished with less knowledge of algorithms and other deep concepts.



* Grouping multiple instructions together into a function is useful as is grouping multiple functions together into a library.
* A function is a group of instructions that you want to use in your program more than once and a library is a group of functions that you want to use in more than one of your programs.
* Libraries keep you from having to write the same functions over and over again since they can be referenced by any program that needs them.
* Learning libraries is almost as important as learning programming languages since much of what you accomplish in programming will be via a library.
* Each programming language has its own set of libraries available for common tasks and there is usually a central repository online where these libraries can be downloaded.
* The libraries are kept separate from your code, but the compiler will link your code to a library function when you use it.
* The links are actually resolved to specific RAM addresses once the executable file produced by the compiler is actually run on the computer.
* The operating system will replace the symbolic function name added by the compiler with a pointer to the first address where that library function has actually been loaded in RAM.
* This extra layer of indirection adds flexibility. Dynamically linked libraries, called DLLs in Microsoft Windows, offer most of the capabilities that your program, and the operating system itself, have to offer.

# How Data Can Change Itself

This is a setup to understand classes later on.



* Functions can be grouped together with other functions into libraries but they can also be grouped together with other functions that process the same data structure.
* In fact, the data structure itself can hold a reference to these functions.
* Data structures don't have to be a single element like a number or letter, they can also be larger structures with those elements inside.
* Some of those elements can be pointers to the functions that can process that data structure.
* An employee data structure can contain pointers to all the functions that process employee data, for instance.
* One function may change the job title and another may change the salary but they are all accessible from the employee data structure itself.

# How Pointers Work

A key, often misunderstood concept. Pointers exist when the data in RAM represents the address of other data in RAM. Pointers can be very useful in programming.



* A pointer simply means the data at a RAM address represents another RAM address.
* It's like the data is pointing to that other RAM address.
* At that address could be anything. It might be the first byte of a large data structure.
* It might also be the first byte of the first instruction in a function.
* Or it could even be a pointer itself.
* An address can only be treated like data because they are both represented as binary numbers.
* These pointers make it possible to use RAM more efficiently since a large data structure doesn't have to be copied around to multiple places in RAM.
* The address of the first byte of that data structure can be copied around instead.
* This gives functions access to that data structure directly without having to make a copy of it.
* The data in the structure can be changed in place by these functions since they know how to find it in RAM.
* A pointer is always the same size even if it is changed to point to a different data structure.
* That's because all RAM addresses in a computer are the same size so it always takes the same number of bytes to represent them.
* Since pointers are always the same size, they always take up the same amount of space, even when they're used in a larger data structure.
* This is important because it means these larger data structures can always take up the same number of bytes in RAM, even when they include pointers.
* Pointers also allow data structures to take up less space in RAM since each structure can keep references to the other data structures they need instead of full copies of them.

# How Classes Work

...



* The layout of a data structure in RAM is always the same, even if that data structure is copied to multiple places in RAM.
* There may be multiple employee data structures in RAM, for instance, representing different employees, but they will all have the same data fields in the same order in RAM.
* This is why the functions that process this type of data structure can process any particular copy of that data structure.
* These functions are programmed to find certain data fields in that data structure at certain places in RAM, relative to the starting address of that particular data structure.
* Since the pointer to the string of characters holding the job title is always the second data element in the employee data structure, for instance, the function that changes the job title always knows where to find it.
* Data structures are classified according to how their data is laid out in RAM.
* Each layout is given a name.
* The employee classification, or class for short, is the layout of data in RAM as needed for the fields that hold the data for an employee.
* The compiler knows how many bytes to reserve for an employee in RAM by referencing this class definition.
* A class tells the compiler how to represent a set of data fields in RAM, but it doesn't actually reserve those bytes in RAM.
* When you're ready to represent a particular employee in RAM you tell the compiler to set aside a new block of bytes in RAM, called an object.
* Every object has the exact same data fields in the same order in RAM as other objects of that class, it's just that the values used for each data field are different.
* The compiler knows where each data field begins in that block of RAM and what initial value each field should have by referencing that object's class.
* The class definition can also tell the compiler which field values must be set by the programmer when they construct a new object of that type.
* These constructor functions ensure fields are properly populated before they are used.

# How Class Interfaces Work

A setup to generic interfaces.



* If two data structures objects have the same data fields in the same order in RAM it's possible for the compiler to treat them the same way.
* If the compiler knows the Promote function pointer always starts at the 9th address down from the top of each object, for instance, it doesn't matter which class that object has, the compiler still knows how to Promote that object.
* The order that fields and pointers are placed in a data structure is called its interface.
* It's how you work with that object from other parts of your code.
* Not only can objects share an interface, but so can functions.
* If you can call two different functions using the same number and type of inputs and you get the same type of output, then those functions have the same interface.
* For two data objects to have the same interface, any function they point to must have the same interface too.
* Two data objects can be of different types, in other words they could have been created by the compiler using different class definitions, but they may still share the same interface
* This means the compiler can treat a Manager object like an Employee object or an Employee object like a Person object, for instance.
* They all have the same fields and function pointers in the same order, or at least they all share the initial set of fields applicable to all of them.
* The Manager object has more fields and pointers than the employee object but the manager and employee both have the same fundamental fields as the person object.
* It's almost like the person class is the template that the employee class is built off of and the employee class is the template that the manager class is built off of.
* The compiler can treat any of these objects like a person since they all share the first set of fields as the person class.
* You can also treat a manager like an employee since both classes share the same fields, the person fields plus the employee fields.
* You can't treat a person like a manager, though, since the compiler might think it can promote that person, but that person may not be an employee, let alone a manager.
* That's the kind of error the compiler helps you prevent.

# How Interfaces Work

An explanation of interfaces as a (usually) fully abstract concept.



* If a compiler only has to know what fields come in what order to use an object, that interface can be defined separately of any particular class.
* An interface just tells the compiler what particular fields an object has and where to find them, relative to the starting address of that object.
* Any class can then implement that interface, as long as it has all the fields defined in the interface.
* The interface itself, though, just tells you the structure than an object will have, it doesn't allow you to actually create an object with it.
* For that reason, an interface is only allowed to be used as the data type for the memory location that will hold a pointer to an object.
* It doesn't have a constructor function so you can't actually create a new object of that type.
* In other words, it can be used on the left side of the equals sign, but not the right.

# Why Interfaces are Useful

Understanding interfaces as "contracts" was never helpful for me. Understanding them as pre-programmed remote controls would have been much more helpful for me, I think.



* Interfaces allow you to program to an abstraction, not a concrete implementation.
* It's like your first day on the job you're given a remote control and told people will call you to press the buttons but you won't know what device the remote is hooked up to.
* You just do as you're told and whatever happens happens.
* Whoever gave you the remote control preprogrammed it for you, or whoever gave it to them.
* Interfaces are passed into functions like that remote control.
* The functions press the buttons on that remote control but don't ultimately know what they do. They just know what buttons are on that specific remote.
* This way you can pre program that remote to control a TV or a fan, or any other device that has the same basic functionality.
* You can use a simple remote control with only a few buttons to control a lot of different devices that all implement at least those few actions, or you can use a complex remote control with lots of buttons to control a smaller number of complex devices that implement all those actions.
* Either way, the remote control is only programmed to one specific device at a time, but the function you give it to doesn't have to know which one it is.
* This means the function can perform some generic task that could apply to any of the devices controlled by that remote.
* The more generic you can make your code, the more it can be reused for different tasks, so the less code you need.

# Why Indirection is Useful in Programming

Basically, an explanation of the reasoning behind the "[fundamental theorem of software engineering](https://www.google.com/url?q=https://en.wikipedia.org/wiki/Fundamental_theorem_of_software_engineering&sa=D&source=editors&ust=1705519967348424&usg=AOvVaw0pl7K1v0ppN2yOKR91TQRk)".



* Writing code that does things indirectly, using interfaces for instance, is the heart of problem solving in programming.
* There's a famous saying in programming that says "any problem in programming can be solved with another layer of indirection".
* "Layer" and "indirection" are the key words.
* This basically means that not every part of your code should be dedicated to doing the real work.
* Some of your code should be making decisions at higher levels and letting other code do the real work.
* It also means that those different levels should not be interacting with each other directly, but through interfaces.
* Interfaces are indirect because you don't know what they control on the other side, you only know what they allow you to do. It's the same idea as management.
* The more complex organizations get, the more need there is for higher level decision making.
* When those decisions are made at a higher level, there's usually no knowledge of how they will actually be implemented at a lower level.
* This organizational structure allows the generic goals to be managed separate from the specific details about how those goals will be accomplished.
* This approach can be tremendously helpful when adding new devices for your code to use, such as a new database system or a new app platform.
* As long as you set up your management layers to be able to interface with any of these devices by using the same set of fields and functions, you don't have to change that management layer at all when those new devices are added.
* All you have to do is make sure the code for the new device will be able to implement your existing interface.
* Then you just preprogram the interface to control your new device and pass it as input to your management code.
* Your management layer uses the same policies and procedures it always has to make decisions, they're just being implemented differently unbeknownst to that layer.

# Using Mocking to Test Code

I wish I had really gotten a clear understanding of what "mocking" was early on. Testing seemed like such an abstract and even arcane subject to me when I first started out, especially as it relates to mocking.



* Interfaces can be used to control mock devices that don't actually exist but that do things a real device would do.
* Why would you want to do that?
* To test your code to see if everything still works even after you've made a change to it.
* You don't want to test new code with the real device in case something goes wrong in the code and breaks the real device.
* Instead, you pre-program the remote to control a mock device and then give that pre-programmed remote to the new code.
* If the new code causes the mock device to break, it will cause the real device to break too.
* These mock devices are created in separate test code and passed via an interface to the main code.
* Certain actions are triggered in the main code and then the mock device is checked to see if the results are as expected.
* Due to the amount of code that exists in most projects, it's usually not feasible to know if all the code is working properly by just looking at it.
* Instead test code can be written that uses interfaces preprogrammed to mock devices allowing the application to be extensively tested.
* This type of testing is called regression testing because you're testing if the code base has regressed and failed where it wasn't failing before.
* These tests are usually run automatically every time a new batch of changes is made to the application so developers know if their changes broke any existing functionality.

# How Git Works

Oh git. How critical you are to coding yet how seemingly complex and arcane. This is the first of several sections to really break down git and try to explain it slowly and simply.

Specifically about git branches, I did NOT get this concept early on. I didn't understand that the entire set of files and folder for the application were kept inside a branch, and that you could have multiple branches and each one could have the ENTIRE set of files and folders inside it, usually only with a small set of changes between them.



* When programmers make changes to code, they are changing the contents of text files.
* Those text files are usually a copy of some text files sitting on a remote computer.
* That remote computer exists so that multiple programmers can work on a program at the same time.
* Each programmer just copies the text files off the remote computer and makes whatever changes are necessary.
* When the programmers finish making changes to those files, they can be copied back to the remote computer.
* If the same text file is changed by two different developers at the same time, though, the changes made by the last developer to upload the files are kept and the other developers' changes are lost.
* To prevent this, developers use version control software like Git that runs on each developer's machine and on the remote computer to make sure all the changes made by different developers are properly synced up and merged appropriately.
* All the history of changes that have ever been made, along with all the actual text from old versions of the text files, are kept in what's called a repository, or repo for short
* The repo is just the name used for the whole project history for a single application
* However any particular version of the application is kept in what's called a branch
* The entire set of text files for the current version of the application are kept in a single branch, for instance- often called the main branch.
* A single repo may have many branches within it, with each branch usually containing the entire source code for that program but each with a slightly different version of the application.
* Maybe one branch is that main branch that has the code used in the live system, while another branch has nearly the exact same code except with a few small changes to fix a bug found in the live system.
* The code in the bug fix branch can then be merged into the main branch once the developer is satisfied that the bug is fixed.
* A merger just updates one set of text files in one branch with the same set of text files in another branch, often with minor changes
* So a single branch within the repository will consist of all the files needed for the application.
* This means that a developer only works on one specific branch at a time.
* It also means that only a single folder on the developer's machine has those files in it - so what happens when the developer decides to look at a different version of the application by switching which branch is active on his local machine
* If the developer wanted to checkout a different branch, all the files in that local folder would be deleted and replaced with the files from that other branch.
* Any changes made locally to the files in the old branch will be lost when the new branch is checked out, unless those changes had already been added to the version control system.
* There is a multi step process, above and beyond just saving the files, that allows them to be tracked by version control.
* Using Git, for instance those files must first be added to a local index of files.
* That index must then be committed to that branch
* Once those changes are committed to that branch, then they'll still be there even after the developer looks at the files in a different and then comes back to the first one.
* Finally, every other developer won't see those changes on their local machine until that branch is first pushed up onto the remote server and then pulled down by those other developers.
* In other words, until the updated branch is pushed up to the remote server and then pulled down to their machine, no other developer can see the changes made.
* To keep track of all this, Git uses a hidden subfolder in the local folder to keep track of all the data on all the branches.
* This subfolder contains compressed files that ultimately contain all the text for all the files in all the branches.
* All the code in all the branches in version control is saved on each developer's machine and on the remote server.
* Changes made to one branch on one machine do not automatically update to all the other machines as we discussed.
* Any changes made to a branch are first saved, indexed, and committed locally on that machine, and then that updated branch is pushed back up to the remote server.
* Before other developers make a change to that branch, they first pull a copy of it off the remote server to their local machine.
* This ensures their copy of the branch is up to date so their changes don't conflict with the ones already made.

# Git Ready

Git only handles the text files for an application that are fed to a compiler, not the results of the compiler which can be the actual binary files with instructions for the CPU.

* Changes to text files that are tracked by version control software do not immediately show up in the live application, even after a branch is pushed from the developer's machine to the remote server.
* After all, a branch only holds the text files for a program, not the executable files.
* The executable files must be built from the text files by a compiler.
* Since the executable files are large and since they can be rebuilt from the text files at any time, they're not saved in the version control system with the text files.
* Instead, they're built only when they're needed.
* Each developer's computer builds the executable files for an application when the developer is testing locally and a remote server will also need to build them again when the changes are ready to go live.
* Often there is a long list of steps that must be taken when updating an application, including updating the main branch, building executable files and then releasing those executable files to the application server.
* Online services, like GitHub, exist to allow you to manage all these steps in one place.
* Github adds extra features not available in the standard Git software like Pull Requests.
* Pull requests are made by one developer to other developers requesting that they approve that changes made on a development branch can be pulled (merged) into a main branch.
* Once approved, that development branch is merged into the main branch.
* When the main branch is updated, GitHub can then trigger new executable files to be built, sent to test servers and then to production once they've been approved.

# Why Operating Systems Are Needed

...



* Running a program requires a program already running.
* That program calls a function you defined, usually called main, to kick off your program.
* The Main instructions you wrote then call whatever other functions you called in your program that do all the work.
* The program that calls your program is called the operating system.
* The operating system is a series of instructions and function calls like everything else.
* The difference is that it has special access to the resources on the computer that no other programs have.
* To access resources on the computer, such as files on the hard drive, your program first calls a function in one of the dynamically linked libraries owned by the operating system.
* Sometimes those DLLs end up calling other functions that only they can call, no user level code can call directly.
* These special functions are a part of what's called the kernel of the operating system, which are just another set of DLL files.

# How Operating Systems Multitask

...



* The operating system kernel contains some of the most secure low-level code in the computer.
* It does things like make sure the CPU isn't spending too much time processing the instructions from a single application and neglecting the others.
* To prevent this, the kernel sets a hardware timer that will interrupt the CPU when the timer expires.
* This interrupt forces the CPU to stop whatever program it's running and jump to the code that handles the specific interrupt triggered.
* Interrupts are triggered for different reasons, such as requested data now being available from a relatively slow external device like a hard drive, so they are handled by different sets of instructions.
* This forced multitasking makes sure any application that freezes will not bring the entire computer down with it.
* It also allows the CPU to run the program code for every window in quick succession so that it feels like multiple applications really are running at once.

# How Executable Files Work

...



* When a program is compiled, the compiler goes through a series of stages that each produces its own output.
* The output from each stage becomes the input to the next.
* The final output is an executable file that can be loaded and run by the operating system.
* On Windows, that executable file can either have an exe or dll file extension since dynamically linked libraries are loaded to RAM the exact same way as a regular program.
* Executable files have a very specific binary format that allows the operating system code to load and run them on the computer.
* This format is called Portable Executable or PE for short on Windows computers.
* These files all start off with a short program that old 16 bit computers with MS-DOS installed would run which displayed a message saying Windows was required to run the program.
* There are then headers in the PE file that tell the operating system where the rest of the sections are located in the PE file.
* Each section represents code or data of some sort.
* The so-called "text" section is where the CPU instructions for your program are kept.
* Another section of the Portable Executable file contains a list of all the dynamically linked functions you use in your program.
* When it loads your executable file into RAM, Windows creates an Import Address Table that connects this function list to the correct address in RAM where those library functions actually reside.
* Correspondingly, those DLL files, again using the same Portable Executable binary file format as the exe files, have a section containing a list of the functions that it makes available for other programs to use.
* Windows then creates an Export Address Table for these DLL files when loading them into RAM.

# What is a Process and What is a Thread?

...



* When an executable file is loaded into RAM it becomes part of a process created by the operating system.
* A process gets its own complete copy of RAM, or at least the operating system and hardware coordinate to make the process think it has its own copy of RAM.
* They translate any virtual RAM address used by the program to a real RAM address, checking first to make sure the program is not requesting an address it is not allowed to access.
* This virtual memory address translation also enables more efficient use of RAM because different processes can have virtual addresses that are mapped to the same physical area of RAM.
* The executable file is placed into this virtual address space with each of its sections starting at a new page boundary.
* All the DLLs used by this executable file and all their sections are also mapped into this same process address space.
* The import address tables and export address tables are in these sections as well allowing your program to call functions in these DLLs.
* All the specific addresses used were determined by the operating system loader program that created the process address space for your executable file when you ran it.
* The actual execution of the code in your process address space occurs in a thread.
* A thread is a concept used by the operating system to separate the processing of one sequence of instructions from another.
* The CPU can process multiple sequences of instructions at a time.
* CPUs normally have multiple cores and each core is usually hyper threaded which means it can process multiple threads at a time.
* This CPU, for instance, has 6 cores and each core can process 2 threads so that's logically like having 12 processors in the computer.
* Each thread is given its own stack, which is also mapped into your process address space.
* In fact, each thread has both a user-mode stack for your program to use and a kernel-mode stack that's used by the operating system kernel to perform restricted actions on behalf of your program.

# How Operating Systems Schedule Threads

...



* With multiple applications open, there are usually way more threads those applications need to run at any one time than there are logical processors available.
* The operating system kernel runs a scheduler program constantly that schedules these threads to be executed from a prioritized queue it maintains of active threads.
* When a thread finishes, its allotted time slice has elapsed, or a higher-priority thread needs to run, the kernel pushes the thread's current state, including all the CPU registers, onto the stack and then pops the state of another thread off the stack and into the CPU registers to begin executing.
* The kernel itself may also process some of its own code in the interim as well.
* The amount of time allocated to each time-slice is small, usually only 20 milliseconds or so.
* The kernel sets a timer for this amount of time that triggers a CPU interrupt when it expires, forcing a new thread to run.
* This means around 50 different time slices are available per second on each logical processor.
* These time slices help the user feel like the computer is running all their applications at the same time.
* Applications can be programmed to use multiple threads: one to display the window on the screen and one to perform a slow task like retrieving a file from the hard drive, for instance.
* If these tasks used the same thread then the user interface would freeze until the file was retrieved.
* The file retrieval thread can also block itself from running again until a certain event occurs, such as the file data being available.
* The operating system will skip over this thread the next time a time slot opens for it.
* When the file data is available, the hard drive will trigger a CPU interrupt to load the data into RAM and continue with the blocked thread.

# How Operating System Events Are Handled

...



* Operating systems capture events that occur in each window on the screen and then call the associated application code you wrote for that application making each event available to it.
* Your main code runs a set of instructions in a loop checking these events to see if there is one it cares about.
* Each application may be using multiple windows even though it may only appear to have one.
* Notepad on Windows, for instance, actually has many windows inside as you can see with the free Spy++ tool in Visual Studio.
* There are lots of different types of events that can occur in each window, such as mouse movements, keyboard buttons being pressed down or being let up, scroll wheels going up or down on the mouse.
* When you are creating an application for Windows, you write it in a language like C and work with these windows and events using Microsoft's Windows API, or WinApi for short.
* An Application Programming Interface, or API, is a set of standards you must follow when writing functions so that they can interact with the target system.
* Using the WinApi ensures the operating system can properly call your main function when starting your application which itself calls operating system functions to check for and process these events.
* Applications such as web browsers, can create their own events similar to the ones that occur inside their windows.
* When a user moves their mouse pointer over a button inside a browser window, for instance, and clicks their mouse button, the browser application receives that click event from the operating system and then creates its own similar event to be processed by the JavaScript code running on that website.
* That JavaScript code then processes the click event for that button.

# How the Operating System Interacts with Hardware

...



* Hardware devices are accessed via addresses just like RAM data.
* You can see these addresses in Device Manager on Windows under the "Resources by Connection" view.
* Devices either use the same memory addresses as RAM, except the data is routed to the device instead, or they use a separate address bus used just for devices.
* When a program needs to interact with that device it does so with the help of a driver.
* A driver is a piece of software running at the same security level as the kernel of the operating system.
* To interact with hardware, your program calls a function in an OS-level DLL which, in turn, calls a function in a kernel-level DLL that interacts with the device using its driver.
* Using multiple layers of indirection like this allows the operating system to remain flexible enough to use new devices that did not exist when the operating system was created.

# How GPUs Work

...



* Displaying complex graphics can be costly for CPUs as they are designed to process a long thread of instructions as quickly as possible.
* GPUs are more fit to that purpose as they have lots more processors that can process multiple parts of the display at the same time.
* An image is typically processed by a GPU by splitting it up into equal sized blocks and processing those blocks in parallel.
* Instead of one thread with lots of instructions like a CPU, a GPU processes a single instruction on multiple threads.
* Nvidia calls this technique SIMT for Single Instruction, Multiple Threads and it is used heavily in their CUDA GPU programming language.
* This massively parallel form of computing is great for processing graphics but it also turns out to be great for Artificial Intelligence algorithms as well.
* These algorithms often use grids of numbers, each called a matrix, to calculate a result much like pictures use a grid of pixels allowing a GPU to process these AI algorithms in the same way as pictures.

# How Computer Snapshots Work

...



* A program proceeds one snapshot of the CPU at a time.
* You could save a snapshot of the data in the CPU and RAM, turn the computer off and on, and then load those snapshots back to the CPU and RAM and the program would continue as if nothing happened.
* This ability to preserve snapshots for later use allows the entire state of a computer to be stored in its own file.
* Specialized software can then load and run these files as if they were virtual machines running inside of the computer.
* Multiple virtual machines can even be run on one physical computer at the same time.
* This is the basis of cloud computing where multiple customers are able to use the same physical device without conflict.
* Newer virtualization technologies don't require the entire snapshot of RAM be saved but only a small container with just those operating system files necessary to run that particular application.
* These containers are much smaller and more versatile than virtual machine snapshots.

# Why Config Files are Useful in Cloud Computing

...



* A program tells the computer exactly what to do step by step.
* However as cloud computing advances, you don't necessarily know what specific computer or even operating system will be running your program.
* This means you may not know exactly how to tell the computer what you want it to do.
* It can be easier to tell the cloud service what state you want the computer to ultimately be in rather than how to get there step by step.
* This leads to the use of more configuration files in programming rather than just source code files.
* These configuration files are used heavily in cloud computing as they allow the cloud providers to be a lot more flexible in delivering their services to customers since there are less implementation details involved.
* This also makes the process easier for customers since they don't have to manage every tiny implementation detail necessary to get the infrastructure off the ground.

# How Data Encoding Works

...



* Data can be encoded in bytes in various ways.
* Sometimes the program reading a file knows exactly what the bytes mean based on where they're located in the file.
* Looking at those same bytes you may see meaningless information, but the program reading that file knows exactly what they mean because it is programmed to read that file by assuming its bytes have a particular layout in memory.
* This is how executable files work. The operating system is built to understand a particular binary format of executable files, such as the Portable Executable format used on Windows, and decipher these executable files based upon where it expects to find the data inside.
* Other file formats may encode data using bytes that strictly represent text characters.
* These text files are the basis of not only every programming language file, but also most data files sent over the internet.
* Data structures can be encoded in text files using an extra layer of encoding where, for instance, words are separated by colons to represent data elements of names and values.
* These name value pairs are then separated by commas to form a list and elements can even be nested inside other elements to form hierarchies.
* Using the parsing rules for this encoding format, a program then determines what relationships these elements have to each other and converts the entire data structure into a computer-friendly data format.
* That data is then processed by the program and a new text file in the same format is usually sent back.
* Since there are so many different types of computers and programs out there, it can be hard to find data formats that are ubiquitous and can be read by all of them.
* Text files fill this gap.

# How Relational Databases and SQL Work

...



* When large amounts of data need to be stored on a computer and processed quickly, databases are often used.
* Databases store data in binary files to improve processing speed and to reduce file sizes so more data can be stored in the same number of bytes.
* Databases pack the data elements together into rows and then pack those rows together into what are called tables.
* Every row on each table has the same data elements in the same order and each data element takes up the same number of bytes.
* This way the computer can quickly jump to the 3rd row and the 5th data element, for instance, using a simple calculation.
* Any variable-length data is saved elsewhere and a fixed size reference to that data is kept in the table.
* A row of data in one table can relate to a row in another table by storing the other row's ID as one of its data elements.
* This allows complex relationships between data sets to be created.
* Programmers control the structure of database tables and the data inside them using a special programming language called SQL.
* For example, using SQL you can select data elements by name from a particular table where the values of those elements match the values you specify.
* You can also use SQL to delete that data in nearly the same way and insert it again by listing out the names of the data elements followed by their values.

# How Computers Send Data Over a Network

...



* When computers need to send each other data, they do so in a similar way to how we communicate.
* If you're in a conversation with friends and you start talking at the same time as another friend, you both normally stop talking right away.
* You both usually wait for a second or two and then try to start talking again.
* This is how computers communicate over a network too.
* When computers have something to say and there's nothing being said, they send a meaningless pattern of bits onto the network to let other computers know they have something to say.
* If they sense another computer sending a signal at the same time, they stop and wait a random amount of time to start again.
* If there's no conflict then they begin sending the main part of their message.
* First they send the unique identifier for the computer they are addressing, their own unique identifier, and what they're going to be talking about.
* They then share something on that topic in no more than 1500 characters.
* Oddly they may communicate what someone else said, and that person may have been communicating what someone else said too.
* It's as if there is a message within a message within a message, which is exactly how Ethernet, IP, TCP, and HTTP work.
* They're all packed inside the other like boxes inside boxes.
* Different programs in the computer unpack different boxes until the application that made the request, like a web browser, receives its box and processes it.
* It may send out another request inside an HTTP box that gets put into a TCP box, packed in an IP box, and finally shoved in an Ethernet box to be sent to another computer on the local network.
* Each box has its own header data written on top of it.
* Other computers will unpack and repack the Ethernet box with new headers along the way, based on which computer is closer to the target IP address.
* The inner box with the core message stays pretty well intact until it gets to the destination where it will be processed.

# How HTTP Requests Work

...



* An HTTP request has a text header with name and value pairs separated by colons.
* After these headers is an empty line followed by the body of the HTTP request, if there is one.
* HTTP requests include a verb at the very top that tells the server what the client wants to do.
* GET requests are used to get resources from a server and the address of the website is typically enough for the server to know what the client wants, so GET requests don't need a body.
* When you fill out a form on a website and submit it, an HTTP POST request is normally sent with the form's data in the body of the request.
* When the HTTP response comes back from the server to your browser, it also includes headers of key value pairs followed by a blank line and the body of the response.
* The body of the response usually includes binary encoded data like images or text encoded data like HTML or JSON.
* HTML tells the web browser how to display a web page and JSON is usually received when the JavaScript in that HTML requests additional data because a user presses a "Show More" button, for instance.
* That JavaScript then displays the JSON data by adding new elements to the HTML.
* The HTML format surrounds a value with its name on both sides while the JSON format puts the name before the value with a colon in between.
* JSON is heavily used by almost all programming languages to store and transmit data since it is easy for programmers and programs to read quickly due to its simple rules.

# Extra Notes:

https://learn.microsoft.com/en-us/archive/msdn-magazine/2002/february/inside-windows-win32-portable-executable-file-format-in-detail
https://learn.microsoft.com/en-us/archive/msdn-magazine/2002/march/inside-windows-an-in-depth-look-into-the-win32-portable-executable-file-format-part-2
https://www.youtube.com/watch?v=CM2Tfvxrs74&ab_channel=DrJoshStroschein

https://techcommunity.microsoft.com/t5/windows-blog-archive/pushing-the-limits-of-windows-processes-and-threads/ba-p/723824
“Every thread has both a user-mode stack, which is what I’ve been talking about, but they also have a kernel-mode stack that’s used when they run in kernel mode, for example while executing system calls.”


https://learn.microsoft.com/en-us/windows-hardware/drivers/gettingstarted/user-mode-and-kernel-mode

https://www.codeguru.com/windows/how-do-windows-nt-system-calls-really-work/

https://learn.microsoft.com/en-us/windows-hardware/drivers/gettingstarted/virtual-address-spaces


GPUs - How CUDA Works
https://www.nvidia.com/en-us/on-demand/session/gtcspring22-s41487/
How GPU Computing Works
https://www.nvidia.com/en-us/on-demand/session/gtcspring21-s31151/


the minimum access size of 64 bytes, which matches the cache line size used by x86 microprocessors.
https://en.wikipedia.org/wiki/DDR5_SDRAM



Virtual memory requires the processor to translate virtual addresses generated by the program into physical addresses in main memory. The portion of the processor that does this translation is known as the memory management unit (MMU). The fast path through the MMU can perform those translations stored in the translation lookaside buffer (TLB), which is a cache of mappings from the operating system's page table, segment table, or both.
https://en.wikipedia.org/wiki/CPU_cache


https://learn.microsoft.com/en-us/windows-hardware/drivers/gettingstarted/what-is-a-driver-


Most of the requests that are sent to device drivers are packaged in I/O request packets (IRPs). 
https://learn.microsoft.com/en-us/windows-hardware/drivers/gettingstarted/i-o-request-packets

https://www.travismathison.com/posts/PEB_TEB_TIB-Structure-Offsets/

https://www.entsoftsol.com/Home/Blog/memory-and-disk-io-in-windows

https://www.microsoftpressstore.com/articles/article.aspx?p=2201309&seqNum=3



https://www.thewindowsclub.com/ntoskrnl-ntkrnlpa-exe-win32k-sys-files

This article provides an overview of the core libraries that are included with every modern Windows installation, on top of which most Windows applications are built.
https://en.wikipedia.org/wiki/Microsoft_Windows_library_files

TCP Fundamentals Part 1 // TCP/IP Explained with Wireshark
https://www.youtube.com/watch?v=xdQ9sgpkrX8

https://www.informit.com/articles/article.aspx?p=21320&seqNum=4


How to Find Which Process is Listening on a Given Port in Windows 10
https://www.top-password.com/blog/find-which-process-is-listening-on-given-port-in-windows/

netstat -aon

Then find PID in process explorer

https://answers.microsoft.com/en-us/windows/forum/all/device-io/8ee64904-e136-4484-920c-fc4a14b43c45

https://www.fpgakey.com/wiki/details/352
some architectures, such as IA64, port I/O occupy physical address space

The cmp instruction computes the subtraction and sets flags according to the result, but throws the result away.
https://learn.microsoft.com/en-us/windows-hardware/drivers/debugger/x86-instructions



C# Managed object internals, Part 1. The layout
https://devblogs.microsoft.com/premier-developer/managed-object-internals-part-1-layout/
https://devblogs.microsoft.com/premier-developer/managed-object-internals-part-2-object-header-layout-and-the-cost-of-locking/
https://devblogs.microsoft.com/premier-developer/managed-object-internals-part-3-the-layout-of-a-managed-array-3/
https://devblogs.microsoft.com/premier-developer/managed-object-internals-part-4-fields-layout/

```
public class ClassWithNestedCustomStruct
{
    public byte b;
    public NotAlignedStruct sp1;
}
Size: 40. Paddings: 11 (%27 of empty space)
|========================================|
| Object Header (8 bytes)                |
|----------------------------------------|
| Method Table Ptr (8 bytes)             |
|========================================|
|     0: Byte b (1 byte)                 |
|----------------------------------------|
|   1-7: padding (7 bytes)               |
|----------------------------------------|
|  8-19: NotAlignedStruct sp1 (12 bytes) |
| |================================|     |
| |     0: Byte m_byte1 (1 byte)   |     |
| |--------------------------------|     |
| |   1-3: padding (3 bytes)       |     |
| |--------------------------------|     |
| |   4-7: Int32 m_int (4 bytes)   |     |
| |--------------------------------|     |
| |     8: Byte m_byte2 (1 byte)   |     |
| |--------------------------------|     |
| |     9: padding (1 byte)        |     |
| |--------------------------------|     |
| | 10-11: Int16 m_short (2 bytes) |     |
| |================================|     |
|----------------------------------------|
| 20-23: padding (4 bytes)               |
|========================================|
```

https://stackoverflow.com/questions/2413483/virtual-method-tables
https://stackoverflow.com/questions/926352/how-is-valuetype-gettype-able-to-determine-the-type-of-the-struct
https://en.wikipedia.org/wiki/Virtual_method_table

Clang memory layout stuff
https://stackoverflow.com/questions/1632600/memory-layout-c-objects#27682344
https://eli.thegreenplace.net/2012/12/17/dumping-a-c-objects-memory-layout-with-clang/
https://devblogs.microsoft.com/cppblog/diagnosing-hidden-odr-violations-in-visual-c-and-fixing-lnk2022/

https://stackoverflow.com/questions/6664313/vftable-what-is-this
The dispatch table is the same for all objects belonging to the same class, and is therefore typically shared between them. Objects belonging to type-compatible classes (for example siblings in an inheritance hierarchy) will have dispatch tables with the same layout: the address of a given method will appear at the same offset for all type-compatible classes.

https://stackoverflow.com/questions/3972548/virtual-dispatch-implementation-details
Typically, compilers compose a new vtable which consists of all the vtables of the virtual bases appended together in the order they were specified, along with the vtable pointer of the virtual base.They follow this with the vtable functions of the deriving class.

How the 8086 processor's microcode engine works
https://www.righto.com/2022/11/how-8086-processors-microcode-engine.html
In other words, microcode forms another layer between the machine instructions and the hardware.

The little visuals on this page are awesome. They allow you to see coding without being interrupted by details you don’t understand.
https://flow.org/

HTTP Version Explanations
https://m.youtube.com/watch?v=a-sBfyiXysI
The channel has all kinds of other stuff:
https://m.youtube.com/@ByteByteGo

How the 8086 processor determines the length of an instruction
https://www.righto.com/2023/02/how-8086-processor-determines-length-of.html

