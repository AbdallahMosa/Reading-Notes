# Read 1 
## Big O Notation
### What is Big-O Notation?
To put it generally Big-O Notation is a simplified way to analyze how efficient the algorithm is. It doesn't do it based on the computer you're running the code on, it's based on the computational steps in your algorithm and the complexity in terms of the input size. It accounts for both how efficient the algorithm is not only in terms of time but also in terms of the amount of memory it takes to process.

1. There are two general rules when it comes to how you represent the tier of Big-O notation your code runs at. One is we always declare it at the highest order of term it runs at. The tiers in order are: 
O(1) < O(logn) < O(n) < O(nlogn) < O(n^2) < 0(2^n) < O(n!)
1. Another rule when it comes to syntax is we don't declare any constants. So even if you have 2n in your computation we will still declare it as O(n) not O(2n). The reason behind that is Big O is an analysis of your codes efficiency in terms of super large scales so that constant becomes negligible compared to say an exponent.


![Big O](https://res.cloudinary.com/practicaldev/image/fetch/s--UvbynQ9T--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/ya7xk4n9ch50xgwibt9t.png)

https://dev.to/eidorianavi/an-introduction-to-big-o-notation-424e

## Facts and myths about Python names and values

As in many programming languages, a Python assignment statement associates a symbolic name on the left-hand side with a value on the right-hand side. In Python, we say that names refer to values, or a name is a reference to a value:

x = 23

### Facts :- 
1. Fact: Many names can refer to one value.
1. Fact: Names are reassigned independently of other names.
1. Fact: Values live until nothing references them.
1. Fact: Assignment never copies data.
1. Fact: Changes in a value are visible through all of its names. (Mutable Presto-Chango) 


## Sources 
 1. [Big O Notation](https://dev.to/eidorianavi/an-introduction-to-big-o-notation-424e)
1. [Facts and myths about Python names and values](https://nedbatchelder.com/text/names.html)
