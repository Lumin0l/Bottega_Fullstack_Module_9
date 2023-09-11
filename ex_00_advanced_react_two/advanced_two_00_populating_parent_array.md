# Populating Parent Array in React

If you have a function that gets some data and wants to add that to an existing array, like, in state for example, you can't add it normally.

First you need to convert whatever data is comming into an array, and then react will be able to add it to other arrays:

```
handleSuccessfulFormSubmission(portfolioItem) {
  this.setState({
    portfolioItems: [portfolioItem].concat(this.state.portfolioItems)
  });
}
```
