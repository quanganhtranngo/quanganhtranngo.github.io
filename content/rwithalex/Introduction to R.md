---
title: "Introduction to R"
output: html_document
author: Alex Tran (Tran Ngo Quang Anh)
date: "`r Sys.Date()`"
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

Welcome to my blog - R with Alex (or Rawlex for short. Don't worry, I'll make the name stick). In this blog, I will (hopefully) acquaint you with R and its application for data analysis, with multiple examples. Most of my examples will be drawn from datasests from Psychology, because that is my domain of specialty. However, you can apply these principles to apply to your own analysis and answer your own research questions from other disciplines.

## Don't fear

It is normal to feel overwhelmed and fearful as you start learning a new language. The process is similar to learning a foreign language. In fact, think of R as a foreign language. Without any knowledge, foreign language can look and sound like gibberish to you. After learning and consistently practicing, you start to understand. Better yet, you will be able to communicate with others using that language. R is the same. It may be a little difficult at the beginning but you will get yourself familiar with it in no time. In fact, students who have started learning R showed neutral to positive attitudes towards R. Many find R valuable and they feel competent (which you are!) after being able to use R (Counsell & Cribbie, 2020; Tucker et al., 2022). The key is to sustain your engagement with R overtime (Tucker et al., 2022). In other words, practice, practice, and practice (Tucker et al., 2022).

## Why R

These are just a few reasons:
- Free and open-source
- User-created packages make it easy to conduct even more complicated analysis.
- Flexible and wide range of uses
- Better data visualization (the graphs look really pretty!)
- Highly valued skill in academia and industry

However, unlike other (paid) services (e.g., SPSS), R do not have a point-and-click system, but it is a powerful tool to conduct more complicated analysis efficiently and quickly. Once you learn the basics, you can teach yourself to do even more with R. 

## Positionality

For answering why make a positionality statement, read Qin (2016).

Before I engage in writing these blogs, in the spirit of self-reflexivity, I acknowledge my standpoint as an international Ph.D. student from Vietnam studying Social Psychology at Indiana University Bloomington. 

Being an international student informs my choice of blogs as a form of education. I come from an education system in which obedience and silence are valued. Teachers expected me to listen to their demands in class and my silence while attending the lectures was always met with praises. However, that all changed when I came to the U.S., where participation is encouraged and often part of the evaluation. Having difficulty adjusting, I needed more time collecting my thoughts. This resulted in my failure to constantly follow the fast pace of the American classroom. Now, after 5 years of acquainting myself with the U.S. education system, I found blogging as an effective form of education for three reasons: (1) it can reach a wider and different set of audiences; (2) it avoids the heavy academic jargon that often prevents non-academic folks from participating/reading; (3) it has been shown to increase students' engagement and participation (Brownstein & Klein, 2006; Shaohui & Lihua, 2008). Furthermore, there is a fourth reason that resonated with my experience: the asynchronicity of blogging allows learners to learn at their own pace. I hope for these reasons, you will also benefit from learning from my blog.
Experiencing Vietnamese education also allowed me to appreciate the growth mindset my teachers promoted. For us Vietnamese students, naturally endowed intelligence (e.g., genetics) matters less than individual efforts. As long as I work hard, I will succeed. This is the mindset I am carrying into these blogs. Learning R requires effort and consistency. Practice with me regularly and I promise you can learn how to use R. Forget about the "math gene," you do not need that.

As a scholar, I have a special interest in education and teaching and I believe in evidence-based teaching, teaching practices that are informed by research. That is why, throughout these blogs, you will see citations, with a complete bibliography at the end for your reference. My research interests broadly involves the perception of minoritized individuals with intersecting identities, which informs the data I choose as practice and demonstrative exercises in these blogs. I will feature more research from scholars of colors, whose research are rigorous and informative but have been more invisible in the common discourse than their White counterparts' (Roberts et al., 2020).


## Structure

The structure of each of these blog will be as followed:
1, Each blog will be opened with a short introduction, followed by the outlined goals of each blog.
2, The content of that blog (e.g., how to produce descriptive statistics with R) along with examples
3, Exercises for you to try for yourself
4, Recommended readings (if any)
5, Bibliography 
Blogging is always a work in progress. Thus, if you have anything to add, don't hesitate to let me know through my contacts.

## Goals for this module

By the end of this module, you will 
1, Understand what R and R Studio are and how to install them successfully on your device.
2, Familiarize yourself with the R Studio Interface.
3, Understand what R packages are, how to install them and learn about them.

## Let's get started! Downloading R and R Studio

You already know R is a programming language used to perform statistical computing. R Studio is an Integrated Development Environment (IDE) to make it easier and more efficient and execute R codes. Think of R Studio like Microsoft Word, but instead of helping writing English, it helps you write R (Wickman & Grolemund, 2014). When we use R, most of the times I am actually referring to using R Studio. Screenshots in this blog will also be from the R Studio interface.

Here is the link and instructions on how to download R and R Studio:

