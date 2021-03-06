# Guide to generate a Quiz

## Intro

In this repo the raw quiz data for the vogella Quiz App ist maintained.

Each quiz is assigned to a course category id.
The server then assigns a quiz to a course according to the category id and sorts the quizzes according to the course structure.

The name of the yaml file will not be used for the assignment of a quiz to a course or the ordering of the quizzes in a course.
Nevertheless for maintenance reasons a prefix of the underlying course should be set upfront. e.g.:
* `rcp_` for the Rich Client Platform course
* `flutter_` for the Flutter course
* `plugin_` for the Eclipse IDE extensions course

The following will give an introduction on how to create a quiz for a category in a course.

## Header

* assign the categoryId to which the quiz is for by: `categoryId: **categoryId**` 
* assign a name to the quiz by `name: **name**`

## Questions

`questions` consist of:
* `description`: the description of the question
* `choices`: 2 to 4 choices can be defined. For number of choices less than 4, add missing choices as `NULL` at the end.
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
      - # Choice C or NULL
      - # Choice D or NULL
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