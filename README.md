# Guide to generate a Quiz

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