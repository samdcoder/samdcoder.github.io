---
title: "Lets Go!"
layout: post
date: 2019-04-05
headerImage: true
category: blog
description: My experience with Go!
---


<img src="https://cdn-images-1.medium.com/max/1600/1*vHUiXvBE0p0fLRwFHZuAYw.gif"/>


It'd been a while since I had learnt or tried any new programming language. The last programming language I learnt was Python which was over 2.5 years ago! Python started out as a hobby to hack around with some cool scripts to automate tasks.

These days I primarily work with JavaScript/Node.js along with Python.

Last weekend I decided to try the Google's famous programming lanugage Go!

<img src="https://media.giphy.com/media/KGVgi2nOVkCoE/giphy.gif"/>

Go has been built for scale and is expected to be a very strong choice in enterprise space in near future! Being a compiled language it really out performs popular interpreted languages such as Python and JavaScript which are heavily used in backend development.

Go could be a good alternative to the above programming languages especially if your application requires high computation on the backend. It brings out the accuracy of statically typed languages and ease of dynamically typed languages.

I roughly spent 15 hours on learning Go in 1 week and wrote about 15-20 small programs experimenting with the basic syntax of the language such as data types, conditions, functions, looping along with some data structures like slices, maps, etc.

I started with sentdex's tutorials and watched about 12-14 video lectures. I then refered to the famous Go blog
gobyexample.com to look up at examples and play around with them on my own. I also watched a 1 hour YouTube video on the language explaining all the basic concepts quickly.

Learning syntax is important but not enough to really understand a programming language. I am a strong believer in learning by doing. So I decided to build some simple applications using Go to improve my understanding of the language.

I built some simple web services using it such as a simple echo server, services interacting with Google APIs to
return some search results to the user in JSON format, etc.

My overall experience with the language was very solid. As I have used C and C++ extensively (for 4-5 years) in past for competitive programming and for solving problems on algorithms and data structures, I could quickly grasp the basic syntax in a couple of hours.


<h4> A few things that struck me as unique/different/amazing about Go are: </h4>

1) If there are any unused imports or variables, your program won't run. This is a good practice from software quality
point of view but could be really annoying if you are quickly trying to hack some programs!
<hr>
2) Go feels more restrictive overall and strict about the style/pattern with which you write code. For example: You cannot write else or else if
on new lines, they need to adhere to the coding style recommended by Google/Go.
<hr>
3) It might take some time to wrap your head around a few things at first, for example here is a code in Go to initialize an array of size 5 with numbers 1 to 5.
{% highlight go %}
b := [5]int{1, 2, 3, 4, 5}
{% endhighlight go %}

We use := if we are initializing and declaring a variable at the same time.

It is much more intuitive in C++ with:
{% highlight c++ %}
int b[5] = {1,2,3,4,5};
{% endhighlight c++ %}



It's easier to understand such things if you look at them through generic ways like:

**`<name> := [<size>] <data_type> {values1, value2}`**
<hr>
4) You can create functions in Go that can return multiple values which is not possible in most of the programming languages.

{% highlight go %}
func vals() (int, int) {
    return 3, 7
}
{% endhighlight go %}
Here function vals returns 2 integers.

<hr>
5) You can create functions in Go that can accept any number of arguments. These functions are called variadic functions.

<h4> Example of Variadic functions </h4>

{% highlight go %}
func sum(nums ...int) {
  fmt.Print(nums, " ")
  total := 0
  for _ , num := range nums {
      total += num
  }
  fmt.Println(total)
}
{% endhighlight go %}

We can call the above function with any number of arguments (numbers) & it will print the total sum of all the values.
<hr>
6) Go feels incredibly simple to learn, especially if you come from C/C++ background. It's like C and Python decided to have a baby. It's simplicity can be naively demonstrated by its list of keywords.

<h4> List of all the keywords in Go</h4>

<img src="https://image.slidesharecdn.com/golang101-170327030632/95/golang-101-concurrency-vs-parallelism-36-638.jpg?cb=149058419"/>
Compare this with something like Java which is a widely used language in enterprise space & you will get an idea.

<h4> List of all the keywords in Java</h4>

<img src="https://www.oreilly.com/library/view/oca-java-se/9781259587535/t0496-01.jpg" />

Obviously the comparison isn't completely fair as Go has been around just for a decade now and Java for a much more longer time. With new revisions, Java added features & keywords but it still gives us a rough idea about the gentle learning curve for Go.
<hr>
7) Goroutines make it possible to write non blocking code in synchronous manner. This is a huge advantage as you do not have to deal with things like callback, callback hell, etc which are available in programming languages like JavaScript. The Go runtime handles these things for you efficiently. Go being designed to be used internally at Google has managed to handle concurrency in a very efficient way.

Link to Github Repository of some Go programs: <a href="https://github.com/samdcoder/Go-Programs"> Go Programs</a>
