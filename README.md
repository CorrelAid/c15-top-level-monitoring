# Challenge 15: Top-level Monitoring QA

## Code
Code file used in this challenge is the Notebook c15_monitoring.ipynb in the code folder, with requirements in the txt file.
The main ideas/problems for this challenge can be found below.

## Expected input

* Frequency tables on replies of questions
* Meta data: at what questions respondents left
    

## Monitoring


Monitoring: Comparing Raw and Clean Data

* overall: how many respondents have participated vs. how many “valid” respondents participated
   * Warning if ratio lower than threshold, e.g. 70 %

* per question & subquestion: how does the number of respondents change from raw to clean
   * Warning if ratio lower than threshold, e.g. 70 %

Monitoring “Raw Data” 

* how many have responded (per q & sub_q) 

* attrition rate: how many have aborted the survey
   * when to count respondent as aborted?
   * can we use the time spent on questions to determine this? Eg NA for the time for a question when user aborted before getting to it vs some time value for question left empty when the question was skipped

* how to assess the logical modelling of question —> follow-up question dependencies?

  -  which questions have low participation even though they were not filter questions?
  -  number of expected answers vs answers returned

Monitoring “Clean Data” 

* how many have skipped a question
    - e.g. none of the question battery questions were selected
    - All questions that were shown have a timing but skipped questions do not have a reply.

* attrition rate: how many have aborted the survey

* aborted survey where: first question that was not answered
    * first question (give order of questions to the code) that has no timing, already in columns "last_page" (last question shown)

* Which questions need most time?
    * Are there many abortions at these questions?

* how to assess the logical modelling of question —> follow-up question dependencies?



## To Do
- count aborted surveys
- at which questions most aborts
- visualise:
    - categories of warnings

## Recommendations

- Before publishing the survey, do some test runs with the final survey configuration and check the structure of a test export of the data 
- If possible, record timestamp for start and end of response
- Record timing of each question, and have only one question per page for precise measurements




#diversity-hackathon
