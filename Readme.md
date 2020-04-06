# Software Quality Assurance


## Code Review

### Introduction

Let's start with a little definition. Code review is a review of a piece of code before it is added to the overall source code of an application. This review aims to detect (among other things) non-compliance with best practices, architectural weaknesses, forgotten "dead code" ... Code review is a fairly common practice in development. This practice can be implemented regardless of the size of the teams. Having an effective code review policy is time consuming and may seem at first glance to be an unnecessary cost. However, it offers many advantages, some directly visible, others more latent:

- The quality of the code is obviously improved, it becomes more maintainable, better architected...
- As mentioned above, the number of bugs is reduced;
- Communication and collaboration between team members is increased;
- Reading code has a formative effect on the project team;
- The knowledge of the project is correctly spread over the whole team.

It is therefore essential to know the best practices of code reviewing.

### Best Practices

This practice can be divided into two categories. You can do automated checks for some of the things — e.g., structure and logic. But others — e.g., design and functionality — require a human reviewer to evaluate. We will therefore first talk about good practices in the case of a manual code review.

#### Manual Code Review

- Take your time. Never exceed 60 minutes of examination time at a time. Performance and attention to detail tend to decrease after this point. Studies show that taking breaks from a task for a period of time helps to maintain workflow without sacrificing much of its quality. So if the task requires a great deal of attention from you, it is best to take a break. During this break, think about something else, clear your head. This way, when you resume the code review, you will get a fresh look at the code. So if your review lasts more than 60 minutes, take a break.

- Review Less Than 400 Lines Of Code. As well as the time spent reviewing code, reviewing too much code is also counterproductive. Try to limit each review session to 400 lines or less. A lot of research shows that beyond this line limit, the brain can no longer process information efficiently. Keep in mind that code review is a matter of quality rather than quantity. If a team decides to exceed the 400 LOC limit, the ability to find defects is severely affected. It is estimated that if a code examination is performed on less than 400 lines, in several times if necessary, it would cover 70 to 90% of defects.

#### Automatic Code Review

- Automate to Save Time. Despite good practices, reviewing the code remains a very time-consuming task. It is therefore important to automate what can be automated using the right tools. One such tool is static code analyzers, for example, which detect potential problems in the code by comparing it to coding rules. Running static code analyzers on code minimizes the number of problems that reach the peer review phase.

- Lookout For The Key Metrics. Of course, you need to know what to look for in the case of automatic code examination. Closely monitor internal process parameters such as inspection rate - the speed at which an examination is performed -, defect rate - the number of bugs identified per hour of examination -, defect density - the average number of bugs per line of code. These are the metrics that will give you a global view of the state of your code.

- Immediately Fix Defects Found. C'est parfois dure de quitter ça tâche actuel pour revenir sur un bug fraîchement découvert. Ce n'est pas parse que vous arrêtez votre tâche actuel pour s'occuper d'un bug que vous allez être en retard sur votre travail. Au contraire, le but est de ne pas laisser les bug s'accumuler au file du temps.

### Bad Practices 

- Too many comments. When a person makes a mistake, chances are they have made the same mistake in several places. Do not drown the person who is going to correct the code under your comments. By doing so, you may just discourage the person. Grouping comments together allows you to convey the same message without overwhelming the review requester. It will also make the correction clearer.


https://medium.com/cuelogic-technologies/code-review-process-best-practices-3eeecab26ded

https://www.perforce.com/blog/qac/9-best-practices-for-code-review

https://medium.com/palantir/code-review-best-practices-19e02780015f

https://medium.com/@sandya.sankarram/unlearning-toxic-behaviors-in-a-code-review-culture-b7c295452a3c

https://techbeacon.com/app-dev-testing/how-sabotage-code-review