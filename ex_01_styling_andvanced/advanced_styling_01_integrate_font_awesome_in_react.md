# Font Awesome in React

Unlike in just HTML , you need to import several modules into react:

`npm i @fortawesome/fontawesome-svg-core @fortawesome/free-solid-svg-icons @fortawesome/react-fontawesome`

And then import them where the final render is going to happen and use it from there (maybe import it from there into other components too).

```
import { library } from "@fortawesome/fontawesome-svg-core";
import { FortAwesomeIcon } from "@fortawesome/react-fontawesome";
import { faTrash, faSignOutAlt } from "@fortawesome/free-solid-svg-icons";
```

As a tip, it is necessary to adapt to and follow the steps set by each different outside library.

## Styling Font Awesome icons

Just like any oother css element. Apply a class and apply the styles.

## Naming Font Awesome icons

Sometimes the icons have special names or names with spaces. The way to make them work is to use "camel case" and "-" instead of space.
