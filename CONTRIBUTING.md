# Contributing

Thanks for considering contributing to Chasers!

If you’re new to all this GitHub, Open Source, JavaScript, Node.js, testing, wow all this stuff seems really difficult I just want to make my sites better stuff, I get it. I’m still there, too.

Feel free to [send me an email](hello@kennethormandy.com) or [open an issue here](http://github.com/kennethormandy/chasers/issues) and I’ll do my best to share some resources that have helped me out. No promises—I’m still learning, too—but I can say it would be great to have you stay around, or be involved in any capacity, if you’re interested.

## Opening issues

If you find a bug, please feel free to [open an issue](https://github.com/kennethormandy/chasers/issues).

If you taking the time to mention a problem, even a seemingly minor one, it is greatly appreciated, and a totally valid contribution to this project. Thank you!

## Fixing bugs

We love pull requests. Here’s a quick guide:

1. [Fork this repository](https://github.com/kennethormandy/chasers/fork) and then clone it locally:

  ```bash
  git clone https://github.com/kennethormandy/chasers
  ```

2. Create a topic branch for your changes:

  ```bash
  git checkout -b fix-for-that-thing
  ```
3. Commit a failing layout test for the bug in `text/index.html`:

  ```bash
  git commit -am "Adds a failing test to demonstrate that thing"
  ```

4. If you’ve figured out the problem, commit a fix in the SCSS that makes your test pass:

  ```bash
  git commit -am "Adds a fix for that thing!"
  ```

5. Review the tests. You’ll need to have [Harp](http://harpjs.com), which you can [get started with here](http://harpjs.com/docs/quick-start).

  ```bash
  npm install -g harp
  npm test
  # Test is now available in the browser at http://localhost:9023/test
  ```

6. If everything looks good, push to your fork:

  ```bash
  git push origin fix-for-that-thing
  ```

7. [Submit a pull request.](https://help.github.com/articles/creating-a-pull-request)

8. Enjoy being the wonderful person you are

  After you’ve opened your pull request, [you should email me](mailto:hello@kennethormandy.com) your mailing address so I can mail you a personal thank you note. Seriously!

## Adding new features

Thinking of adding a new feature? Cool! [Open an issue](https://github.com/kennethormandy/chasers/issues) and let’s design it together.
