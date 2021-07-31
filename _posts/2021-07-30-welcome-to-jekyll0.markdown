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
In this program
**/

{% endhighlight %}

For part A we will be using n and k in the program for n and k for binomial coefficient's. We use 4 since there's two teams it would be the first to four is the winner. After plugging in 7 and 4 we end up with 35.

For part B however we need to consider how the 6th game can happen if Team A wins the very last game. Since this is the case all we need to do is subtract 1 from the total number of games since we know how one game will end. We also need to consider how many games actually need to be won so we subtract 1 from 3 since team A already won one game. Meaning n will be 6 and k will be 3.

{% highlight ruby %}
/**
Name: Raymond Bell
In this program we can change n and k in a binomial equation which is typically n! over k!
**/

{% endhighlight %}

Finally for part C we follow the exact same process! since the tournament is only 6 games and team A won the last one we use 5 for n this time and 3 for k(since only 3 games need to be won for a win). Giving us 10 possibilities.

{% highlight ruby %}
/**
Name: Raymond Bell
In this program we can change n and k in a binomial equation which is typically n! over k!
**/

}

{% endhighlight %}

If the tournament goes lower however this would mean that team A either won or won all games since the won the last match. They would win because team B never could stop them from winning thus the last match had happened.
