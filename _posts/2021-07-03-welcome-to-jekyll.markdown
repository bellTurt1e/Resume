---
layout: post
title:  "Worked out problem!"
date:   2021-07-01 04:47:35 -0700
categories: jekyll update
---
Problem (Using C++):
{% highlight ruby %}
The Stanley Cup is decided in a best of 7 tournament between two teams. In how many ways can your team win? Let's answer this question two ways:

  A. How many of the 7 games does your team need to win? How many ways can this happen?

  B. What if the tournament goes all 7 games? So you win the last game. How many ways can the first 6 games go down?

  C. What if the tournament goes just 6 games? How many ways can this happen? What about 5 games? 4 games?
{% endhighlight %}

`Program`
{% highlight ruby %}
/**
Name: Raymond Bell
In this program we can change n and k in a binomial equation which is typically n! over k!
**/
#include <iostream>
using namespace std;
int binomial(int n, int k);
int main()
{
    int n = 7, k = 4;
    cout << "C(" << n << ", " << k << ") = " << binomial(n, k);
    return 0;
}
int binomial(int n, int k)
{
    if (k > n)
        return 0;
    if (k == 0 || k == n)
        return 1;
    return binomial(n - 1, k - 1) + binomial(n - 1, k);
}
{% endhighlight %}

For part A we will be using n and k in the program for n and k for binomial coefficient's. We use 4 since there's two teams it would be the first to four is the winner. After plugging in 7 and 4 we end up with 35.

For part B however we need to consider how the 6th game can happen if Team A wins the very last game. Since this is the case all we need to do is subtract 1 from the total number of games since we know how one game will end. We also need to consider how many games actually need to be won so we subtract 1 from 3 since team A already won one game. Meaning n will be 6 and k will be 3.

{% highlight ruby %}
/**
Name: Raymond Bell
In this program we can change n and k in a binomial equation which is typically n! over k!
**/
#include <iostream>
using namespace std;
int binomial(int n, int k);
int main()
{
    int n = 6, k = 3;
    cout << "C(" << n << ", " << k << ") = " << binomial(n, k);
    return 0;
}
int binomial(int n, int k)
{
    if (k > n)
        return 0;
    if (k == 0 || k == n)
        return 1;
    return binomial(n - 1, k - 1) + binomial(n - 1, k);
}

{% endhighlight %}

Finally for part C we follow the exact same process! since the tournament is only 6 games and team A won the last one we use 5 for n this time and 3 for k(since only 3 games need to be won for a win). Giving us 10 possibilities.

{% highlight ruby %}
/**
Name: Raymond Bell
In this program we can change n and k in a binomial equation which is typically n! over k!
**/
#include <iostream>
using namespace std;
int binomial(int n, int k);
int main()
{
    int n = 5, k = 3;
    cout << "C(" << n << ", " << k << ") = " << binomial(n, k);
    return 0;
}
int binomial(int n, int k)
{
    if (k > n)
        return 0;
    if (k == 0 || k == n)
        return 1;
    return binomial(n - 1, k - 1) + binomial(n - 1, k);
}

{% endhighlight %}

If the tournament goes lower however this would mean that team A either won or won all games since the won the last match. They would win because team B never could stop them from winning thus the last match had happened.
