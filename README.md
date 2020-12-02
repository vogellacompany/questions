# Guide to generate a Quiz

## Intro

This is a repo for Quiz App @vogella to obtain raw quiz data. The assignment of the quiz to a category in course is achieved by fetching from KnowledgeForge server, and later processed by server according to the `categoryId`.

The following will give an introduction on how to create a test for a category in Training course.

## Header

* assign the categoryId to which the quiz is for by: `categoryId: **categoryId**` 
* assign a name to the quiz by `name: **name**`

## Question

* the `questions` is a set for object `question` 
* one object `question` consist `description`, `choices`, `hint`, `explanation`, `correctChoice`
* `description`: the description of the question
* `choices`: four choices designed for the question
* `hint`: a hint for user to get the answer, if does not exist then please put `NULL`
* `explanation`: an explanation for the answer, if does not exist then please put `NULL`
* `correctChoice`: the id for the correct choice, range 0-3
  
## Template

```yaml
categoryId: # CategoryId
name: # QuizName
questions:
  - description: # Question Description
    choices:
      - # Choice A
      - # Chocie B
      - # Choice C
      - # Choice D
    hint: # hint
    explanation: # explanation
    correctChoice: # choiceId
  - description: # Question Description
    choices:
      - # Choice A
      - # Chocie B
      - # Choice C
      - # Choice D
    hint: # hint
    explanation: # explanation
    correctChoice: # choiceId
  - description: # Question Description
    choices:
      - # Choice A
      - # Chocie B
      - # Choice C
      - # Choice D
    hint: # hint
    explanation: # explanation
    correctChoice: # choiceId
...
```