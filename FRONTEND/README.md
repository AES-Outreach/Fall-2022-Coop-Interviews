# OutStem Front-end Challenge

Welcome to the OutStem front-end challenge. Submission instructions are listed below. The deadline to submit this challenge is **Wednesday May 25th, 9:00 AM**. We would like to emphasize that we are looking for effort, and that the challenge is just part of our discussion with you during the interview, so don’t worry if your solution is *hacky* or even if it doesn’t work, we want to see it!

## Challenge - Star Wars University face book pagination

For this challenge, you will be implementing the pagination feature for the new Star Wars University face book. ([What's a university face book?](https://en.wikipedia.org/wiki/Face_book)).

Pagination happens when we divide the data into discrete pages and load them one at a time. It is a crucial optimization tool we use to improve the performance of our service and give users a better experience. We would like to see how you will implement such a feature. [Here is an example of load more pagination, the example works on scroll, your implementation does not have to.](https://connekthq.com/plugins/ajax-load-more/examples/rest-api-example/)

This challenge is done on CodeSandbox where you fork the base project and make all necessary changes. **Note: you can modify any of the existing code in the project. You do not need to use any of the existing methods, and you are allowed to change them however you like.**

Finally, the data of this challenge is provided by [*SWAPI - The Star Wars API*](https://swapi.dev/). We will add a link to their documentation in the resource section.

### Requirements

- The app shall load the next page of people data from the API when user clicks `Load next page`.
- The app shall not show the `load next page` button if the user has reached the last page of the data. *(Hint: watch the `next` property in the JSON response)*
- The app shall be implemented with Angular and Typescript, you may use additional libraries to adi your process.

### Bonuses

- Use RxJS and observable recipes instead of promises for the data pipeline.
- Display a loading indicator when loading data.
- Add a search functionality that allows users to search for a person by their name (*Hint: the API has a search functionality*)
- Improve the UX of the loading next page button. (Use infinite scrolling, load the data predictively to speed up user interaction, etc.)
- Improve the styling of the app.

## Submission
**Challenge CodeSandbox URL: https://codesandbox.io/s/outstem-frontend-challenge-2022-summer-875l5**

The challenge must be completed on CodeSandbox, and the final submission shall be a CodeSandbox URL. We recommend that you sign up for an account with CodeSandbox to make sure your project is properly saved, however, it's fine if you want to proceed without signing up.

### Steps

1. Open the link above
2. Fork the project by pressing the `Fork` button on the top right of the page.
3. Do the challenge!
4. Navigate to the following link (https://github.com/aes-outreach/summer-2022-interviews/issues/new/choose) or:
   1. Navigate to the challenge repository
   2. Click **Issues**
   3. Click **New Issue**
5. Click **Get Started** for Solution Submission
6. Change `YOUR_NAME` to your full name in the title field
7. Fill out the form
8. Click **Submit New Issue**
9. Done! Thank you for completing the challenge, we look forward to discussing your solution with you during the interview. 🎉

## Resources
- [Angular documentation](https://angular.io/docs)
- [SWAPI (API) documentation](https://swapi.dev/documentation)
- [RxJS help guides](https://www.learnrxjs.io/)
- [CodeSandbox Documentation](https://codesandbox.io/docs)
