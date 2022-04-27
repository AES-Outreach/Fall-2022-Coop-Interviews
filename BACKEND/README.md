
# OutStem Back-End Challenge
Welcome to the OutStem back-end challenge. Submission instructions are listed below. The deadline to submit this challenge is **Wednesday May 25th, 9:00 AM**. We would like to emphasize that we are looking for effort, and that the challenge is just part of our discussion with you during the interview, so don’t worry if your solution is *hacky* or even if it doesn’t work, we want to see it!

*All tasks and characters in this challenge are fictional. The context is made up.*

## The Challenge

> This year, OutStem would like to explore gamified learning by providing an API students can use to play Wordle.

For this challenge you'll be working on writing a Wordle API that supports sessions through a unique session key, as well as validation on user guesses.


For this challenge we will be using a simplified version of the game, where a user tries to guess a 5 letter word with no limit on the number of tries, and the API returns:
- which letters are in the correct position 
- which letters are in the wrong position 
- which letters are not in the word at all

If you are unfamiliar with the Wordle game, here is a link with further details: [Wordle](https://www.washingtonpost.com/video-games/tips/whats-wordle-how-to-play/)


## Endpoints

Your API will have 2 endpoints:

### Generate Session
URL: `/key` 

Method: GET

Description: This endpoint will chose a secret 5 letter word, and provide a session key to the user that lets the user keep making guesses for this word

**Response Body Example:**
*Note: the session key can have the format of your choosing as long as they're unique for the generated word*
```
{
  "session_key": "3912837alskjd198237123"
}
```


### Guess Word
URL: `/guess` 

Method: POST

Description: This endpoint will check the guess against the word associated with the session key and will return the result for this guess

**Request Body Example:**
```
{
  "session_key": "3912837alskjd198237123",
  "guess": "abcde"
}
```

**Response Body Example:**

Where the following letters indicate the following result:
- y: letter is in the correct position 
- m: letter is in the incorrect position  
- n: letter is not in the word at all
```
{
  "result": ["y", "n", "m", "y", "n"]
}
```



## Example

### Getting a key

Request is made to `/key` and the following is returned:

Result: 
```
{
  "session_key": "this_is_a_test_key"
}

```

*The word associated with the key "this_is_a_test_key" is "apple" (this is not known to the user)*

### Guess 1

A request is made to `/guess` with the following request body:

Request Body: 
```
{
  "session_key": "this_is_a_test_key",
  "guess": "spoil"
}

```

And the following is returned:

Response Body: 
```
{
  "result": ["n", "y", "n", "n", "m"]
}

```

### Guess 2

A request is made to `/guess` with the following request body:

Request Body: 
```
{
  "session_key": "this_is_a_test_key",
  "guess": "opals"
}

```


And the following is returned:

Response Body: 
```
{
  "result": ["n", "y", "m", "y", "n"]
}

```

### Guess 3

A request is made to `/guess` with the following request body:

Request Body: 
```
{
  "session_key": "this_is_a_test_key",
  "guess": "apple"
}

```


And the following is returned:

Response Body: 
```
{
  "result": ["y", "y", "y", "y", "y"]
}

```


## Your solution

Here are the requirements for your solution.

1. You can complete this challenge using any language of your choice, however, we prefer to see you do this challenge in JavaScript/TypeScript or Java.
2. Your solution must be able to handle HTTP `GET` requests to fetch a session key. 
3. Your solution must be able to handle HTTP `POST` requests to validate a user guess with a JSON request body.
4. You must submit your solution in a GitHub repository or a Repl.it (recommended). **Please make sure your project/repository is public and accessible by us.**

## Evaluation 

You will be evaluated on:
- Completeness: did you complete the features?
- Correctness: does the functionality act in sensible, thought-out ways?
- Maintainability: is it written in a clean, maintainable way?
- Testing: is the system adequately tested?
- Best Practices: does your solution use Javascript/TypeScript's and your chosen framework's best practices

## Submission

Please submit your solution in the 2022 Fall interview GitHub repository via GitHub Issue. 

1. Navigate to the following link (https://github.com/AES-Outreach/Fall-2022-Coop-Interviews/issues/new/choose) or:
   1. Navigate to the challenge repository
   2. Click **Issues**
   3. Click **New Issue**
2. Click **Get Started** for Solution Submission
3. Change `YOUR_NAME` to your full name in the title field
4. Fill out the form
5. Click **Submit New Issue**
6. Done! Thank you for completing the challenge, we look forward to discussing your solution with you during the interview. 🎉