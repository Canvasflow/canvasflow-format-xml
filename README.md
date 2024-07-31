
# Canvasflow Format

Canvasflow Format serves as a way to create content that can easily be interpret by Canvasflow, it uses `.xml` to describe what the structure of the `articles` and `issue` looks like and it packages them using a `.zip` file

Currently Canvasflow supports the following formats

## Formats

| Format                  | Extension  | Description                                                                                                         |
| :---------------------- | :--------- | :------------------------------------------------------------------------------------------------------------------ |
| [Article](./Article.md) | `.article` | Enables user to express a single article in canvasflow                                                              |
| [Issue](./Issue.md)     | `.issue`   | Enables user to express a single issue in canvasflow, which contains `articles` and adds support for replica pages. |

## Example

### Article Format

| File                                                        | Description                                                                                             |
| :---------------------------------------------------------- | :------------------------------------------------------------------------------------------------------ |
| [Simple Article](./examples/articles/simple-article)        | This is an example of a simple article that have `text`, `image`, `divider` and `spacers`               |
| [Simple Advert](./examples/articles/simple-advert)          | This is an example of a simple article that serve an advert                                             |
| [Article Columns](./examples/articles/article-with-columns) | This is an example of a more complex article that support `gallery`, `columns`, `container` and `video` |
