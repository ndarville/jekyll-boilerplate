How-To for Writers
==================
You join the blog as a writer by doing the following:

Create a User
-------------
1. Create at GitHub user. [#](https://github.com)
2. Upload a display image for your user. Use one that will look good in a `125x125` circle (if the blog uses [the default settings](https://github.com/ndarville/jekyll-boilerplate/blob/293c6e90ae10305061583b452f7c090e46a83596/static/css/_config.scss#L15-L16).) [#](https://github.com/settings/profile)

Create or get invited as a contributor to a repository.

Enter Your Details
------------------
1. Either you, or someone on your behalf, will have to go to `people.yml` in the `_data` folder. ([Example](https://github.com/ndarville/jekyll-boilerplate/blob/master/_data/people.yml).)
2. Create an entry for yourself next to the other contributors. Place your name entry alphabetically.

    ```yml
    ndarville:  # GitHub username
      name: Niclas Darville
      twitter: pessimism
      website: ndarville.com
      mail: ""

    xampleuser:
      name: John Appleseed
      twitter: ""
      website: example.com
      mail: ""
    ```

    The only mandatory field to enter is your GitHub username, as that will be used to look you up in the data file, and to retrieve your GitHub avatar. To leave a field blank, use an empty (`""`) value.

You are now set up as a user.

Write!
------
You can use GitHub's own interface for writing post, but that is generally not recommended.

If you know your way around an editor and terminal, you won't need any help, but if you don't, do this:

Go to <https://prose.io>, log in with your GitHub credentials, and write your posts - or edit your credentials in `people.yml` - in a much friendlier writing environment.
