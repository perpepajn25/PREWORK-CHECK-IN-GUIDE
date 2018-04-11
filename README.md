# Pre-Work Check Ins

The purpose of the pre-work check in is to ensure that a student is ready for Day 1. It is our chance to assess the student's pre-work progress and confirm a student's readiness to join the in person immersive. It is also an opportunity to identify students that might need more support early on.


## Setup

The manager of faculty for that campus will reach out to instructors on-site if students need a pre-work check-in. When an instructor volunteers, the faculty manager invites both the student and the assigned instructor to a meeting. The instructor will then follow up with an email to the student containing a zoom meeting link the morning of the check-in.

##### Example
```
"Hello [Student Name],

My name is [Instructor Name] and I will be checking in with you at [time] today. Please have the Hashketball lab open and ready to review.

You can use this link to join the zoom meeting at [time]: [insert zoom link].

I look forward to speaking with you soon!

Best,
[Instructor Name]"
```

#### If the student has not finished Hashketball?

In the event that the student has not finished the Hashketball lab prior to your check-in, use this time to gauge where the student is currently. Ask them which lab they are currently on.

See how they do with iterations:

How can we pick out only the odd numbers from an array of integers?

```
[1,2,3,4,5].select do |num|
  num.odd?
  ##or num % 2 != 0
end
```

Students may also use `.each` and push all the odd numbers into a new array which is okay, just mention that there might be a better solution.

Ask to schedule another check-in with the student no later than Friday morning of that week. This will allow enough time for communication between admissions and the student if the student is still not up to pace and needs to defer to a later date. Use the information gathered from this check-in and their position in the pre-work to help dictate how much time to give the student before the next check-in. Emphasize the importance of getting through Hashketball prior to the next check-in.


### Hashketball Review

##### Overview
Pre-work check-ins should only last about 20-30 min.
  1. **5min** Intro
  2. **5min** Review of an already written method
  3. **10min** Write a new method using the game_hash
  4. **5min** Address any questions or concerns
  TOTAL: 25min give or take

###### Intro

Ask the student how they are feeling about the pre-work. This is the an opportunity to possibly find out if something is hindering their completion of the pre-work and if our team can further support. Let the student know that we will take the first few minutes reviewing a method that is already written and we'll take the next 10 minutes writing a new method similar to the ones already written.

###### Review

This is an opportunity for a student to walk you through a method they have already written: either `shoe_size` or `num_points_scored`. Instead of asking pointed questions, let the student walk you through the method line by line - this will allow the student to demonstrate their knowledge and you can ensure that the student didn't copy a previous solution.

##### Write a new method

Ask the student to write a new method: player_by_number(num). This method should return the name of the first player that has the number given as an argument from either team.

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

Questions to ask are: why did you choose that iterator? what are the arguments of that iterator? what does that iterator return?

Use this time to understand a student's process in approaching the new problem. This could be beneficial to the lead and instructional team for that new cohort. It is also a good teaching moment - course correct the `sandwich pattern` if it exists. Are their better iterators we could have used? How could we have split this method up by using helper method?(ex: `players` that returns an array of players)


###### Wrap Up

Use the last few minutes to discuss the student's game plan for completion of the rest of the labs before the program.
  'What time do you work best?'
  'How can you use Google and AAQ feature to assist you?'

After completing the check-in, slack any updates or feedback to the manager of faculty for that campus.
