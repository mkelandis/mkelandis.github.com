---
layout: post
title: "Managing Technical Debt"
description: "Managing Technical Debt in Software Engineering."
category: "software engineering"
tags: [agile practices]
---
{% include JB/setup %}

In a previous article, I introduced **[technical debt as a *system* with a positive feedback loop](/software%20engineering/2014/03/06/tech-debt/)**. In this one, I discuss using **Agile Practices** to tackle not only the debt, but also the **Technical Debt System** in order to minimize and break the positive feedback loop. Let's talk about the how and the when, on the following fronts:

* Business Pressure, Inadequate Review, Definition of Done, Delayed Refactoring, Fear

![image](/assets/posts/2015-02-06-managing-tech-debt/techdebt-attack-state.png)

###How

####Labels and Filters

Hopefully you're using an **issue tracking** system. Track technical debt just as you would any other task or bug. Use labels and filters so that you can bring up a Technical Debt Dashboard. Simply by tracking technical debt we have removed **fear** and promoted **transparency** in order to have better conversations that help alleviate **business pressure**. Now we're in a good position to tackle it. 

####Definition of Done

You have a **Definition of Done** right? Having an adequate definition of done is a key component in constraining the accumulation of technical debt. Your definition of done could include but not be limited to:

* Acceptance Criteria for Story is met.
* Unit Tests that exercise your changes.
* Integration Tests that exercise your changes.  
* All tests pass.
* 80-95% branch & line test coverage (decide what thresholds make sense for *your* team).
* Has been code reviewed by N team members.
* Static Analysis and Code Formatting rules.

####Continuous Integration

Exercise as much of the **Definition of Done** as possible in your **Continuous Integration** builds, and have them fail when these standards are not met. This removes **fear of refactoring**, thereby limiting the introduction of new technical debt. 

Run CI builds on your topic branches such that code which doesn't pass CI doesn't get merged into an integration branch. Extra bonus - running CI on topic branches avoids the practice of shaming developers who break integration.    

####Backlog Grooming

Prioritize and point your technical debt dashboard during grooming sessions and work with the **Product Owner** to order these items in your regular backlog. Ask clarifying questions like "*What is the business value of refactoring this?*" and "*What is the cost of not refactoring it?*"

Keep in mind that the **Product Owner** should be responsible for ordering the backlog, including issues of technical debt. It may seem obvious, but a key success factor for an agile team is iterating on business value, always pulling in the highest value from the top of the backlog. Cherry picking other tasks is analagous to **stealing from the project**.

On the other hand, determining the business value of technical debt relative to delivering stories can be tricky. Remember that the cost of technical debt includes **[Time to Deliver, Code Smell and Bugs](/software%20engineering/2014/03/06/tech-debt/#time_to_deliver)**    

####Sprint Planning

Pulling technical debt points into your sprint becomes trivial if it's part of the ordered backlog. However, if ordering technical debt isn't working, establish a **policy**. Examples:
 
* Our team can do 20 points per Sprint and we pull in 3 points of technical debt during each sprint planning session.  
* Every third sprint we do 10 points of technical debt. 

####Sprint Retros

Agile Values include **Transparency**. Dedicate time during Sprint Retros to raise up issues of new technical debt, and ensure that these issues are comprehended in your Issue Tracking system. 

Do you have a **policy** for tackling tech debt? ...is it working?  ...does it need to be changed?

Accumulation of tech debt could point to an **[inadequate definition of done](/software%20engineering/2014/03/06/tech-debt/#inadequate_review__dod)**. Is your definition of done up to date?  Does it need to be re-evaluated?

###When?

####Right now

On the ground, in the trenches... If **Delayed Refactoring** can be avoided, take some extra time and work through your technical debt right now. Be a steward of the code and leave it better than you found it. If you can't address it now, then make sure you track it as an issue.

Pull technical debt points into your sprint during **Sprint Planning**.

####During Code Reviews

Code Reviews can and should be **iterative and conversational**. Budget enough time in your process and *expect* to make changes based on peer feedback. Make an effort to identify technical debt during code reviews and take the time to address those issues.  

####When it’s Blocking You

When technical debt blocks you from completing your work, that's probably a red flag that it's time to tackle it. You may be able to put in a work-around but it's likely going to just keep blocking you in the future. Resist the temptation to adjust the Definition of Done (lowering test coverage thresholds for example) in order to move on. 

####Dedicated Sprints

More often than we might like to admit, technical debt is accumulated more during the last bit of development, close to release time. That is when we're most likely to experience elevated **[Business Pressure](/software%20engineering/2014/03/06/tech-debt/#business_pressure)**. We're more likely to sacrifice the **definition of done** in order to get a release out the door. 

Although this particular risk can be mitigated by practicing **Continuous Delivery**, that technique is for another time, another blog.

Once that big release goes out the door, there will likely be a period of relaxed **business pressure**. This is a really good time to pay back technical debt in a big way. It may make sense for your team to dedicate an entire sprint theme to technical debt, with buy-in from the Product Owner.

###Agile Practices

Hopefully you can see how **Agile Practices** address Business Pressure, Inadequate Review, Definition of Done and Delayed Refactoring in order to attack the **[system of technical debt](/software%20engineering/2014/03/06/tech-debt/#technical_debt_has_a_feedback_loop)**. Using these techniques we can prevent and tackle technical debt on your projects.

