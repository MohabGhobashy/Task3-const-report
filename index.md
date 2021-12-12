<h1 style="margin-left: 150px">*const* uses in c++</h1>
<p style="font-size:18px ">1-The const keyword specifies that a variable's value is constant
and tells the compiler to prevent the programmer from 
giving variable another value</p>
<p style="color: blue">Example<br>int main() {

const int i=10;<br>
const int j=i+10; // works fine<br>
i++; // run time error


} </p>
<hr > 
<p style="font-size:18px "> 2-you can use the const keyword instead of the <span style="color:blue">#define</span>
to define constant values and with it
, you can specify the size of an array with a const variable</p>
<span style="color: blue">Example </span>
<p> 
const int max_array = 255; <br>
char store_char[max_array];     // allowed in C++; not allowed in C</p>
<hr > 

<p style="font-size:18px ">3-We can use ‘const’ keyword with pointers too. It can be used in <span style="color: blue">two possible ways:</span></p>

<h3>We can make a pointer constant at time of declaration:-<br></h3>
<h4 style="color:green">A constant pointer to
a variable is useful when you want a storage that can change the value but cannot be moved in memory</h4>
<span style="color:blue;" > Example:-</span>
<p> int x=1;<br>
int* const w=&x;
</p>

<h3>We can make the value constant to what the pointer is pointing to:-</h3>
<h4 style="color:green"> 1-This means that the pointer is pointing to a const variable.</h4>



<h4  style="color:green"> 2- Pointers to a const variable is very useful, as this can be used to make any string or array  cannot be changed</h4>
<span style="color: blue"> Example:-</span>
<p>const int value{ 5 }; // value is const <br>
int* ptr{ &value }; // compile error: cannot convert const int* to int*<br>
*ptr = 6; // change value to 6</p>
<hr>
<p style="font-size:18px ">4- const Function Arguments and Return types:-</p>
<a href="https://ibb.co/DMcvWs6"><img src="https://i.ibb.co/094628W/sooooooo.jpg" alt="sooooooo" border="0"></a><br /><a target='_blank' href='https://nonprofitlight.com/tn/nashville/nashville-christian-schools-inc'>nashville christian school</a><br />

<h4 style="color:green">We can use the const keyword with the arguments of a function. If an argument is declared as const then the function will not be allowed to change its value.When a function is declared as const, it can be called on any type of object. Non-const functions can only be called by non-const objects. </h4>

<hr>
<p style="font-size:18px ">5-Constant Objects of a Class:-</p>
<h4  style="color:green"> If we declare an object of class as const then the values of data members cannot be changed later on. If we try to change the values of data members then compiler will generate an error,The const attribute of the object takes effect after the constructor finishes executing, and ends before the destructor of the class executes. So the constructor and destructor can modify the data members of the object, but the other methods of the class cannot</h4> <hr><hr>
<h1 style="margin-left: 150px">*&* uses in c++</h1>
<p style="font-size:18px ">1-Bitwise AND Operator :-</p>
<h4 style="color:green"> The bitwise AND & operator returns 1 if and only if both the operands are 1.
Otherwise, it returns 0.</h4><hr> 
<p style="font-size:18px ">2-declaring a reference to a type :-</p>
 <h4 style="color:green"> If you use & in the left-hand side of a variable declaration, it means that you expect to have a reference to the declared type. It can be used in any type of declarations </h4>
<span style="color: blue"> example:</span> <br>
<p> string& theBoss = Mohab;</p> 

<span style="color: blue"> note:</span>
<p> This doesn't just mean that both Mohab and theBoss will have the same value, but they will actually point to the same place in the memory</p><hr>
<p style="font-size:18px ">3- geting the address of a variable :-</p>
 
<h4 style="color:green"> When using it on the right-hand side of a variable, it's also known as the "address-of operator",it'll return its address in the memory instead of the variable's value itself. It is useful for pointer declarations.  </h4>
<span style="color: blue">example </span>
<p>string Mohab("Andy");<br><br>
std::string* theBoss;

theBoss = &Mohab;
</p><hr>
<p style="font-size:18px ">  4-Use & or && for function overloading:-</p>
<h4>you can use both the single and double ampersands as part of the function signature, but not part of the parameter list for
overloading</h4>
<span style="color: blue"> Example:- </span>
<p>
void Mohab() &;<br> 
void Mohab() &&;<br>
auto Mohab() & -> int;<br>
auto Mohab() && -> int;
</p>
<p> What this means is that you can limit the use of a member function based on whether *this is a lvalue or an rvalue</p>

<hr>
<p style="font-size:18px "> 5- && in a conditional expression;-</p>
<h4> && in a (logical) expression is just the C-style way to say "and"</h4>
