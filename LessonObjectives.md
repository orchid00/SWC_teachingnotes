# Lessons and Objectives

## Questions
1. How can I design more effective lessons?
2. What lessons do Software and Data Carpentry currently contain?

## Objectives
1. Describe the characteristics of a good learning objective and correctly state whether a learning objective meets those criteria.
2. Classify the level of a learning objective in terms of Bloom's taxonomy and similar cognitive hierarchies.
3. Write learning objects that cover multiple learning outcomes.
4. Describe the four steps in reverse instructional design and explain why following them is an efficient way to create good teaching materials.
5. Analyze a lesson by comparing it to the elements of WHERETO.
6. Summarize the existing Software Carpentry lessons.
7. Write a learner profile describing a typical member of their intended audience.

## Writing Learning Objectives
Summative and formative assessments help instructors figure out what they’re going to teach. In order to communicate that to learners and other instructors, we should also write learning objectives. It’s easy to come up with fuzzy ones like, “Learners will gain an appreciation of the role of research software engineers in the research process.” Useful ones take a bit more work.

What we want are specific, verifiable descriptions of what learners can do to demonstrate their learning. Each learning objective should have a measurable or verifiable verb specifying what the learner will do, and should specify the criteria for acceptable performance. For example, a better learning objective than the one above would be, “Learners will list three things that make research software engineers distinct from other specialists involved in the research process.”

In order to formulate good learning objectives we need to decide what kinds of learning we are aiming for. For example, do we wants students to diagnose why a microscope isn’t focusing properly and to design a new microscope that focuses more easily. These two things require vastly different learning skills. 

### Bloom's Taxonomy 
Bloom's taxonomy is a set of three hierarchical models used to classify educational learning objectives into levels of complexity and specificity. This table shows the cognitive domain or knowledge-based domain of learning and provides examples of typical learning objective verbs that address each level.

|Desired Learning Outcome|Learning Objective Verbs|
|:---:|:---:|
|knowledge|name, define, recall|
|comprehension|restate, locate, explain, recognize|
|application|apply, demonstrate, use|
analysis|differentiate, criticize, compare|
|synthesis|design, construct, organize|
|evaluation|choose, rate, select|


### Exercise: Think, pair, and share to evaluate SWC and DC learning objects

Complete the following steps to evaluate real learning objectives from current SWC and DC lessons and then reword them. 

1. Pick one of the learning objectives listed below. 
2. Identify the learning objective verb. 
3. Decide what type of learning outcome this applies to (i.e. comprehension, application, evaluation)
4. Reword the learning objective for a different learning outcome (i.d. from application to knowledge based outcome or vice versa). 
5. Pair up to discuss your rewording. Help each other with point 3 or 4 if necessary. 
6. Paste the original and your re-worded learning objectives in the Etherpad. 

