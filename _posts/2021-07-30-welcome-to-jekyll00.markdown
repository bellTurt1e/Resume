---
layout: post
title:  "Truth Value of Molecular Statement "
date:   2021-08-09 05:52:45 -0700
categories: jekyll update
---
Problem (Using C++):
{% highlight ruby %}
You stumble upon two trolls playing Stratego®. They tell you:
  Troll 1: If we are cousins, then we are both knaves.

  Troll 2: We are cousins or we are both knaves.

Could both trolls be knights? Recall that all trolls are either always-truth-telling knights or always-lying knaves.
{% endhighlight %}

`Program`
{% highlight ruby %}
/**
Name: Raymond Bell

**/
/******************************************************************************

You stumble upon two trolls playing Stratego®. They tell you:
  Troll 1: If we are cousins, then we are both knaves.

  Troll 2: We are cousins or we are both knaves.

Could both trolls be knights? Recall that all trolls are either always-truth-telling knights or always-lying knaves.
*******************************************************************************/

#include <iostream>
#include <ostream>
using namespace std;
//These two functions just bold text they're helpful in this case for organization.
ostream& bold_on(ostream& os)
{
    return os << "\e[1m";
}

ostream& bold_off(ostream& os)
{
    return os << "\e[0m";
}
void space()
{
    for(int i = 0; i <=3; i++)
        cout <<endl;
}

int main()
{
    bool a,b,c,d;
    cout << bold_on << "Instance 1" << bold_off << endl;
    cout << "If we are cousins, then we are both knaves." << endl << endl;
    a = false;
    b = true;
    cout << "Troll 2: We are cousins or we are both knaves." << endl << endl;
    c = true;
    d = false;

    if(a == false && b == true)
    {
        cout << "Troll 1 confirmed they're not cousins" << endl;
    }
    if(c == true && d == false)
    {
        cout << "Troll 2 can't be telling the truth because we've confirmed that troll 1 is telling the turuth meaning troll 2 isn't a truth telling knight!" << endl;
    }
    space();
    cout << bold_on << "Instance 2" << bold_off << endl;
    cout << "For instance two we can assume troll 1 to be lying! Meaning we can infer that he's indeed lying. This however invalidates his statement... meaning they're not cousins but their knaves" << endl;
    cout << "Troll 2 is a lying knave since they're not cousins... So they're not knights" << endl;

    /**
    For trolls 1's case we will use a and b vs troll 2 we will use c and d
    **/

    return 0;
}

In this program we essentially run through the problem if an if statement that's some what like a truth table. We have two scenarios that can play out one either troll 1 is telling the truth and they're not cousins and troll 2 is lying meaning troll 2 isn't a truth telling knight. Where as in the second scenario They're both lying and both knaves which would intel that they're cousins but not knaves according to troll 1. Then troll 2 is lying since they're not cousins.  
