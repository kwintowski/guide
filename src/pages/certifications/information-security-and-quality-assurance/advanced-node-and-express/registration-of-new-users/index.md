---
title: Registration of New Users
---
## Registration of New Users

Be sure to edit views/pug/profile.pug, line 11:
<br>
```pug
h1.border.center FCC Advanced Node and Express
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;into
<br>

```pug
h1.border.center Profile Home
```
---
title: Check your mongodb Version
---

The code (and mongo version in Glitch) is for mongodb < v3.

Be sure to update to the latest version via npm in package.json

And update the connection code to:

```
MongoClient.connect('mongodb://localhost', function (err, client) {
  if (err) throw err;

  var db = client.db('mytestingdb');

  db.collection('customers').findOne({}, function (findErr, result) {
    if (findErr) throw findErr;
    console.log(result.name);
    client.close();
  });
});
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;or else the tests wouldn't pass
<br>
<br>

This is a stub. <a href='https://github.com/freecodecamp/guides/tree/master/src/pages/certifications/information-security-and-quality-assurance/advanced-node-and-express/registration-of-new-users/index.md' target='_blank' rel='nofollow'>Help our community expand it</a>.

<a href='https://github.com/freecodecamp/guides/blob/master/README.md' target='_blank' rel='nofollow'>This quick style guide will help ensure your pull request gets accepted</a>.

<!-- The article goes here, in GitHub-flavored Markdown. Feel free to add YouTube videos, images, and CodePen/JSBin embeds  -->
