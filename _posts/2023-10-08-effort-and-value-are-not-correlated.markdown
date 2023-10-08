---
layout: post
title:  "Effort and value are not correlated"
date:   2023-10-08 23:00:00 +0100
categories: software management leadership
image:
    path: /assets/img/correlation.jpeg    
    width: 500
    height: 500
---
Economic theory says that we must increase interest rates in order to get more people in the market, so country productivity numbers can improve. The idea is that with less money or needing money more, people will feel "motivated" to go back to the market and work more for money, thus generating more richness (value, in this context), that can be spread across the whole population.

If the amount of value we produce through products and services is bigger, we should have more value produced and money power would be bigger. 

> Note: This is actually production, not productivity, but without diving deeper in the details, a bigger production for a nation affects its productivity, as the amount of people in the nation is constant and a bigger production implies bigger productivity.

But when we look at the micro level, is this actually happening? Does it work as supposed? 

Keep reading to find out my ideas about.

---
>


Once upon a time, there was a rich guy, who hired 100 people paying 100 pounds per day. He ordered everyone to dig a hole in the ground, for 1 month (30 days). 1 month later, he had a huge hole of the size of a football field, and he put that hole for sale for 300.000 pounds. When confronted about what would people do with the hole, he argued that he had paid 100 people paying 100 pounds per day for 30 days, totalling 100 * 100 * 30 = 300.000 pounds, so that's what the hole was worth.

That may sound like a small or ridiculous thing to many people, but the idea described above is many times adopted by many unconsciously, as it might be part of a mental model transmitted through culture over time.

That apparently inoffensive idea can greatly affect everyone's quality of life. I remember how it was working 13 hours a day when I had this routine in my life, it affected my health and stress a lot. Many people I know embrace that life style and religiously think that labour is good for the human being and the more people work, the merrier. But when after living other work experiences when I was seeing better results while working the half, I started questioning that more strongly.

Years ago, I was once working on a company, where everyone used to work 13 hours per day, some times also on weekends. All people working there were very smart and capable, and even so, we were struggling to deliver working software that would allow us to advance more quickly. 

Years later, I was working on another company, where the team was never deploying software on Fridays, nobody was working more than 7 hours a day, and surprisingly, we were generating a huge amount of value every sprint, and the manager got promoted as consequence.

Have you lived something similar in your work experience?

What were the main differences between these 2 situations? 

Let's brainstorm on these scenarios, checking what was different between the 2 team set ups to compare how much each factor can affect the production output of a software development team.  

In this article, I list 3 factors: tools, the way the team works and mastery. After discussing each of these points, I discuss what we can change our mental model to and what practical actions we can take to be closer to the second example.

## Tools

I think this is specially relevant nowadays, given everyone is talking about AI and how it could replace human beings. I don't think AI will replace human beings so soon (not in the next 50 years), but I definitely can see *tools* based on AI increasing our production output a lot. 

Using the right set of tools can definitely affect the amount you produce, and the trade-offs become hard when the tools that could improve your work still don't exist in the market. 

As a very simple example, let's imagine for a second the time were you had to code in assembly to write some software. From that time to now, the market has created different languages, paradigms of programming, frameworks, that affect the amount of code we have to write to get modern software working. 

Now, can you imagine, for a second, what would happen if we instead had tried to write modern software we know today in assembly, just by putting more effort to it, instead of trying to find new tools to help us improve the productivity? 

We can't check for sure the numbers, unfortunately, because it's impossible to measure this, but I imagine that for writing a software like Microsoft Word, for instance, fully in assembly, you would take... 100.000 hours of software engineers effort? Of course this would depend on the techniques employed, how much reuse they would get, how they would test each part of the software, etc. But looking at this extreme example, if you had 100.000 hours of software engineers available and you could decide between:

- Writing Word from scratch, entirely in assembly, without frameworks
- Writing tools like compilers for a new language, libraries and frameworks, then using those to write the same software

