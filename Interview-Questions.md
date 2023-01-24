These are some questions we can ask during phone screens and interviews.

Note that most of these are used to identify technical skills.
However, there are many non-technical skills and traits that we'd also like
to identify (although they tend to be harder to determine objectively):

* Ability to work with other team members
* Ability to learn
* Ability to teach/mentor
* Empathy
* Curiosity
* Courage
* Communication
* Entrepreneurial mindset
* Gets things done
* Discipline
* Sense of purpose
* Leadership


General
-------

* What interests you about this position?
* How would you describe your ideal boss?
* How would you describe your ideal work environment?
    * What do people in that environment do to create/keep their culture?
* How do you define success?
    * Do you see yourself as a success?
* What aspects of your current job are you most passionate about?
* How do you currently affect the bottom line at your company?
* Where do you see the IT industry in 3 years?
* What did you like least about your last manager?
* Have you ever been fired?


Learning
--------

* What are you passionate about (work-wise)?
* What are you currently (interested in) learning?
* What ways do you like to learn new things?
* How do you stay up to date on technologies?
* What are some of the books you’ve read recently?
    * They don’t have to be work-related.
* Could you tell me about the last time you had to learn a brand new skill?
    * How did you go about learning it?
    * How long did it take?
    * What was the toughest part of the process?


UNIX
----

* What arguments do you prefer for the `ps` command?
* How would you show the PID of something named "xyz" running?
    * How would you avoid the `grep` process being shown a well?
