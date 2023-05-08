# e-commerce-back-end

# Employee-Tracker

## Table Of Contents

*[Technology Used](#technology-used)

*[Description](#description)

*[Code Snippet](#code-snippet)

*[ScreenShot](#screenshots)

*[Video](#video)

*[Credits](#credits)

*[Author](#author)

## Technology used

| Technology Used         | Resource URL  |
| -------------           |:-------------:|
| Node.js                 | [https://nodejs.org/en](https://nodejs.org/en) | 
| npm                     | [https://www.npmjs.com/](https://www.npmjs.com/)      |
| Inquirer                | [https://www.npmjs.com/package/inquirer#prompt](https://www.npmjs.com/package/inquirer#prompt)
| Git                     | [https://git-scm.com/](https://git-scm.com/)     | 
| JavaScript              | [https://developer.mozilla.org/en-US/docs/Web/JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) |
| MYSQL                   | [https://www.mysql.com/](https://www.mysql.com/) |
| MYSQL2                  | [https://www.npmjs.com/package/mysql2](https://www.npmjs.com/package/mysql2) |
| Express                 | [https://expressjs.com/en/5x/api.html](https://expressjs.com/en/5x/api.html) |
| Dotenv                  | [https://www.npmjs.com/package/dotenv](https://www.npmjs.com/package/dotenv) |


## Description
This Program stores information in a database and specifically for retail stores, we are able to access the data via insomnia. this way we can see the list of items these stores have to offer.

## Code Snippet
This is a view of the end of my restful CRUD method for my categories, it deletes the specific id location.

```JavaScript
router.delete('/:id', async(req, res) => {
  // delete a category by its `id` value
  try{
    const categoryAll = await Category.destroy({
      where: {id: req.params.id,},
    });
    res.status(200).json(categoryAll);
  } catch (err){
    res.status(500).json(err);
  }
});
```
## ScreenShots
![Products insomnia](./Assets/Module%2013%20api%20products.png) ![Categories insomnia](./Assets/Module%2013%20api%20categories.png)
![Tags insomnia](./Assets/Module%2013%20api%20tags.png)

## Video
[Walk through video](./Assets/Module%2013%20recording.mp4)

## Credits
[CRUD Help](https://www.codecademy.com/article/what-is-crud)

[mySQL syntax](https://www.mysqltutorial.org/mysql-cheat-sheet.aspx)

## Author
```MD
### Emanuel Molina

[GitHub](https://github.com/AcquahLopid)
[LinkedIn](https://www.linkedin.com/in/emanuel-molina-65b84426b/)
[GitLab](https://ucb.bootcampcontent.com/emanuelmolina2k-BAsayK)

```