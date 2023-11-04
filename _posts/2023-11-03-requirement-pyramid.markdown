---
layout: post
title:  "The Requirement Pyramid: Simplifying Problem-Solving"
date:   2023-11-03 22:00:00 +0100
categories: software management leadership
image:
    path: assets/img/requirement_pyramid.png  
    width: 500
    height: 500
---

<img src="/assets/img/requirement_pyramid.png" alt="The Requirement Pyramid: Simplifying Problem-Solving" style="width:300px;margin-left: 10px; margin-right: auto; float: right;"/>

In the organization you work, have you ever thought about how much the decisions you make cost? Have you ever stopped to calculate the cost of over engineering? Or the cost of developing a solution that doesn't actually solve the problem it was supposed to?

This article introduces the concept of requirement pyramid, showing how to incorporate it to your mental process, to avoid huge unnecessary costs when solving problems. 

The article focus on software development scenarios, but the concept is not limited to that and can be applied to a variety of situations in life.

---
>

## Intro

Once upon a time, there was a very high skilled developer, with knowledge in dozens of technologies and programming languages. 

One day, a prospect customer appeared asking him to quote a software to book appointments and show reminders to her employees. 

The developer quoted a full fledged solution, split into multiple microservices domains, running a very rich and responsive UI in browser and mobile, with alerts, logs, dashboards, admin interface, services running in the cloud and a very nice configuration screen. 

Later on, the customer comes back saying another quote was accepted: someone else had quoted creating a script that would automatically send an email to every employee in the beginning of the day with the daily agenda, solving the problem costing 1% of the price to develop, and less than 1% of the maintenance price.

This scenario is very common and every day, similar scenarios happen across multiple development companies around the world.

Have you ever lived a similar situation?  

## The pyramid

To understand the concept of the requirement pyramid, we must understand what requirements are. First thing to notice is that requirements are very often not the problem you want to solve, but solutions to a higher level problem. 



<img src="/assets/img/requirement_pyramid_new_clothes_scenario.png" alt="New clothes decision option tree" style="width:50%;margin-left: 10px; margin-right: auto; float: right;"/>

For instance, suppose you want to buy new clothes, and you're short on money. Here are some possible solutions for this problem:

- You can find a way of getting more money
- You can stop using clothes and decide to walk naked
- You can use the internet to search for many places selling clothes for you so you can find one that suits your taste for a price you can pay. 

So, in the beginning, you had no requirement, you had a pain, a job to be done - your clothes are bad. That's the top of the pyramid - the original pain. When you decide to solve this pain, you very likely dive into a new set of problems or pains. 

In the example above, suppose you decide you will search the internet to find new clothes to buy. Here are some things you could do:

- You could spend hours searching for new clothes in the most used online store website on internet, that has agreement with multiple clothing vendors
- You could spend hours searching for new clothes in the most used search engine website on internet, enter on each vendor website and search for clothes in there
- You could write a python script that scans a set of stores of your choice, finds the clothes that meet your search requirement and filter by those, generating a report with the best candidates for you to select. 

So, here is the second level of the pyramid - you decide to solve your pain with one of the above solutions, so the chosen solution is your second level of requirements. Just to make things interesting, suppose you chose the python script solution. 

Now in order to get your python script running, you need to install python, set up your environment, and you have many options in there:

- You could use pip and pipenv
- You could use pip and requirements.txt, without a virtual env, installing dependencies system wide
- You could use conda
- You could use docker and install everything on docker, then use docker run

We arrived to the 3rd level of requirements, which is already digging into details on how to implement your solution. You could have even more options, you could decide to filter manually the results in the report, or you could output a spreadsheet that would allow you to filter stuff, etc. 

Finally, you implement your code and run your script. Based on the output, you find the clothes you want, then you buy them, solving your problem. You're at the last level of the requirement pyramid now - the thing that actually solved the original problem. 

Thinking about this example, we followed a branch in the tree of possibilities with the many choices of solutions on every level, and for this branch, the more we approach to the bottom, the more complex things become. It started very simple - you need new clothes. 

The second level was more detailed and the requirements were already more complex - it ended very complex, with more things to consider to make a good decision.

The third level was almost the design of a software. 

Finally, the forth level was the implementation of a running software, that took most effort of all. 

That's how the final pyramid would look like: 


<img src="/assets/img/requirement_pyramid_new_clothes_scenario_chosen.png" alt="New clothes chosen branch" style="width:50%; margin-left: auto; margin-right: auto; display: block;"/>

## Pyramid Properties

- **Simplicity vs. Complexity**: 
  The higher you solve a problem in the pyramid, the simpler the solution is likely to be. Conversely, the closer to the bottom, the more complex the solution becomes.

- **Risk of Over-Engineering**: 
  The more levels your pyramid has, the greater the risk that your solution might not completely fulfil the original need. An extensive pyramid may suggest over-engineering, hinting that there might be a simpler solution closer to the top.

- **Solution Efficacy**: 
  Pyramids with too many levels can overcomplicate the solution, while pyramids with too few levels might indicate that the problem isn't fully addressed, unless a very simple solution is actually adequate.

