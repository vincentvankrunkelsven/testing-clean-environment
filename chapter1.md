---
title       : Insert the chapter title here
description : Insert the chapter description here
attachments :
  slides_link : https://s3.amazonaws.com/assets.datacamp.com/course/teach/slides_example.pdf

--- type:VideoExercise lang:r xp:50 skills:1
## Analyze movie ratings

*** =video_link
//player.vimeo.com/video/154783078

--- type:MultipleChoiceExercise lang:r xp:50 skills:1
## A really bad movie

Have a look at the plot that showed up in the viewer to the right. Which type of movie has the worst rating assigned to it?

*** =instructions
- Adventure
- Action
- Animation
- Comedy

*** =hint
Have a look at the plot. Which color does the point with the lowest rating have?

*** =pre_exercise_code
```{r}
# The pre exercise code runs code to initialize the user's workspace. You can use it for several things:

# 1. Preload a dataset. The code below will read the csv that is stored at the URL's location.
# The movies variable will be available in the user's console.
movies <- read.csv("http://s3.amazonaws.com/assets.datacamp.com/course/introduction_to_r/movies.csv")

# 2. Pre-load packages, so that users don't have to do this manually.
library(ggplot2)

# 3. Create a plot in the viewer, that students can check out while reading the exercise
ggplot(movies, aes(x = runtime, y = rating, col = genre)) + geom_point()
```

*** =sct
```{r}
# The sct section defines the Submission Correctness Tests (SCTs) used to
# evaluate the student's response. All functions used here are defined in the 
# testwhat R package

msg_bad <- "That is not correct!"
msg_success <- "Exactly! There seems to be a very bad action movie in the dataset."

# Use test_mc() to grade multiple choice exercises. 
# Pass the correct option (Action, option 2 in the instructions) to correct.
# Pass the feedback messages, both positive and negative, to feedback_msgs in the appropriate order.
test_mc(correct = 2, feedback_msgs = c(msg_bad, msg_success, msg_bad, msg_bad)) 
```

--- type:NormalExercise lang:r xp:100 skills:1
## More movies

Empty exercise

*** =instructions
- nothing here

*** =hint
- and nothing here

*** =pre_exercise_code
```{r}

```

*** =sample_code
```{r}

```

*** =solution
```{r}

```

*** =sct
```{r}

success_msg("Good work!")
```
