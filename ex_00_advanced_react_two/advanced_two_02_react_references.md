# React References

They allow contact with the **DOM** directly instead of with the virtual DOM.

It shouldn't be abused because it would go against the basic principle of react and using the virtual DOM with all the tools and safeguards that react provides, and it can create a lot of bugs.

There are some good uses:

- Managing focus, text selection or media playback.
- Triggering imperative animations
- Interacting with third-party DOM libraries.

To use refs we need to create **reference objects** and then used in the JSX to reference elements in the real DOM, like this:

```
this.thumbRef = React.createRef();
this.bannerRef = React.createRef();
this.logoRef = React.createRef();

<DropzoneComponent
              ref={this.thumbRef}
              config={this.componentConfig()}
              djsConfig={this.djsConfig()}
              eventHandlers={this.handleThumbDrop()}
            />
```