- **Cost and Effort Considerations**: 
  Complexity can be understood in terms of cost or effort. Aiming to solve problems with the shortest requirement pyramid possible is usually the most efficient approach.


### Are you looking at the top?


<img src="/assets/img/requirement_pyramid_bigorg.png" alt="New clothes decision option tree" style="width:60%;margin-left: 10px; margin-right: auto; float: right;"/>

In real life, we receive requirements all the time, from a variety of people. The bigger the organization is, the farther you probably are from the original need, and the less vision you might have of the original pain that causes your salary to be paid. 

When a task is assigned to you, it's always good to question yourself whether you're looking at the top of the pyramid or what the top of the pyramid is. Some times, the top most requirement you are able to see is a pain being solved, but if you dive deeper, you figure out you're looking at a sub-tree of the bigger decision tree above. 

For example, suppose at the top of the pyramid you see, you see the need of a catalogue listing all the microservices that exist in the company you work, as you have the pain of needing a service and you can't easily find the one you need, because you don't have a list, and you're often having to speak to every one in the company to find the service you can use. 

This looks like a top level pain at the beginning, but when you ask yourself why you need to find that service, you see you're not looking at the top. 

It's essential to consider this in practice, as if you don't question why, you could be missing opportunities for simplifying solutions. Some times, and I can say this from experience, the whole project you're working on might not be needed, and you could be spending your time to cause a bigger impact.

### Are you looking at the bottom?

Imagine that, instead of creating a python script, you were using AI to find the clothes for you. Or you were using an existing tool for that. 

The overall complexity of the whole solution would still be bigger (AI is such a complicated tool, for example), but the cost might not be, as as someone else could be taking responsibility for the complexity of the tool you're using. 

Using existing tools instead of reinventing the wheel can make your cost smaller and your effective requirement pyramid smaller

Be aware that using external tools will make your solution **easier**, but not necessarily **simpler**. For a more detailed deep dive on these terms, I recommend the great talk from Rich Hickey, the creator of Clojure language, [Simple Made Easy](https://www.youtube.com/watch?v=SxdOUGdseq4).



### Understanding Your Position in the Pyramid

The level of the pyramid you occupy is not just about your role; it's also influenced by the type of company you work for. Startups may find that roles are less defined and more fluid, with individuals covering multiple layers of the pyramid. In contrast, larger companies tend to have more defined roles and clearer separations between layers.

- **Startups**: If you're in a startup, you might be wearing multiple hats, covering tasks from strategic market alignment using the [Jobs to be Done](https://example.com/jobs-to-be-done) framework (there is also a [book](https://www.amazon.co.uk/Jobs-Be-Done-Customer-Centered-Innovation/dp/0814438032)), down to the nitty-gritty of feature implementation. Agility and adaptability are your allies here.

- **Larger Companies**: In a more established company, your position in the pyramid likely aligns with a specific set of responsibilities. Leaders focus on market needs and strategy, while individual contributors tackle the execution details within a defined scope (specific levels in the pyramid).

- **Accountability and Communication**: Regardless of company size, know what you're accountable for, and maintain clear communication channels. This is crucial to ensure that the company's strategies are well-informed and its operations remain efficient.

Thinking about the pyramid is useful for the managers, because by having clarity on the pyramid they can see how their levels of responsibility are being solved, so they can easily spot when cost was assigned to solve a problem, but in practice it's going to a direction it won't solve it. 

For the engineers and people responsible for the bottom layers, it can be useful to see layers above, so the solution is focused on the problems that exist, without trying to over engineer and solve problems you don't have. It also can help you to know when to escalate when you're solving a problem in the last layer, but you see a better way of solving it in a layer above. 

By understanding your role within the requirement pyramid—factoring in the size and nature of your company—you can better align your work with the overarching goals of your organization.



## Practical Applications and Steps

Implementing the Requirement Pyramid framework in your workflow can streamline decision-making and ensure resources are optimally allocated. Here are steps to incorporate it effectively:

1. **Map Out the Pyramid**:
   - Clearly delineate each layer of the pyramid specific to your project.
   - Place the core problem at the top and arrange secondary issues accordingly.

2. **Align with the Core Issue**:
   - Regularly refer back to the top of the pyramid when making decisions.
   - Use the pyramid as a visual aid in design and strategy meetings for alignment.

3. **Leverage Existing Solutions**:
   - Before building a custom solution, explore if existing tools can meet your needs.
   - Weigh the complexity that each tool brings against its benefits.

4. **Maintain Big-Picture Awareness**:
   - Ensure that every team member understands their role concerning the pyramid.
   - Promote a culture of checking if tasks are directed toward solving the core issue or merely a symptom.

5. **Document and Communicate**:
   - Keep a well-maintained documentation of the pyramid and the rationale behind chosen solutions.
   - Foster clear communication around how each part of the solution addresses a specific layer of the pyramid.

By regularly revisiting and refining the Requirement Pyramid, you can make more informed decisions, prioritize effectively, and ensure that your efforts are contributing to a meaningful resolution of the core problem.
