# Destructuring part 2

As a reminder, you can assign all values in an object at the same time if you know another object has that data.

For example, we'll have an object coming from an API and we want to populate the contents of a var we are going to use with it, it would be done like this:

```
const BlogItem = props => {
  const {
    id,
    blog_status,
    content,
    title,
    featured_image_url
  } = props.blogItem
}
```
