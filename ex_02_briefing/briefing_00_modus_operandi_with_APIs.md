# Usual way of operating when working with APIs

We've created a component, the component has called an outside API, that API sends data back to us, and then from there, we render the data out into the screen after putting it inside of that local component state.

```
export default class BlogDetail extends Component {
  constructor(props) {
    super(props);

    this.state = {
      currentId: this.props.match.params.slug,
      blogItem: {}
    };
  }

  getBlogItem() {
    axios
      .get(
        `https://jordan.devcamp.space/portfolio/portfolio_blogs/${this.state
          .currentId}`
      )
      .then(response => {
        this.setState({
          blogItem: response.data.portfolio_blog
        });
      })
      .catch(error => {
        console.log("getBlogItem error", error);
      });
  }

  componentDidMount() {
    this.getBlogItem();
  }

  render() {
    const {
      title,
      content,
      featured_image_url,
      blog_status
    } = this.state.blogItem;

    return (
      <div>
        <h1>{title}</h1>
        <img src={featured_image_url} />
        <div>{content}</div>
      </div>
    );
  }
}
```
