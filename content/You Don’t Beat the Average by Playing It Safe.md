
If you want to gain a substantial advantage over your competitors, you need to do something different.This whole point will be emphasized more by telling you guys more about the startup "Viaweb" .

# **Viaweb**


Viaweb was started by Paul Graham. It focused on rendering websites on the server rather than the client’s computer. This approach removed the dependency on the client-side tech stack, allowing them to use any language they preferred.

# The Blub Paradox

Paul  introduces the Blub paradox that explains that a normal programmer  will not know what features he is missing, since he is thinking the whole software in his own programming language.He won't understand the power of macros or what features he is missing that make software more useful and elegant that can be achieved by adopting some other language.

#  **why Lisp ? why go to some uncharted Land of Lisp?


**Lisp** (short for **LISt Processing**) is one of the oldest high-level programming languages, invented by **John McCarthy** in **1958**.
## Why to use Lisp:
### Macros:
Macros are powerful tools using which you can generate code from code!!
Yes,Generating code from code seems like a weird idea.
```
(defmacro unless (condition body)
  `(if (not ,condition)
       ,body))
```
this block of code may seem just like function ,you take some arguments and you get some value in return but it's different.MAIN difference between function and macros  are that in function all arguments are executed irrespective if you gonna need them or not
for example 
```
function(x>0 ,do_something,do_something_else)
```

In this function all arguments gets executed ,even if you need them or not.
so the ability to control your execution,can introduce new control flow in the program.

If you look at the "unless" Macro it is just if and not combined together this can be achieved in other languages also. 

Things like changing the execution depending on how many time a block of code has run can be done which can't be done naturally in other languages.
In lisp you are transforming code before it runs.

In future I will go more deeply into how lisp is different from other languages.

I’ll dive deeper into these macro patterns—like backtracking, reactive triggers, and coroutines—in upcoming sections, which are difficult to express together in most conventional programming languages without building complex frameworks or interpreters.

Things which are unique to one language can be created in lisp ,that is why Lisp is called language that can create other languages.

so i will summarize Macros.

**Macros are powerful tools that generate and manipulate code in compile time meaning you are writing code in compile time phase** 


### Code as data:



In **Lisp**, code is written using **the same structures** that are used for regular data.
This idea is called **homoiconicity**:
**Homoiconic** means the primary representation of code is also a data structure in the language itself.

So in Lisp:
- Code **is data**
- And data **can be used as code**

In Lisp code and data both are represented using an Abstract Syntax Tree
this allows code to be passed as an argument which introduces the concept of macros since  code is written in Abstract Syntax tree so you don't need a parser to parse your code what you need in other languages.

You don’t need a **separate mechanism** to handle code.  
The **same tools you use for data** — like `car`, `cdr`, `list`, `subst`, `mapcar` —  
can be used to inspect, transform, and generate code.


Example 1: If Statement

AS CODE
```
(if (> x 0)
    (print "positive")
    (print "non-positive"))

```

AS DATA(Quoted list)
```
'(if (> x 0)
      (print "positive")
      (print "non-positive"))

```

The only difference in syntax is the presence of the `'` (quote), which tells Lisp to treat the expression as data rather than executing it.

You can write a macro to transform this, because it’s just a list!

So you can write a function that says:
 “Any time you see `(print "positive")`, replace it with `(display "POS")`.”



# Why is it not so widely used? 

Learning a new programming language is learning new way to think about the solution of the problems.Each programming languages come with their own way
to think which we can call programming paradigm(I will explain programming paradigm more Extensively in my coming blogs).Programming revolution and hardware revolution have not grown at the same rate of growth.It takes time to change habits of mind.

# The Strategic Advantage and Disadvantage

## Advantage

The advantage is your competitor won't understand how you are developing your software so fast.This is evident in Paul's essay when he was talking about his startup days.When They were able to copy competitors features within days only.

(Note - I still have understand to understand more about Lisp what more you can do instead of developing your own domain specific language and building complex dynamic systems fast)

## Disadvantage

It is difficult to find programmers who still use Lisp, since it is the second-oldest high-level programming language still in use today (after Fortran). This makes collaboration with others more challenging.
