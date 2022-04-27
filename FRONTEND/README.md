# OutStem Front-end Challenge

Welcome to the OutStem front-end challenge. Submission instructions are listed below. The deadline to submit this challenge is **Wednesday May 25th, 9:00 AM**. We would like to emphasize that we are looking for effort, and that the challenge is just part of our discussion with you during the interview, so don’t worry if your solution is *hacky* or even if it doesn’t work, we want to see it!

## The Challenge


For this challenge, you will be implementing a front end solution for MFA code validation.

Multifactor authentication (MFA) adds a layer of protection to the sign-in process. When accessing accounts or apps, users provide additional identity verification, such as scanning a fingerprint or entering a code received by phone such as in this challenge. [More on MFA](https://www.onelogin.com/learn/what-is-mfa)

The API for MFA code validation will be available at `https://coop-interview.outstem.io/`

Details on this API will be available in the resources section.

## Requirements

*The styling for this challenge is up to you, feel free to use any UI libraries*

This challenge has multiple goals that increase in level of difficulty. Implement as many of these goals as you are able to

### Goal 1: Basic input field with validation
- For this goal, implement a basic input field that only accepts 6 digit numbers
- On submit, the page should validate with the API provided and show correct or incorrect depending on the results

### Goal 2: Error Handling
- Occasionally the MFA validation API will throw a 500 error, ensure that your solution provides the user with good error handling and prompts them to try again at a later time

### Goal 3: Pasting Optimization
- For this goal, the user should be able to copy paste a 6 digit number into the input field and this should automatically trigger the validation of the code

**More Challenging Goals**
### Goal 4: Separate Input Fields
- For this goal, each digit will be given its own input field.
- On submit, the page should validate with the API provided and show correct or incorrect depending on the results

### Goal 5: Chained Pasting
- For this goal, copy pasting a 6 digit number in the first input box should chain these into each input box
- Make sure to look for edge cases to ensure a good user experience

### Goal 6: Pasting Optimization
- For this goal, when the user pastes a 6 digit number into the first input box, it should chain these numbers into each input box and automatically trigger the validation of the code

### Goal 7: Pasting Optimization
- For this goal, add a password mode the user can enable that masks the inputs with an asterisk instead of showing the digits




### Bonuses

- Make your UI responsive, that is usable of all screen sizes
- Implement any other features you think would provide a better MFA experience

## Your solution

Here are the requirements for your solution.

1. You can complete this challenge using any front end framework of your choice, however, we prefer to see you do this challenge in JavaScript/TypeScript and Angular.
2. Your solution submission should indicate which goals you've achieved
4. You must submit your solution in a GitHub repository or a Repl.it (recommended). **Please make sure your project/repository is public and accessible by us.**

## Evaluation 

You will be evaluated on:
- Completeness: did you complete the features?
- Correctness: does the functionality act in sensible, thought-out ways?
- Maintainability: is it written in a clean, maintainable way?
- Testing: is the system adequately tested?
- Best Practices: does your solution use Javascript/TypeScript's and your chosen framework's best practices
- User Friendly UI: does your solution anticipate what users might need to do and have elements that are easy to access?

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
## Resources

### Testing API Documentation

**URL**: `https://coop-interview.outstem.io/`
**Method** POST

**Request Body Example**

```
{
   "code": "123456"
}
```

**Response Body Example**

```

{
   "valid": true
}
```

#### Test Data
We have hard-coded a few MFA codes to provide you test cases for your solution:

Correct MFA Code: 123456

Throw an 500 error MFA Code: 000000