Which option would you choose? 

Consider not only the amount of hours, but that software is something you actually change over time. How many lines of code would you have to change, in assembly, to change a button that appears in multiple places? 

I hope by thinking in similar extreme examples like this, it becomes obvious to you, as much as it becomes to me, that tools are essential for our job. I have no doubt I would choose to develop the tools first, and then to write the software. Write it entirely in assembly could even be possible and have a similar amount of hours in the short term, but in the long run, you would spend much much more on every modification.

### Using too many tools can be worse

Now let's think on the opposite example - you want to write a kernel driver for a new device that you created and that will communicate with the operating system by USB. Can you imagine trying to create the kernel driver using C#? 

Trying to use a high level language for something that needs such a low level hardware dependent access would require way more effort than using assembly directly, keeping it simple. Imagine the amount of software you would require to be able to glue the output of C# byte compiled code with the kernel code...

So, it's not about saying that using tools improve productivity - using the wrong tools can *decrease* your productivity instead. The secret is choosing the **right one**.

> Using the best tool for the job is an essential factor to increase productivity.

### But what if the best tool doesn't exist yet?

This is very common is some big companies I worked in the past, as well as some very innovative ones, where they had a need that nobody else had in the market before, and you then realize that a specific tool would boost productivity a lot, but it doesn't exist yet. 

In this situation, you start considering trade-offs, you could be in a scenario where going without a tool would make you reach your goals faster, but after you reach your goal you're not productive to maintain or pivot what you built. That might still be worth though, depending on the business benefit you get from reaching your goes faster. 

It could be the case it's better to develop a tool in parallel while you progress. Or it could be the case it's better to create the tool first and then do the business work that will contribute to value, or it could still be the case you have to iteratively create tools as you go. 

> The best tool for the job short term might not be the best tool for the job long term

In all cases, we're talking about another productivity factor, orthogonal to tools now: the way you work and how you prioritise the backlog.

## The way you work as a team

The worst enemy of productivity, IMHO, is over engineering. Over engineering can be so bad, that a bad decision can just cause your project to fail, as although it might still be possible to overcome it, it turned the cost of going ahead so big that it's not worth it any more. 

To have good productivity, it's essential to work on a way where you do not over engineer, and the decisions you make on prioritization of tasks, as explained in the prior section, can also affect it by a large amount. 

Let's again consider 2 scenarios, one where you do everything wrong and other where you do everything right, and compare the effort estimates. Imagine you're on a project to build a billing system.

### The bad way 

In scenario A the team over engineer a lot: they first split the billing system in 3 micro services, and as the project advances they realize that was not what they needed, the domains should have been split in a different way. 

The team built a library upfront to automate configuration, as configuring it manually was painful, so a library would save work. In practice, it was a wrapper over configs and when things didn't work, they had to dig into a badly written library, released before it was really ready, and after 1 year that library entered the deprecation path, and the team was discussing in every sprint when they would deprecate that and replace it by a new one. 

Then they built a new one and, after another year, that one was also in the deprecation path, because they rewrote the software, but made the same mistake in the way of working again. 

The team had also some understanding of requirements upfront, and they developed the software based on their understandings, but the requirements kept changing over time and this was not only affecting productivity, but also stressing software engineers, who were dedicating so much effort to fulfil the requirements perfectly, to get frustrated to see changing requirements over and over again, figuring out a good part of what they built was designed for something else and it was perfect for the requirements they imagined, but now it looked like many parts could be thrown away.

Does it sound familiar to you? It's impressive how many times I have seen the same kind of scenarios in practice, along my career. 

### The good way

In scenario B, none of these mistakes happened. The team didn't work for requirements, they worked from the pain of customers, and instead of figuring out complex solutions to advanced problems, they often implemented workarounds and very simple solutions that would solve the pain and, although might not be perfect or ideal from one point of view, they were low cost and easy to maintain. 