* How does the `kill` command work? (_most people don't get this quite right_)
* How would you restart Apache?
    * When would you have to restart Apache?
    * When would you NOT have to restart Apache?
* Explain file permissions.
* What is the sticky bit?
* Where's the difference between a soft link and a hard link?
* What is an inode?
* If you do `ls`, you can see files, directories, and what else?
* If you accidentally delete a file, but another process still has it open, how can you rescue it?
* What command(s) can you use to show what process has a file open?
    * Answer: `lsof`
    * Answer: `fuser`
* How can you see what process is listening on a port?
    * `lsof -i tcp:$PORT` (Linux)
    * `fuser -v $PORT/tcp` (BSD)
    * `netstat -planet | grep $PORT` (Linux)
    * `netstat -n | grep LISTEN | grep $PORT` (Mac)
* What are the advantages of Nginx over Apache?
* All I/O is through "files" in the file system, except for what?
* What is RAID?
    * What are the RAID levels?
    * BONUS: Why does nobody use levels 2, 3, or 4?
* What does the `ldd` command do?
* Name a few UNIX commands you use that you think other people should use more.


Networking
----------

* Can you explain how DNS works?
* When should you *NOT* use a CNAME DNS record?
* What is a proxy?
    * What is a reverse proxy? (_people have a hard time putting this into words_)
* How does a switch work?
* How does a router work?
* What’s the difference between TCP and UDP?
* Name some commonly used TCP and UDP ports, and their associated protocols.
* What's the difference between IP and UDP?
* Can you name the 7 layers of the OSI model?
    * Can you name the 4 layers of the TCP/IP stack?
* How does a TCP 3-way handshake work?
* What's an MTU?
    * Why is it important?
* What is a VLAN?
* How can you find a server's IP address?
    * How can you find a server's *public* IP address? (_kind of a trick question_)
* What challenges do self-signed SSL (TLS) certificates present?
* How does a system get its IP address?
* How does DHCP work?
* How does ARP work?
    * What is a gratuitous ARP? When/why would you send one?
* Explain CIDR and CIDR notation.
* What is the subnet mask for a 24-bit subnet?
* What is the loopback address? What is it used for?
    * What is the IPv6 loopback address?
* Can you name all 3 private IPv4 address ranges? (_the 20-bit block will be trickiest to recall_)
    * Which RFC defines them?
    * Bonus points if you can name a 4th.
    * Bonus points if you can name the IPv6 private address range.


Web
---

* What's the problem with inline CSS?
* What are the advantages and disadvantages of HTTP being stateless?
    * How can a web app maintain state on top of a stateless protocol?
* How do the HTTP methods correspond to the CRUD verbs?
    * Bonus points for knowing where Rails CRUD actions don't work as the HTTP methods are intended.
* What are the parts of a URL?
* What's the difference between a URL and a URI? (_this is really just a trivia question_)
* Can you describe the HTTP request/response cycle?
* What tools can you use to view the HTTP request/response cycle?
* What does an HTTP request look like?
* Can you name some HTTP request and response headers?
* Which HTTP methods are idempotent? Which are NOT idempotent?
    * What does "idempotent" mean?
* Which HTTP methods are "safe"?
    * What's the problem with GET requests that make database changes?
* What happens when you enter `google.com` in a web browser?
    * Tell me everything that happens between your computer, Google's servers, and any other Internet devices that are involved.
    * Start with a 1-minute overview, then we can dig deeper.
    * (_This is also helpful to see if someone can be consise, while still being able to dig in deeper._)


Cloud
-----

* Do you know what a 12-factor app is?
* What are some factors that need to be considered when deploying an app to the cloud?
* What's the difference between REST and SOAP?
* What is HATEOAS?
* What are some solutions to the challenges of versioning APIs?
* Do you know what the CAP theorem is?
* What are the trade-offs of NoSQL versus SQL?
* What AWS services are you familiar with?
* Why should you not put databases on VMs and containers?
    * Answer: performance issues (still)
    * Answer: possibility of accidentally taking down due to configuration issues


OOP
---

* What is Object Oriented Programming? (_not getting "polymorphism" very often_)
    * What is polymorphism?
    * What is encapsulation?
* What's the difference between an object and a class?
* Can you have object-orientation without classes?
* What does SOLID stand for?
    * What does the single responsibility principle (SRP) mean?
    * What is the open/closed principle?
    * What is the Liskov substitution principle?
    * What is the interface segregation principle? (_probably the hardest of these_)
    * What is the dependency inversion principle?
* What is the Law of Demeter?
* What problems can inheritance cause?
    * How can you mitigate those problems?
    * What's the problem with multiple inheritance?
* Can you explain cohesion and coupling?
* What is a god class?
    * How can you mitigate the issues with having a god class?
* What is a pattern?
    * Explain one of the patterns you use.


Dev
---

* What is the DRY principle?
    * What are some things to be aware of when DRYing up code?
* What’s your favorite programming language?
    * What do you like about it?
    * What are the biggest problems you have with that language?
* How do you feel about commenting code?
* What’s the difference between `git merge` and `git rebase`? (_not many are getting this_)
* Why should you not use regular expressions to parse HTML?
* Can you explain what big-O notation is? (_not many are getting this one quite right_)
* What is SQL injection?
    * How can you prevent SQL injection?


Architecure
-----------

* What even is software architecture?
* What are the pros and cons of micro-services?
* Have you used message queues to communicate between components?
* Have you used a service bus?


DevOps
------

* Have you used Ansible, Puppet, or Chef?
* Have you used Docker?
* Have you used Kubernetes?
* Have you used Terraform?
* Have you used any other DevOps tools?


Agile
-----

* What does Agile mean to you?
    * How does this compare to the Agile Manifesto?
    * Which Agile methodologies do you know best?
* What are the pros and cons of Agile methodologies (in general, and particular methodologies)?
* Which Agile practices do you like/dislike?
* What's the purpose of a retrospective?
* What's the purpose of standup meetings?
    * What are the biggest anti-patterns that happen with standup meetings?
* Have you pair programmed?
    * How do you feel about pair programming?
    * Have you worked in a mob/ensemble?
* What are the benefits of TDD?
    * What does the “driven” in TDD mean?
    * What’s the advantage of test first?
* What is a code smell?
    * Can you name a code smell?
* What is refactoring? (_most people miss the part about not changing external behavior_)
    * Can you name a refactoring? (_see http://refactoring.com/catalog for a list_)
* What is continuous delivery? How do you get there?


Management / Leadership
-----------------------

* Can you explain the difference between management and leadership?
* How have you gone about improving your teams' processes?
* How do you ensure that you're neither micro-managing nor being too hands-off?
* How do you offer criticism?
    * How do you best receive criticism?
        * (_Hopefully this will prompt them to talk about offering criticism differently to different people._)
* What is your approach to delivering bad news?
* How do you prioritize your time managing a team?


Behavioral
----------

* What kinds of things do you do to improve how you do your job?
* How would your most recent teammates describe you?
* What do people assume about you that is incorrect? Why?
* Talk about a fun problem that you've solved in the past that you're proud of.
* What is the most original, innovative solution you’ve ever created?
* How do you take criticism? How do you like to receive criticism?
* Could you tell us about a time where you had to make an unpopular decision?
* How do you convince teammates that you're right?


Closing
-------

* Are there any questions you wished we would have asked?
* How would you rate me as an interviewer?
