# npm init with custom values

`npm init` command is the simplest way to start a project, but filling answers to those questions are irritating. If we use `npm init -y` it will skip all the questions, but it will generate the `package.json` with npm default values. We have to update the author details, version and license later.


To make this easier we can set the author details, starting version and our favorite license in the `.npmrc` file so that next time we do `npm init -y` instead of npm default npm use `.npmrc` and fill the details.

copy paste the below code in the notepad and run in the terminal

```
npm config set init-author-name "Suresh Alagarsamy"
npm config set init-author-email "firstname.lastname@domain.com"
npm config set init-author-url "http://example.com/"
npm config set init-license "MIT"
```

Now the `.npmrc` will have these configuration (To find the .npmrc navigate to account folder C:\Users\SURESHA)

```
init-author-name=Suresh Alagarsamy
init-author-email=firstname.lastname@domain.com
init-author-url=http://example.com/
init-license=MIT
```

Please note that your package.json will update only updated. See the code sample

```json
{
  "name": "test",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "Suresh Alagarsamy <firstname.lastname@domain.com> (http://example.com/)",
  "license": "MIT"
}
```

Next time when we do npm `init -y` this will set the author name as `Your name`, email as `firstname.lastname@domain.com`, url as `http://example.com/` and license as `MIT`.


### globally installed packages

<b>Get list of globally installed packages</b>

```json
npm list -g --depth 0
```

![image](https://user-images.githubusercontent.com/6780840/46667977-ce5f3f80-cbe8-11e8-82e9-72b623fe571d.png)