This team evaluated correctly trade-offs between creating technical debt and delivering useful stuff, and they would often deliver business value on every sprint, learning new things during each sprint that would avoid errors in the next one. 

Do you want to know more? Please keep following the blog and other articles, I will very soon post more articles about this subject in specific on this blog.

### The comparison

I would LOVE to have data to show you when comparing A and B, but it's not the kind of data easy to get. All I can tell you is that, in my personal experience, this is how the production output looks like, over time:

![Difference of productivity](/assets/img/bad_good_productivity.png)

So, initially, the productivity difference is not so apparent, but when the way of work is different, it can exponentially affect productivity over time, and the reason is that there is much less **waste**. That's why all agile methodologies are based on that - eliminating **waste**, like over engineering, guessing requirements instead of understanding the pain to be solved, and bad prioritization decisions in general. 

> Making good decisions and eliminating waste affects productivity exponentially in the long run
 

## Mastery of team members

Another factor that can affect productivity a lot is how good and independent the member of your team are. This is far from obvious, as most of the times this isn't easily measurable - don't expect that a senior team member will produce 10 times what a junior team member, that costs way less.  Very often, what you see is exactly the opposite, the more experience the software engineer is, the less you see lines of code from him/her. 

That said, having more experienced people in a team affects, among other things:
- prioritization - which can affect productivity
- risks - that often you only see because of experience
- trade-offs in technical design and in what tools to use / develop - which we already saw below that affect productivity
- the productivity of less experienced team members, reducing their waste
- business throughput - this is the harder to achieve, I think, and the most valuable one, it's when you don't affect productivity by reducing the waste or cost, but by increasing the value generated by the software you created. One interesting idea easy to implement can some times pay off years of development, all of a sudden.

The exception to this rule, is when people are experienced in doing things wrong. I know many people in the market who have years of experience in a subject, and they start thinking that is the only possible and correct approach.

Maybe the correct term here is mastery - which involves experience, but also humility and being open to new ideas, scientific knowledge, among many other factors hard to define. The fact is - don't under estimate the difference that hiring better people can make in your team - trying to hire the "less expensive" professional that suffices for a role is something that usually plays *against* productivity, and not in favour of it.

> Good engineers increase team productivity indirectly in many ways that are hard to measure

## Conclusion

I hope this article made you stop to think in things you never have time to. 

The key lesson to take here is that working more is not the main factor that can affect productivity. Even if every team member works 6 days in the week instead of 5, the output value you're supposed to generate will increase by less than 20% max. If you work much more, but make bad decisions in the middle, it's more likely your productivity will even decrease instead of increasing. 

I have lived that in practice across many different jobs I had in my career. Factors as way of working, focus of the team on the right things, good decisions in general, these things usually affect productivity much more than increased effort, and usually the effect over time is exponential instead of linear, while you can only increase effort linearly. 

So, here is what we can do, in practice, to actually increase productivity:

- Work in a way that eliminates waste of effort
- Focus on business value, not implementing software that perfectly fulfil requirements
- Hire good engineers - consider mastery when evaluating different engineers in the market - do not focus on hiring only the cheapest that you can
- Make good trade-off prioritization decisions or make sure whoever is accountable for such decisions are doing a good job and has everything needed to make such decisions
- Use the best tools for the job, considering that some times the best tool short term might not be the best tool long term
- Make over engineering your worst enemy, as it's one of the most expensive forms of waste

> Stop with the effort mental model - working hard affects productivity linearly, while working smart affects productivity exponentially. 

Hopefully, this article contributed to change or confirm your mental model towards this subject. 

I also hope that, next time someone tells you that productivity is low and therefore people must work more, you remember the ideas in this article - are your leaders being smart and pursuing business value? Or are them blindly pursuing effort, thinking the 2 things are the same?

Keep following the blog for more related articles in the future.


