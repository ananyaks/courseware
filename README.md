Courseware for Engineering Software as a Service
================================================

a/k/a UC Berkeley CS (W)169(A,L) Software Engineering, a/k/a CS 169.(1,2,3)x on
EdX

## Review/Discussion materials (available to anyone)

This repo contains information useful to instructors (and arguably
students) using the [ESaaS](http://www.saasbook.info) course materials, including the following:
* `discussions`: Worksheets providing hands-on coding and problem solving exercises.
* `practice-exams`: Review slides and practice exams for midterms and finals.
* `self-checks`: Questions per module for students to verify their understanding.

## CHIPS (Coding/Hands-on Integrated Projects) with Autograding

The recommended setup is to use [Codio](https://www.codio.com/resources/esaas?utm_campaign=E-SaaS&utm_source=Referral&utm_medium=AF)
for programming assignments and autograding; their implementation of ESaaS resources (including the full textbook, ungraded activities, and auto-graded CHIPS) allows you to use our fully configured coursework in your classes with just a few clicks at a very low cost per student that includes direct customer support.
The [book's website](http://www.saasbook.info/instructors) has other options if you don't wish to use Codio.  

Here's a quick summary of the assignments, presented in the order in which they appear in the [ESaaS textbook](http://www.saasbook.info). There are three types:

1. **Autograded:** The solutions repos (restricted to [registered instructors](https://www.saasbook.info/instructors)) include reference solutions, Codio-based autograders in the Codio course, and files for manually configuring [Gradescope](https://gradescope.com)-based autograding.
2. **Self-graded:**  CHIPS involves coding, but rather than an autograder, includes tests students run themselves.
3. **Comprehension:** CHIPS involves minimal or no coding, but rather performing some tasks and answering self-check questions about them.  You can, e.g., use these for group work, peer grading, etc.

* 2.5 [Ruby Intro](/saasbook/hw-ruby-intro) ([autograder/solutions](/saasbook/hw-ruby-intro-ci)): gentle intro to Ruby idioms, including running instructor-provided unit tests to check your answers
* 3.3 [HTTP and URIs](/saasbook/hw-http-intro) (comprehension): intro to HTTP requests, URIs, and cookies, using `curl` and `netcat` to see raw data, using the [esaas-cookie-demo app](https://esaas-cookie-demo.herokuapp.com) ([source](/saasbook/esaas-cookie-demo)).
* 3.7 [Create and Deploy a Simple SaaS App](/saasbook/hw-sinatra-saas-hangperson) ([autograder/solutions](/saasbook/hw-sinatra-saas-hangperson-ci)): de-mystifies the creation of a SaaS app (a simple Hangman game using Sinatra) including use of an external service, and how to think about RESTfully "wrapping" application logic in SaaS.
* 4.3 [ActiveRecord Basics](/saasbook/hw-activerecord-practice) (self-graded): write ActiveRecord queries against a provided seeded database.
* 4.5  [Rails Routes](https://rails-routing-practice.herokuapp.com) (self-graded): not actually a homework assignment, but a simple app that lets students enter syntactically valid Rails routes and understand the RESTful routes that Rails would generate for them.
* 4.7 [Hangperson on Rails](/saasbook/hw-rails-hangperson) (comprehension with [reference solutions](/saasbook/hw-rails-hangperson-ci)): use the same Hangperson game logic and Cucumber scenarios as CHIPS 3.7, but scaffolds a walkthrough of how to deploy the app with Rails instead of Sinatra, as an on-ramp understanding the complex Rails framework.
* 4.9 [Hello Rails](/saasbook/hw-hello-rails) (self-graded): create a brand-new Rails app (RottenPotatoes) from scratch, including routes, database setup, using the debugger, and deploying to Heroku.
* 5.3 [Rails Intro](/saasbook/hw-rails-intro) ([autograder/solutions](/saasbook/hw-rails-intro-ci)): enhance RottenPotatoes to filter and sort movie lists. (Coming soon: also add SSO login to RottenPotatoes.)
* 5.7 Associations (TBD) 
* 6.9 AJAX Enhancements to RottenPotatoes (TBD) 
* 7.7 [Intro to BDD and Cucumber](/saasbook/hw-bdd-cucumber) ([autograder/solutions](/saasbook/hw-bdd-cucumber-ci)): write features to test happy and sad paths of RottenPotatoes. 
* 8.5 [RSpec on Rails](/saasbook/hw-tdd-rspec): (**Needs updating & CI repo**) Given a Cucumber scenario for a not-yet-implemented feature, students use TDD and RSpec to write tests that drive the creation of the code to make the scenario pass.  Students also learn to use Travis CI to automate testing workflow.
* 8.9 [BDD/TDD Cycle](/saasbook/hw-acceptance-unit-test-cycle-lite): a complete pass through the BDD and TDD cycle of specifying a feature in terms of stories and then using TDD with RSpec to drive the development and deployment of the feature.
* 10.5 [Agile Iterations]() Two (or more) full iterations of Agile adding features to an existing (legacy) app
* 12.8 [Exploiting Caching and Indices](/saasbook/hw-indices-performance): improve the performance of RottenPotatoes by adding database indices to speed up key queries. 

## Optional additional CHIPS (not referenced in textbook)

* [Oracle of Bacon](/saasbook/hw-oracle-of-bacon): Build a simple command-line app that uses external services in a SOA, including parsing XML responses. 
* [Design Review](/saasbook/hw-design-review): We use this in the project portion of the course. This is not a programming assignment but rather a 3-part scaffolded process for doing design reviews and technical presentations.  (Each part can be used more or less independently.)  It is intended to be used in conjunction with student teams doing their own open-ended projects, so no code is provided.  In part 1 (Design Review), teams are paired up and each team evaluates the other's design and gives feedback on possible improvements.  In part 2 (Presentation), teams give technical presentations about the design review; these are peer-evaluated (or instructor-evaluated) according to a provided rubric.  In part 3 (Handoff), teams modify their repos as needed to ensure the project is easy for another team to pick up and continue working on.

## Open ended questions for written exams ([instructor access only](https://www.saasbook.info/instructors))

[Open-ended response questions](/saasbook/open-response-exam-questions) suitable for manual grading, along with reference solutions.

## Multiple-choice/machine-gradable questions ([instructor access only](https://www.saasbook.info/instructors))

[Multiple choice questions](/saasbook/csw169a-quizzes) grouped by textbook chapter.  The [RuQL gem](/saasbook/ruql) and its associated formatters let you export quiz questions to HTML/hardcopy, the Canvas LMS, and other quiz formats.

## Coding Exam questions with autograders ([instructor access only](https://www.saasbook.info/instructors))

We've given exams where part of the exam is spent writing actual code. We have developed an infrastructure for doing this that allows students full read-only access to the Internet via Google's cache, so they can look up any existing information they want but cannot post a question or send email/messages to ask for the answers.  However, you can also use these as homework assignments since they included test cases.

The repos contain solutions and test cases as well as questions; instructions are provided in each repo's `README-instructor.md` for creating just the student-facing part of the package.

In our setup, since the questions are multiple parts with later parts building on the results of earlier ones, each question subpart is associated with a hint and/or with the answer (i.e. code that if copy-pasted in the right place will solve that subpart).  Students can "reveal" these hints if they accept a penalty of a substantial fraction of the points the exam question is worth.  The hints are part of each repo; our [reveal](/saasbook/reveal) script is installed in the exam environment (described in [this paper]((https://dl.acm.org/authorize?N680620)) to record which hints were used and calculate the penalty.  We [found](https://dl.acm.org/authorize?N680629) that weaker students do not request more hints than stronger students, even though they would sometimes benefit more from doing so; weaker students are more likely to request hints on lower-scoring coding questions than higher-scoring ones; and all students are equally well able to use hints once provided.

* [Interview Scheduler](/saasbook/exam-interviewscheduler-associations): Modify an existing app to add the correct associations among Interviews, Candidates, and Recruiters.  Factor out some common code among the models and mix it back in, to DRY out the code. [Solutions](/saasbook/exam-interviewscheduler-associations-
* **Incomplete** [Ruby Iterators](/saasbook/exam-ruby-iterators) Create Ruby iterators for a new `Matrix` class.
* [Can I Stream It?](/saasbook/exam-rottenpotatoes-canistreamit) Enhance RottenPotatoes by adding a view that displays information retrieved from the `CanIStream.it` API.
*  [Encryption Demo](/saasbook/exam-encrypty) Create this [simple app](https://encrypty.herokuapp.com) ([source](/saasbook/encrypty)) that allows users to specify a key for symmetric encryption and to encrypt/decrypt text with that key.

