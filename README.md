
# Canvasflow Format

The Canvasflow Format provides a way to create content that can be easily interpreted by Canvasflow. It uses `.xml` to describe the structure of the `articles` and `issue`, then packages them in a `.zip` file

Currently Canvasflow supports the following formats:

## Formats

| Format                  | Extension  | Description                                                                                                         |
| :---------------------- | :--------- | :------------------------------------------------------------------------------------------------------------------ |
| [Article](./Article.md) | `.article` | Enables a user to express a single article in canvasflow                                                              |
| [Issue](./Issue.md)     | `.issue`   | Enables a user to express a single issue in canvasflow, which contains `articles` and adds support for replica pages. |

## Example

### Article Format

| File                                                        | Description                                                                                             |
| :---------------------------------------------------------- | :------------------------------------------------------------------------------------------------------ |
| [Simple Article](./examples/articles/simple-article)        | This is an example of a simple article that uses `text`, `image`, `divider` and `spacers`               |
| [Simple Advert](./examples/articles/simple-advert)          | This is an example of a simple article that serves an advert                                             |
| [Article Columns](./examples/articles/article-with-columns) | This is an example of a more complex article that uses `gallery`, `columns`, `container` and `video` |
