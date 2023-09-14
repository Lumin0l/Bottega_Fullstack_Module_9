# Infinte Scroll Intro

The infinite scroll can be handled by creating a function with the React integrated listener **window.onscroll**. That will read whenever a scroll is done.

Example:
```
activateInfiniteScroll() {
	window.onscroll = () => {
		console.log('onscroll');
	}
}
```

What we are going there is create the function and then start the **onscroll** listener in the window, then we assign the console.log to it, so it will register it whenever somebody scrolls.