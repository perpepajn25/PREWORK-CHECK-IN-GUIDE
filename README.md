# Pre-Work Check Ins

The purpose of a pre-work check-in is to ensure that a student is ready for Day 1. It is our chance to assess the student's progress with the pre-work material and confirm the student's readiness to join the in-person immersive program. It is also an opportunity to identify students that might need more support from early on.


## Setup

The manager of faculty for that campus will reach out to instructors on sight if students need a pre-work check-in. When an instructor volunteers, the faculty manager invites both the student and the assigned instructor to a meeting. The instructor will then follow up with an email to the student containing a Zoom meeting link the morning of the check-in.

##### Example
```
"Hello [Student Name],

My name is [Instructor Name] and I will be checking in with you at [time] today. Please have the Hashketball lab open and ready to review.

You can use this link to join the zoom meeting at [time]: [insert Zoom link].

I look forward to speaking with you soon!

Best,
[Instructor Name]"
```

#### If the student has not finished Hashketball

In the event that the student has not finished the Hashketball lab prior to your check-in, use this time to gauge where the student is currently. Ask them which lab they are currently on and have them try to review and explain their code for that lab instead.

See how they do with iterations:

How can we pick out only the odd numbers from an array of intergers?

```
[1,2,3,4,5].select do |num|
  num.odd?
  ##or num % 2 != 0
end
```

Students may also use `.each` and push all the odd numbers into a new array which is acceptable but keep in mind it would be worth mentioning that there might be a more concise solution.

Following this review, schedule another check-in with the student no later than Friday morning of that week. This will allow enough time for communication between admissions and the student. If the student is still not up to pace, the student may need to defer to a later date. Use the information gathered from this check-in and their position in the pre-work to help dictate how much time to give the student before the next check-in. Emphasize the importance of getting through Hashketball prior to the next check-in. Follow up with the manager of faculty with that campus with the feedback from this check-in and the newly scheduled follow-up check-in. 


### Hashketball Review

##### Overview

Pre-work check-ins should only last about 20-30 min.
 ```
  **5min** Intro
  **5min** Review of an existing method from the lab
  **10min** Ask the student to write a new method using the game_hash
  **5min** Address any questions or concerns
  --
  TOTAL: Approximately 25m
 ```

###### Intro

Ask the student how they are feeling about the pre-work. This is an opportunity to find out if something is hindering their completion of the pre-work and if our team can provide further support. Let the student know that we will take the first few minutes reviewing a method that is already written and we'll take the next 10min writing a new method similar to ones already required from the lab.

###### Review

This is an opportunity for a student to walk you through a method they have already written: either `shoe_size` or `num_points_scored`. Instead of asking pointed questions, let the student walk you through the method line by line - this will allow the student to demonstrate their knowledge and you can ensure that the student didn't copy a previous solution.

##### Write a new method

Ask the student to write a new method: player_by_number(num). This method should take in a number as an argument and return the name of the first player from either team that has that number.

```
def player_by_number(num)
  ## get all the players
  players = game_hash.map do |team_key, team_value|
    team_value[:players]
  end.flatten
  ## find the player who's number matches the argument
  players.find do |player|
    player[:number] == num
  end.fetch(:player_name)
end

player_by_number(33)
=> "Brendan Haywood"
```

Questions to ask are: Why did you choose this iterator? What are the arguments of this iterator? What does this iterator return?

Use this time to understand a student's process in approaching the new problem. This could be beneficial to the lead and instructional team for that new cohort. It is also a good teaching moment - course-correct the `sandwich pattern` if it is apparent the student is using that appraoch. Are there better iterators that could have been implemented? Could we have split this method up by using helper method?(ex: `players` that returns an array of players)


###### Wrap Up

Use the last few minutes to discuss the student's game plan for completing the rest of the labs before the program.
  'What time do you work best?'
  'How can you use Goodle and the AAQ feature to assist you?'

After completing the check-in, slack any updates or feedback to the manager of faculty for that campus. 
