# Original review

This project was an unfinished attempt at the second Shapes Drawables exercise. The intent was recognizable, but the resource structure could not produce a valid Android screen:

- a `<selector>` incorrectly contained `<color name=...>` instead of selector `<item>` entries;
- another selector nested a shape and a named color in an invalid way;
- the Activity layout used an `ImageView` as the root while trying to place a `Button` and `CheckBox` inside it, although `ImageView` is not a `ViewGroup`;
- required layout attributes were missing on the child controls.

The modern version completes the historical exercise rather than redesigning it: the two requested `ImageView` controls remain, each rendering a reusable green XML shape drawable. A proper layout container now owns the button, checkbox, and image lines.
