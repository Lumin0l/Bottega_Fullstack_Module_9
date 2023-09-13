# Dynamic Axios

There is a way to make dynamic axios requests by passinf config to the axios. Passing **props** to the axios instead of the api url directlyu. Like here:

```
this.state = {
  name: "",
  description: "",
  category: "eCommerce",
  position: "",
  url: "",


// Config
  editMode: true,
  apiUrl: "https://jordan.devcamp.space/portfolio/portfolio_items/${id}",
  apiAction: "post"


// Axios
axios({
    method: this.state.apiAction,,
    url: this.state.apiUrl,
    data: this.buildForm(),
    withCredentials: true
  }).then(response => {
      this.props.handleSuccessfulFormSubmission(response.data.portfolio_item);
};
```

That way we can assign a different method, like patch, to the another component then we pass different props and it will perform a different action.
