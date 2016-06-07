#Cognitive Load

In our final topic in educational psychology, we’ll be learning more about human memory: specifically how to remove unnecessary “load” in order to facilitate learning.

##Inquiry-based Learning
Inquiry-based learning is the educational process by which learners to ask their own questions, set their own goals, and find their own path through a subject. This is how a lot of graduate student acquire coding skills. However it doesn't work that well because it requires learners to simultaneously master a domain’s factual content and problem-solving strategies. Even though fostering creativity and independence is intuitively appealing, this may not be the best way to learn or teach.

##Theory of Cognitive Load
The theory of cognitive load posits that leaners have to deal with three things when they’re learning:

1. **Intrinsic load**: what learners have to keep in mind in order to carry out a learning task
2. **Germane load**: the (desirable) mental effort required to create linkages between new information and old (which is one of the things that distinguishes learning from memorization)
3. **Extraneous load**: everything else that distracts or gets in the way

Linguistic and visual input are processed by different parts of the human brain and are stored separately as well. This means that correlating linguistic, auditory, and visual streams of information takes cognitive effort. Think about how hard it is to read a power point slide and listen to the speaker! Learning is therefore more effective when redundant information is not being presented simultaneously in two different channels. 

##Step-by-stp solutions followed by faded examples
According to cognitive load theory, searching for a solution strategy is an extra burden on top of applying that strategy. We can therefore accelerate learning providing a  detailed step-by-step solution to a problem, followed by a series of faded examples. The first of these presents a nearly-complete use of the same problem-solving strategy just demonstrated with a small number of blanks for the learner to fill in. The next problem is also of the same type, but has more blanks, and so on until the learner is asked to solve the entire problem.


##Titus's Advanced Beginner Shell Example
My personal favorite example of a step-by-step how rename files in Unix as written by Titus Brown. 

https://github.com/ngs-docs/2016-adv-begin-shell-genomics#renaming-a-bunch-of-files

Titus used this command to test renaming the filename with the .fastq extension and with the .fq extension. Here, we loop through all the .fastq files in a directory. Then we use the function basename to replace the .fastq with .fq for all files. Then we use echo mv to print the original name (i)  and the newname (newname) to the screen as a test before really renaming the file name. 

```
for i in *.fastq
do
   newname=$(basename $i .fastq).fq
   echo mv $i $newname
done
```

##Rayna's Faded examples

Here's my faded example where using the rename principle that Titus built up to, with a modification to echo move R1 reads to R2 reads

**Fade 1 Exercise** Modify the code to only read read 1 (R1) .fastq files rather than all .fastq files.

```
for i in *_______  
do  
   newname=$(basename $i .fastq).fq  
   echo mv $i $newname  
done  
```

**Fade 1 Solution**
```
for i in *R1.fastq  
do  
   newname=$(basename $i .fastq).fq  
   echo mv $i $newname  
done  
```

Here, the important part is that only the first line of the code is modified. The basename section stays the same

**Fade 2 Exercise** Echo move all R1 files to R2 files  

```
for i in *R1.fastq  
do  
   newname=$(basename $i ._______).________  
   echo mv $i $newname  
done  
```
**Fade 2 Solution**
```
for i in *R1.fastq  
do  
   newname=$(basename $i R1.fastq)R2.fastq  
   echo mv $i $newname  
done  
```
Now students see that they need to change what we are modifying with the basename command.

**Fade 3 Exercise** Let's replace i and newname with better variable names that are more representative of the files we are working with, in this case, R1 and R2.

```
for ___ in *R1.fastq
do
   _____=$(basename $___ R1.fastq)R2.fastq
   echo mv $____ $____
done
```
**Fade 3 Solution** 
```
for R1 in *R1.fastq  
do  
   R2=$(basename $R1 R1.fastq)R2.fastq  
   echo mv $R1 $R2  
done  
```
Here, students see that they need the change the variable name and all instances where the variable name is called.

**Note:** I can't imagine when you would want to rename the R1s to R2s, but `echo mv` could easily be replaced with detailed commands for many bioinformatic programs.


##ggplot2 example
Let's take a look at this in practice. Here's the link for a ggplot2 lesson using the Gapminder data set. The first goal is to plot life expectancy as a function of GDP per capita. The instructor walks through the three requirements for the ggplot function (data, aesthetics, and a geometry layer.) Challenge 1 ask asks the students to replace life expectancy with year.  This is a faded example, because its a fill in the blank. Then, you add a color by continent. Then ask the student to color instead by country. Then change geom_point to geom_line. Then add stats, facets, etc. 

http://swcarpentry.github.io/r-novice-gapminder/08-plot-ggplot2.html

Personally, I think the lesson could be a little bit better. You can give the students this cheatsheet, you could see how they could create their own faded example. However, you can see how you can build a step, then ask to fill in the blank, and repeat.

For more examples see the cheatsheet for understanding how one could build a lesson step by step then use faded examples. 

http://www.rstudio.com/wp-content/uploads/2015/03/ggplot2-cheatsheet.pdf

##Faded Example Exercise
1. Get in groups of 2 or 3. 
2. Take a complex line of code from the R ggplot lesson or Python or Unix for loop lesson http://swcarpentry.github.io/r-novice-gapminder/08-plot-ggplot2.html
http://swcarpentry.github.io/python-novice-inflammation/02-loop.html
http://swcarpentry.github.io/shell-novice/04-loop.html
3. Remove 1, 2, then multiple pieces of the code. 
4. Write a question to test the students ability to fill in that blank.
5. Paste you're examples in the etherpad. 

##Faded example Recap
Faded examples work because they introduce the problem-solving strategy piece by piece. At each step, learners have one new problem to tackle. This is less intimidating than a blank screen or a blank sheet of paper. It also encourages learners to think about the similarities and differences between various approaches, which helps create the linkages in the mental model that instructors want them to form.





