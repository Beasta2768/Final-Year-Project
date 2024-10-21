[[Final Year Project Mark Scheme.sheet|Mark Scheme]]
- Project Idea  - Photo Storage web app with react, that uses image recognition to tag and organise images and create collages based on those tags.
## Week 1 (16/09/24)
### Lecture & Seminar
-  FYP is meant to demonstrate students ability to work on a longer term project individually
- Assessment Breakdown
 1.  Project proposal  - 10% 
	 - Document that includes:
		- the reasons you are doing the project
		- the methodology you will be using
		- the objectives of the project
 2. Literature review and Methodology - 15% 
	 - Review of the reading done for the project (relevant documentation counts)
 3. Abstract and Introduction  and Requirements to Conclusions - 35% 
	 - Majority of the marks so is impotent to do well and start as early as possible
 4. Work Done - 20% 
	 - project progress as a whole
 5. Professional Working Practices - 10% 
	 - Engagement and attendance of seminars is important for this
 6. Presentation - 10%
	 - Finished project demonstration
	 - Has to be deployed in a live environment and be accessible through an app or a website
	  - We also covered logbooks and how they should document your progress throughout the project development process
### Project Development (18-19/09/24)
-  For this week with my project development, I have yet to think of an idea for my project. However, I know that I want my project to use the React framework so it would need to be a web-based project. I for next week I want to find a project idea that I could find interesting, but I don't have an idea of what my project could be.
### Advanced web development
-  this week was an introduction to the module where we had a brief summary of the lecture the history of the web, and how the web developed from static to dynamic pages.
- We also covered data exchange formats used in the web like XML, CSV and JSON, with JSON and XML being the most prominent of the three in the modern era
 - With notably widespread use in web API's to transfer information on request
## Week 2 (23/09/24)
### Lecture & Seminar
- We covered proposal writing during the lecture including:
- Things the proposal should include
 - What you are going to do
- Who the project could benefit
 - The reasons you are doing the project
 - The objectives of the project
 - Methodology of the project i.e. waterfall, agile etc.
 - Gantt chart and logbook
- The proposal would be due in week 4 (wb 07/10/24)
- During the Seminar covered :
	- Project should be more complicated than second-year CSS
	- Should be mindful of ethical approval - and the implication of the topic/ project idea I choose
	 - I might have to adjust the project to fit with ethical approval, and reduce the load of work for
	- Project would most likely end up being a proto-type so focus on what the final project would be capable of doing
	 - However, don't keep leave time for write-up and not to  just focus on packing a lot of features into the project for the sake of it
	- Engagement and attendance in the seminars are important at they count toward the working professional section of our proposal grade
### Project Development (25-26/09/24)
- For the second week of project development I decided on making a Photo Storage web app using React, but since that wasn't a complex enough project I decided to add image recognition that tags and organise images uploaded to the web app to create collages based on those tags.
 - This project aims to help people get a curated set of collages through the use of AI
 - I plan to use an image recognition framework in node.js as that is the back-end solution that I am initially planning on using.
### Advanced web development
- This week we covered frameworks and the framework we would be using during the module Symfony. Symfony is a PHP framework that allows you to build PHP web applications faster due to the generic modules it offers.
 - When symphony gets a web request (/about) it goes through the kernel which takes it to the controller where the code for the view is and any arguments are resolved and then sent to the call controller to be turned to a rendered view and send back to the client as a response.
## Week 3 (30/09/24)
### Lecture & Seminar
- The lecture this week covered different development methods we could use for our projects:
 - We covered research-based projects that pick a topic to research and create a product, with their project being focused on answering a research question and code done/ app made would be used to help find the answer to that research question
- We also covered the agile methodology and how it uses an iterative and incremental cycle where you complete sections of your project going through the whole development cycle
- In the seminar this week we covered more proposal-writing tips
- We went over writing about alternative methods that could be used in your proposal methodology and why you wouldn't be using them
- also to talk about what parts of your chosen methodology you are using  and not using
- we also covered how out project objectives shouldn't just be software features and should  include parts of the development cycle like testing.
- We also shared out project ideas with our project supervisors to get feedback on any potential problems
 - My feedback was to look into the viability of image recognition with the react framework since I already had an idea of the framework that I wanted to use.
### Project Development (2-3/10/24)
- For the third week I followed my supervisors feedback form earlier in the week and tested an image recognition module from node.
- ![[Pasted image 20241011142746.png]]
 
 - I created a new react app to test how viable this was, I used the tensor-flow module in node and made a basic UI with an image upload form.
 - I tested it with an apple and got a response after around 12 seconds of an apple with 95.04% confidence on whether it was correct
 - I also started writing my project proposal with my intro and motivation as well as the methodology I planned on using
### Advanced web development
- During this week we covered templating and how it works in symphony.
 - We covered how templating is the process of making placeholder values for content on a web page so actual values can be put in at a later stage after some data processing has occurred
 - We talked about how traditional php templating put you at risk of code injection and the fact that it was hard to maintain as the values were hard to transfer between different templates
 - The solution to this was to use twig, a templating engine which protected you from code injection. As well as the templating engine processing the code and then outputting it in PHP.
 - Development benefits of templating allow us to avoid D.R.Y code
 - We also covered twig syntax and the concept of inheriting templates making it easy to transfer values between templates
## Week 4 (07/10/24)
### Lecture & Seminar
-  In this week lecture we covered research methods for out project
 - This included a literature review, which would serve and an introduction to out project and help justify and give it context with critical evaluation of relevant projects
- It should start with identifying key concepts of the project and use as wide of a range of sources as possible
  - Each source should have a list of identifying information like title, authors, keywords/topic and a brief summary of the source. To help write the review
  - Sources should also be appropriately referenced using APA 7 the university's referencing standard
### Project Development (16-17/10/24)
- This weeks project development mainly focused of finishing an polishing my project proposal by setting my objectives and writing my development requirements
 - I also made a Gantt chart using my objectives to put at the end of my proposal
### Advanced web development
- This week we covered routing with symphony and templates as well as annotations
 - we went over some key syntax to the Yamal files used for routing in symphony and how it reads routing files from top to bottom. So your more specific routes should be at the top of the file with your basic ones at the bottom
 - We also covered annotations and how they work in php versions 8+ vs how they did in 7 and below.
 - With the modern versions no logger using comments but rather being part of the attributes of a routing function


## Week 4 (14/10/24)
### Lecture & Seminar
-  During the first part of  the seminar we discussed the risk assessment due on Friday and how we should approach it
- For the rest of the seminar we discussed the literature review and how to approach the project
	- We discussed how we should do some proof of concepts for some of the tech-stacks we are using
		- Same thing for hosting, if we are using hosting methods other than Poseidon we should talk with our supervisor to get approval for it.
### Project Development (16-17/10/24)

### Advanced web development


## Week 5 (21/10/24)
### Lecture & Seminar
- Seminar
	- Stick to Gannt chart for project coding
	- 
### Project Development (16-17/10/24)

### Advanced web development
