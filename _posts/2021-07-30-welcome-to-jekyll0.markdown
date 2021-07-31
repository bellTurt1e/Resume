---
layout: post
title:  "Arithmetic and Geometric Sequences"
date:   2021-07-28 09:47:35 -0700
categories: jekyll update
---
Problem (Using C++):
{% highlight ruby %}
1. Suppose that the candy machine currently holds exactly 650 Skittles, and every time someone inserts a quarter, exactly 7 Skittles come out of the machine.

  A. How many Skittles will be left in the machine after 20 quarters have been inserted?

  B. Will there ever be exactly zero Skittles left in the machine? Explain.

2. What if the candy machine gives 7 Skittles to the first customer who put in a quarter, 10 to the second, 13 to the third, 16 to the fourth, etc. How many Skittles has the machine given out after 20 quarters are put into the machine?

3. Now, what if the machine gives 4 Skittles to the first customer, 7 to the second, 12 to the third, 19 to the fourth, etc. How many Skittles has the machine given out after 20 quarters are put into the machine?
{% endhighlight %}

`Program`
{% highlight ruby %}
/**
Name: Raymond Bell
In this program we use a do-while loop to show we will never end up with 0 skittles. The end result is -1 since we end up with 6 skittles remaining before we're close to 0.
**/
#include<iostream>
using namespace std;

int main() {
    int skittles = 650, amount = 7;    
   do {
       skittles =  skittles - amount;
       cout << "Amount of skittles remaining " << skittles << endl;
   } while(skittles >= 0);
}


{% endhighlight %}

For part A we actually dont need to program anything however we will include it. All we need to do is multiply 20 by 7 since the machine drops 7 skittles for every 20 quarters(7 * 20 = 140). Now we take that 140 skittles and subtract that from 650 giving us 510 skittles after 20 quarters are put in.

For part B we can actually start programming! now we can do two things to prove the same thing. We can divide 650 by 7 (650 / 7 = 92.8...) notice how we have a decimal. This decimal indicates we will never have 0 skittles. Now we can show this using division OR we can use a do-while loop to show its impossible.

{% highlight ruby %}
/**
Name: Raymond Bell
In this program we can change n and k in a binomial equation which is typically n! over k!
**/
#include<iostream>
using namespace std;

int main() {
    int  amount = 7, i = 0;    
   do {
       if(i != 0)
       {
         amount = amount + 3;
       }
       i++;
       cout << "Amount of quarters " << i <<  endl;
       cout << "Number of skittles given " << amount << endl;
       cout << endl;
   } while(i <= 19);
}
{% endhighlight %}

Finally for the second portion we can still use a do-while loop to accomplish the same goal! Since we start off with the machine giving 7 skittles then 10 then 13 we notice how the amount goes up by 3 every time a quarter is put in. So this do-while loop adds 3 to the number of skittles dropped each time its ran through. Each time a quarter is put through the machine the program will show the amount of quarters put in so far and the number of skittles given. So the machine will give 64 skittles at 20 quarters. This is actually an Arithmetic problem can could simply be represented by the equation an = a + (n - 1)d and after plugging in the numbers given the equation turns into  7 + (20 - 1)3 = 64.  

{% highlight ruby %}
/**
Name: Raymond Bell
In this program we can change n and k in a binomial equation which is typically n! over k!
**/
#include<iostream>
using namespace std;

int main() {
    int  amount = 4, more = 3 ,i = 0;    
   do {
       if(i == 0)
       {
           cout << "Number of skittles given " << amount << endl;
           cout << endl;
       }
       if(i != 0)
       {
            more = more + 2;
            amount = amount + more;
       }
       else {

           amount = amount + more;
       }

       i++;
       cout << "Number of skittles given " << amount << endl;
       cout << endl;
   } while(i <= 18);
    cout << "The total number of skittles given at 20 quarters is: " << amount << endl;
}
}

{% endhighlight %}

For the Final part of the question we actually have to add 3 to the amount changed each time a new customer comes. For example customer 1 gets 4 skittles, customer 2 gets 7, and customer 3 gets 12 notice how the amount given is rising by the previous amount gained added by 2. In the program you'll notice this amount is the integer more. More increases the amount of skittles each customer gets by itself added by two for each customer.
