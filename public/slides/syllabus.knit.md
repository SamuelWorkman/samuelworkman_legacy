---
title: "Maximum Likelihood Estimation"
author: "Samuel Workman, Ph.D."
date: '2020-10-08'
output: 
  html_document:
    css: my_style.css
---



------------------------------------------------------------------------
<div class = "row">
      
<div class = "col-md-6">
<br><!--html_preserve--><i class="fas  fa-envelope "></i><!--/html_preserve--> [samuel.workman@ou.edu](mailto:samuel.workman@ou.edu)
<br><!--html_preserve--><i class="fas  fa-globe-americas "></i><!--/html_preserve--> [samuelworkman.org](https://www.samuelworkman.org)
<br><!--html_preserve--><i class="fab  fa-medium "></i><!--/html_preserve--> @[samuel.workman](https://www.medium.com/@samuel.workman)
<br><!--html_preserve--><i class="fab  fa-twitter "></i><!--/html_preserve--> @[SamuelGWorkman](https://www.twitter.com/SamuelGWorkman)
</div>
      
<div class = "col-md-6">
<br>Office Hours: Remote & By Appointment
<br>Class Sessions: Asynchronous
<br>Office: Remote
<br>Classroom: Remote
</div>
</div>
------------------------------------------------------------------------

## Course Description

The vast majority of data of interest to social scientists do not fit into the Gaussian assumptions of the classic normal regression model taught in introductory statistics courses. Data often diverge drastically from the continuous, normally distributed outcomes associated with the classic model. Common data of interest display binary, ordinal, or nominal outcomes. In addition, data are often correlated across space, time, or are nested, making applications of the classic model difficult. More importantly, the application of the classic model to data of this type often leads to confusing, strained, or nonsensical interpretations of analyses. That is, the classic model applied to this data makes *substantive* interpretation of findings difficult---a major problem when communicating research findings in the academy or to policy makers charged with decision-making. This course will introduce the students to maximum likelihood methods that can be more broadly applied to social science data. Throughout, we will emphasize the communication of these models for substantive import of the findings and decision-making.

There are no specific prerequisites for this course, although familiarity with the classic regression model, such as taught in P SC 5913 & 5933, is helpful. Students should also be ready to make themselves comfortable with matrix algebra, probability, and working with exponents and logs in deriving likelihood functions. All needed math and coding will be demonstrated and covered in class. Students will implement the techniques from the course using freely available statistical programs. Students should also be ready to work with their own data.

# Jump to Section {.tabset .tabset-fade .tabset-pills}

## Texts

* King, Gary. 1998. *Unifying Political Methodology*. Ann Arbor, MI: University of Michigan Press.
* Ward, Michael D. and John S. Ahlquist. 2018. *Maximum Likelihood for Social Science: Strategies for Analysis*. Cambridge: Cambridge University Press.

## Course Requirements

The course requirements are geared towards developing students' skills in the entire range of research, analysis, and storytelling with data. The assignments promote the development of the conduct and presentation of research results, including intuitive data visualization. In addition to these, the assignments develop students' ability to synthesize and integrate theories, ideas, and existing research pertaining to these. The course is asynchronous and designed such that students can work their way through the material at their own pace while still being about to interact with their peers. Each section of the course will consist of a module addressing MLE for particular data-generating processes. Within each module, one or more vignettes will address the practical implementation of these approaches to data using <!--html_preserve--><i class="fab  fa-r-project "></i><!--/html_preserve-->.

*Participation*. We will meet as a group on Zoom 2--4 times this semester. In addition, students will be availed of individual meetings with the professor. During meetings of the class and one-on-one with the professor, students are expected to have read the material, watched any related videos posted by the professor, and attempted to work through vignettes on their own.

*Vignettes*. Each student will develop 2 vignettes of their own that address methods covered in the modules. This means that the student will have to identify a suitable data source for vignettes. The student will then construct their own vignette, complete with code that teaches the reader how to apply the method or model. Data for the vignettes need not pertain to the social sciences or the student's research.

*Research Project*. Over the course of the semester, students will write a research paper. These papers will contain a question of interest, description of the data to be used to answer the question, justification of the method used to analyze the data, and findings employing presentation techniques learned in the class. These papers need not contain fully developed theory and literature review sections (though they could if the student chooses).

The table below displays the grading policy. Since the course is asynchronous, students work at their own pace and due dates reflect the final day to turn in an assignment. Please note that this means students may work ahead and finish the course early as well. ***Students may work together in teams of up to 3 for ALL assignments. Be aware that team membership is permanent if the student chooses and all members of the team will be given the same grade for each assignment. If choosing to work in teams, meetings and participation on Zoom will include everyone in the project team.***

<table class="table table-striped table-hover table-condensed table-responsive" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> Requirement </th>
   <th style="text-align:right;"> Points </th>
   <th style="text-align:right;"> Percent (\%) </th>
   <th style="text-align:left;"> Due Dates </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Participation </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:left;"> When Scheduled </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Vignettes </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 40 </td>
   <td style="text-align:left;"> By Wednesday, November 18 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Research Project </td>
   <td style="text-align:right;"> 50 </td>
   <td style="text-align:right;"> 50 </td>
   <td style="text-align:left;"> By Monday, December 7 </td>
  </tr>
</tbody>
</table>

There are an even 100 points possible in the course. This means that determining and keeping track of your grade is very easy. Please be aware of where you stand in the course with your grade. The points available will be allocated across a range of activities that are designed to foster the skills development outlined above.

**Written Assignments**: 90 points. There will be three, short vignettes that pertain to the texts, our discussion, example <!--html_preserve--><i class="fab  fa-r-project "></i><!--/html_preserve--> code, and your research project. These vignettes should be 2-5 pages single spaced, but are not walls of text, tables, figures, equations, should be sprinkled throughout.

**Participation \& Discussion**: 10 points. Students will engage the professor and their peers in discussion and analysis of the texts, working through <!--html_preserve--><i class="fab  fa-r-project "></i><!--/html_preserve--> code, and development of statistical and presentational procedures.

## Course Policies

### Late & Make-up Policy

All  assignments  are  due  on  time.  Since  all  assignments  are  specified  well  in  advance, or alternatively are completed contemporaneously, late assignments will not be accepted and will receive a grade of zero. Exceptions for late work will be granted for only the most dire of circumstances.

### Professional Communications

Most general course administration questions can be answered by referring to the syllabus. I tend to respond to student email only once every 24 hours. Depending on when I check my email on a given day, the earliest time at which a response may be expected is within 24 hours. Please be aware that I also do not respond to emails on weekends or holidays.

## University Policies

### Religious Observances

The University's policy with regard to religious observances is as follows: "It is the policy of the University to excuse the absences of students that result from religious observances and to provide without penalty for the rescheduling of examinations and additional required class work that may fall on religious holidays."

Students should notify the Professor of a pending absence by the second meeting of the class. Since religious observances are specified well in advance of the academic calendar, students should communicate this well in advance of important dates for the course.

### Academic Dishonesty

Students who violate University rules on scholastic dishonesty are subject to disciplinary penalties and action, including the possibility of failure in the  course and/or dismissal from the University. Since such dishonesty harms the individual, all students, and the integrity ofthe University, policies on scholastic dishonesty will be strictly enforced and pursued to the maximum extent.

### Reasonable Acommodations Policy

*Students must initiate their request for reasonable accommodations through the Disability Resource Center (DRC).* Students must alert the professor immediately if planning for reasonable accommodations. Upon the granting of reasonable accommodations by DRC, students will be given an opportunity to demonstrate their abilities and proficiency in meeting course requirements and expectations.

### Adjustments for Pregnancy \& Childbirth Related Issues

Should you need modifications or adjustments to your course requirements because of documented pregnancy-related or childbirth-related issues, please contact me as soon as possible to discuss.  Generally, modifications will be made where medically necessary and similar in scope to accommodations based on temporary disability.  [Please see the pregnancy faqs for commonly asked questions.](www.ou.edu/content/eoo/faqs/pregnancy-faqs.html)

### Title IX Resources

For any concerns regarding gender-based discrimination, sexual harassment, sexual misconduct, stalking, or intimate partner violence, the University offers a variety of resources, including advocates on-call 24/7, counseling services, mutual no contact orders, scheduling adjustments and disciplinary sanctions against the perpetrator.  Please contact the Sexual Misconduct Office 405-325-2215 (8--5, M--F) or OU Advocates 405-615-0013 (24/7) to learn more or to report an incident.

## Course Schedule

Students will work through each of the modules below. Once constructed, slides, video, and vignettes applying the methods will be linked below each module in the syllabus. These will also be warehoused on Canvas. Students may work through each module at their own pace and are encouraged to work together.

### Modules {.tabset .tabset-fade .tabset-pills}

#### Module 1. Introduction & Logic of Maximum Likelihood

Reading: King, Chapter 1 & 2; Ward & Ahlquist Chapter 1 & 2.

Workman, [Four Principles of Data Collection](https://towardsdatascience.com/four-principles-of-data-collection-82ad07938ac1)

##### Slides

[Introduction](../../../slides/intro_slides.html#1)

[Introduction on YouTube](https://youtu.be/5Y1t3fb-Rm0)

[Basic Probability & Mathematics for Likelihood](../../../slides/likelihood_math.html#1)

[Basic Probability & Mathematics for Likelihood on YouTube](https://youtu.be/wwe_U7z3sKY)

[Classic Approach to Analysis](../../../slides/classical_approach.html)

[Classic Approach to Analysis on <i class="fa fa-youtube"></i>]{https://youtu.be/NXafc2vNU6I}

<!---
<!--html_preserve--><div class="shareagain" style="min-width:300px;margin:1em auto;">
<iframe src="../../../slides/likelihood_math.html" width="100" height="75" style="border:2px solid currentColor;" loading="lazy" allowfullscreen></iframe>
<script>fitvids('.shareagain', {players: 'iframe'});</script>
</div><!--/html_preserve-->
-->


##### Gary King's Take

<iframe width="162" height="100" src="https://www.youtube.com/embed/qs2uCuDL2OQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="162" height="100" src="https://www.youtube.com/embed/qbxNf4iqJPo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="162" height="100" src="https://www.youtube.com/embed/kaL1KzDTotc" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="162" height="100" src="https://www.youtube.com/embed/6C7yRBfh2ok" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Module 2. Maximum Likelihood for Continuous Outcomes 
