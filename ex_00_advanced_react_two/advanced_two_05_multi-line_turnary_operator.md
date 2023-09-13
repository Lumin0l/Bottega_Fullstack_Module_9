# Multiple line turnary operators

Just an example, because pretty crazy:

```
{this.state.thumb_image && this.state.editMode ? (
    <img src={this.state.thumb_image} />
  ) : (
    <DropzoneComponent
      ref={this.thumbRef}
      config={this.componentConfig()}
      djsConfig={this.djsConfig()}
      eventHandlers={this.handleThumbDrop()}
  )}
```