Here is the [link](https://cran.r-project.org/) to download R. Remember to pick the right R for your operating system: Windows, Mac, or Linux.
![Website for Downloading R](C:/Users/linht/Downloads/Rblog/R.png)

Here is the [link](https://posit.co/products/open-source/rstudio/) to download R Studio. Remember, although you mostly use R Studio, you cannot use R Studio without downloading R.
![Website for Downloading R Studio](C:/Users/linht/Downloads/RBlog/RStudio.png)

Have you downloaded and installed them yet? Great! Now let's open R Studio and start learning R. 

## The R Studio Interface

Great job on finishing the first step to a great journey of education. Your screen should look something like this after you have opened R Studio.
![R Studio Interface](C:/Users/linht/Downloads/RBlog/RStudioInterface.png)
In order to start writing in RStudio, it is highly recommended that you use R Script. This is because of several reasons:

(1) Reproducibility: R scripts allow you to document your codes. By writing code in a script, you can easily reproduce your analysis in the future or share it with others. 

(2) Version control: R scripts allows you to track changes, collaborate with others, and revert to previous versions if needed. This is particularly useful when working on projects with multiple team members or when you want to maintain a history of your code changes.

(3) Scalability: R scripts provide flexibility for working with large datasets or performing computationally intensive tasks.

In order to do that, you would go to File -> New File -> R Script

After you have created your R Script, you will see your screen divided into 4 main parts.

(1) In the upper left corner is your R Script file. This is where you write and edit your R code. A helpful tip: you can highlight and run any parts of code by using Ctrl+Enter (Windows) or Cmd+Enter (Mac).

(2) In the lower left corner is your Console. The console displays the output of your R code, including error messages, warnings, and results. It also maintains a command history, allowing you to refer back to previous commands and results.

(3) In the upper right corner are your Environment and History panes. These panes provide information about your R session. The Environment pane displays objects, variables, and data frames that are currently in your workspace. You can view and manipulate these objects, such as inspecting their values or removing them. The History pane shows a history of your executed commands in the console, making it easy to revisit and re-execute previous commands.

(4) In the lower right corner are your Files, Plots, Packages, and Help panes. These panes provide additional functionality and information. The Files pane allows you to navigate and manage your files and folders. The Plots pane displays any generated plots or graphics. The Packages pane shows the installed R packages and allows you to install, update, or load/unload packages. The Help pane provides access to R documentation and help files, offering detailed information about R functions, packages, and topics.

And just like that, you are familiar with the R Studio Inferface.
![R Studio Interface](C:/Users/linht/Downloads/RBlog/RStudio4Q.png)

## R Packages

Alright, one last thing before we finish our Introduction to R: R Packages.
R Packages are "collections of functions, data, and documentation that extends the capabilities of base R" (Wickman & Grolemund, 2014). This is the beauty of R because, thanks to these packages, our data analysis can happen much faster and more intuitive from simplified codes. They allow you to perform functions that others have created, access datasets, and create the most beautiful data visualizations. 

Throughout our journey, we will use a lot of packages. You can install any packages you see in my future blogs using these codes. For example, we will the package "tidyr" a lot. We will install them as follows.

```
install.packages("tidyr")
```

After you have installed them, you would have to load them in in order to use them. I suggest not loading every package you have in, just the ones you are using, to save your computer's power to do analyses. You can load in the packages you have installed using the following codes.

```{R package loading}
library(tidyr)
```

Finally, once you have the package, you can learn more about what the packages are and how to use them using the following codes.

```
?tidyr
```

These codes apply for any packages you will use in the future. So, do not worry, you will get lots of practice.

## Concluding words

Congratulations on finishing your Introduction to R with me, Alex. In this session, you have learned about what R is, how R is useful, how to install R and R Studio, familiarized yourself with the R interface, and learned how to install and understand R packages. There are no exercises for this session, but here are some recommendations for you to further familiarize yourself with today's content.

## Practice makes perfect

(1) Create a new R Script, name it "HelloWorld," and save it to your R Folder.
(2) Install the following R packages: dplyr, psych, rio
(3) Understand what each of the previous R packages do.
(4) Create a list of what you want to learn from R and use those as your goals to guide you as you learn R with me.
(5) Identify 1-2 papers in your discipline that use R. Why did they use R?

## References

Brownstein, E., & Klein, R. (2006). Blogs. Journal of College Science Teaching, 35(6), 18–22.

Counsell, A., & Cribbie, R. A. (2020). Students’ Attitudes toward Learning Statistics with R. Psychology Teaching Review, 26(2), 36–56.

Grolemund, G., & Wickham, H. (2014). Hands-On Programming with R: Write Your Own Functions and Simulations. O’Reilly Media.

Qin, D. (2016). Positionality. In The Wiley Blackwell Encyclopedia of Gender and Sexuality Studies (pp. 1–2). John Wiley & Sons, Ltd. https://doi.org/10.1002/9781118663219.wbegss619

Roberts, S. O., Bareket-Shavit, C., Dollins, F. A., Goldie, P. D., & Mortenson, E. (2020). Racial Inequality in Psychological Research: Trends of the Past and Recommendations for the Future. Perspectives on Psychological Science, 15(6), 1295–1309. https://doi.org/10.1177/1745691620927709

Shaohui, W., & Lihua, M. (2008). The Application of Blog in Modern Education. 2008 International Conference on Computer Science and Software Engineering, 4, 1083–1085. https://doi.org/10.1109/CSSE.2008.1443

Tucker, M. C., Shaw, S. T., Son, J. Y., & Stigler, J. W. (2023). Teaching Statistics and Data Analysis with R. Journal of Statistics and Data Science Education, 31(1), 18–32. https://doi.org/10.1080/26939169.2022.2089410
