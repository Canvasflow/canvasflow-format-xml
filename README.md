
# Canvasflow Format

Canvasflow Format serves as a way to create content that can easily be interpret by Canvasflow, it uses `.xml` to describe what the structure of the `articles` and `issue` looks like and it packages them using a `.zip` file

Currently Canvasflow supports the following formats

## Formats

| Format                         | Extension  | Description                                                                                                         |
| :----------------------------- | :--------- | :------------------------------------------------------------------------------------------------------------------ |
| [Article Format](./Article.md) | `.article` | Enables user to express a single article in canvasflow                                                              |
| [Issue Format](./Issue.md)     | `.issue`   | Enables user to express a single issue in canvasflow, which contains `articles` and adds support for replica pages. |