**Real SWC and DC Learning Objectives**
- [DC Python Ecology Lesson -](https://github.com/datacarpentry/python-ecology-lesson/blob/gh-pages/04-merging-data.md) join two DataFrames together using a uniqueID found in both DataFrames 
- [SWC Programming with Python -](http://swcarpentry.github.io/python-novice-inflammation/04-files.html) use a library function to get a list of filenames that match a simple wildcard pattern
- [SWC R for Reproducible Scientific Analysis -](http://swcarpentry.github.io/r-novice-gapminder/08-plot-ggplot2.html) understand the basics of the aesthetics layer and the geometry layer of a ggplot2
- [SWC Unix Shell Lesson -](http://swcarpentry.github.io/shell-novice/04-loop.html) explain why spaces and some punctuation characters shouldn’t be used in file names 
- [SWC Programming with MATLAB -](http://swcarpentry.github.io/matlab-novice-inflammation/06-defensive.html) - explain what an assertion is
- [SWC Version Control with Git](http://swcarpentry.github.io/git-novice/07-github.html) push to and pull from a remote repository
- [SWC Instructor Training - ](http://swcarpentry.github.io/instructor-training/07-memory/) construct a concept map for a short lesson showing the lesson's key ideas and the relationships between them

## Reverse Instructional Design
Let's face it. Most instructors put together the slides for a lecture the day before they lecture. Then, a few weeks later, they put together the exam for the materials they covered during the previous 3-4 weeks. 

However, there is a better way to do this. To provide an analogy, let's discuss the role of **test-driven development** in software development. When test-driven programmers don’t write software and then (possibly) write tests; instead, they write the tests first, then write just enough new software to make those tests pass, and then clean up a bit. Writing tests forces programmers to specify exactly what they’re trying to accomplish and what “done” looks like. It’s easy to be vague when using a human language like English or Korean, but it’s much harder to be vague in Python or R.

A similar “backward” method works very well for lesson design. As described in Wiggins and McTighe’s [Understanding by Design](http://www.amazon.com/Understanding-Design-Expanded-Grant-Wiggins/dp/0131950843/), the method proceeds through four stages:

1. Identify what is worth learning (e.g., draw concept maps).
2. Decide what constitutes evidence that learning has taken place (i.e., create the final exam or some other summative assessment).
3. Design practice work (formative assessments to be done in class and the exercises to be done out of class) to prepare learners for what they will have to do during the summative assessment. 
4. Sort those practices in order of increasing complexity and then write short episodes to close the gap between what learners know and what they need to know in order to do each one. (An actual classroom lesson will then consist of several such episodes, each building toward a quick formative assessment.)

This reverse instructional design method helps keep teaching focused on its objectives. It also ensures that learners don’t face anything on the final exam that the course hasn’t prepared them for. When writing the lessons themselves, Wiggins and McTighe use the acronym WHERETO:

**Where**: ensure that learners see the big picture, can answer “why?” questions, and know the final performance expectations as soon as possible.
**Hook**: immerse learners in the lesson’s ideas and issues.
**Equip**: provide learners with the tools, skills, and information needed to be successful in the upcoming formative assessment.
**Rethink**: consider different perspectives, challenge their prior assumptions, etc.
**Evaluate**: ensure that the learners and the instructor get actionable feedback from the formative assessment.
**Tailor**: find ways to personalize learning through differentiated instruction and/or assessment.
**Organize**: put the episodes in sequence.

## SWC and DC Lesson Development
The lesson materials for Software and Data Carpentry are hosted on GitHub:

- [Data Carpentry on GitHub](https://github.com/datacarpentry)
- [Software Carpentry on GitHub](https://github.com/swcarpentry/)

Our lessons are developed collaboratively — in 2015 alone, almost 200 people made contributions to various lessons. Each lesson is in a separate repository, and consists of narrative lesson material and an associated directory containing the data or scripts needed in the lesson. This source material is also then served as a website, using GitHubs “gh-pages” feature.

Lesson contribution is managed within the repository using “issues” and “pull requests”. New problems or suggestions can be introduced as issues, discussed by the community, and addressed via a pull request, which serves as a “request” to make changes, and can also be discussed before changes are merged.

Though we aren't perfect, each lesson and the episodes (or subparts of the lesson) each begin with learning objectives and include multiple challenge questions that are designed to test learners grasp of the new knowledge.


## Existing SWC and DC Lessons

**Software Carpentry’s** most commonly used lessons are:

[The Unix Shell](https://github.com/swcarpentry/shell-novice)
[Version Control with Git](https://github.com/swcarpentry/git-novice)
[Programming with Python](https://github.com/swcarpentry/python-novice-inflammation)
[Programming with R](https://github.com/swcarpentry/r-novice-inflammation)
[R for Reproducible Scientific Analysis](https://github.com/swcarpentry/r-novice-gapminder)

Only one of the three programming lessons (Python or one of the R lessons) is used in a typical workshop. Software Carpentry also maintains lessons on Mercurial, SQL, MATLAB, Automation, and Make that are less frequently used.

Take a look through these lessons when you get home to see what we teach. 

You can also take a look at the [future SWXC orkshop](http://software-carpentry.org/workshops/) and [past SWC workshop](http://software-carpentry.org/workshops/past/) webpages to see how people put together workshops using the existing lessons. 

## Leaner Profiles

We have been talking about lot about the teacher perspective and what you need to do to design good lessons, but let's not forget about the learners. One way to characterize the audience for a course is to write learner profiles. This technique is borrowed from user interface design, where short profiles of typical users are created to help designers think about their audience’s needs, and to give them a shorthand for talking about specific cases.

Learner profiles have three parts:
1. the person’s general background
2. the problem they face
3.  how the course will help them

A learner profile for Software Carpentry might be:

João is an agricultural engineer doing his masters in soil physics. His programming experience is a first year programming course using C. He was never able to use this low-level programming into his activities, and never programmed after the first year.

His work consists of evaluating physical properties of soil samples from different conditions. Some of the soil properties are measured by an automated device that sends logs in a text format to his machine. João has to open each file in Excel, crop the first and last quarters of points, and calculate an average.

Software Carpentry will show João how to write shell scripts to count the lines and crop the right range for each file, and how to use R to read these files and calculate the required statistics. It will also show him how to put his programs and files under version control so that he can re-run analyses and figure out which results may have been affected by changes.

All our lessons are designed for novices with no background. However, we collect pre-workshop surveys that are designed to collect this information and more about the students. This information will be given to instructors and can help you tailor your workshop more specifically to the audience. 

## Key Points.
- Communicate lesson goals by writing specific, verifiable learning objectives.
- Use reverse instructional design to create lessons: concepts, summative assessment, formative assessments, teachings.
- Software Carpentry's most commonly used lessons cover the Unix shell, version control, and programming.
- Data Carpentry's lessons cover data cleanup, management, analysis, and visualization in a variety of fields.
- Collecting learner profiles can help clarify the audience for a lesson.



