# Wanhan-Tuukkalan tallin kotisivu

<https://wanhantuukkalantalli.fi>

Tämä repositorio sisältää Wanhan-Tuukkalan Tallin verkkosivuston lähdekoodin. Jos huomaat sivustolla ongelmia, ole hyvä ja ilmoita niistä Heidille, niin voimme korjata ne.

Voit myös [luoda uuden tukipyynnön täällä](https://github.com/rendall/wanhatuukkala/issues/new). Huomaathan, että tukipyynnön luominen vaatii uuden tilin luomisen tälle sivustolle. [Rekisteröidy tästä](https://github.com/signup?return_to=https%3A%2F%2Fgithub.com%2Frendall%2Fwanhatuukkala%2Fissues%2Fnew&source=login).

## Development

If you would like to contribute to the website, great! Happy to have you. Follow the instructions below. If anything is unclear, please get in touch with me or [file an issue](https://github.com/rendall/wanhatuukkala/issues/new)

### Github

- First step: [sign up for an account here on Github](https://github.com/signup)
- Second step: [request access to the Wanhan-Tuukkalan tallin source code repository](https://github.com/rendall/wanhatuukkala/issues/new)

### Software

Third, there is software that you should install on your system. Download and install each of these:

1. [Visual Studio Code (VS Code)](https://code.visualstudio.com/) - This is a kind of text editor for the website's source code.
1. [git](https://git-scm.com/downloads) - This is a _version control system_, how we transfer changes we make on our local machines to Github, so they can show up on Heidi's website.
   - You will also want to integrate _git_ with _VS Code_. Follow these instructions: <https://code.visualstudio.com/docs/sourcecontrol/intro-to-git>
1. [Node.js](https://nodejs.org/) - Node is a used here to run a local webserver.

### Setup

Great. You have everything you need to make changes to the website. To do that, follow these steps:

1. Find or create a "workspace" folder on your computer. It can be in your documents folder or somewhere else convenient. Name it "websites" or "projects" or "workspace" or whatever else works for you.
2. Open _VS Code_. You should see a "Welcome" tab, and with a "Start" headline, and somewhere under that a _Clone Git Repository_ link. Click that.
3. A text field will pop up. Enter this `https://github.com/rendall/wanhatuukkala`. This should download all of the source code into a `wanhatuukkala` folder _inside_ your workspace folder from step 1.
4. Open the project in VS Code.
   - On the left you should see the _Explorer_ panel which has all of the files and folders of the project.
     - If you do not see this panel, from the menu click *View* > *Explorer*.

   - The website folders are in the `public` folder.
     - Click the word `> public` to _expand_ the folder and see the files inside.
   - Inside that folder is an `index.html`.
     - Click `index.html` to open the file in the _Editor_ window.
     - Or from the menu click *Go* > *Go to File...*, then type _index.html_ and press _Enter_ .

   - `index.html` is the source code for the home page of the website.
   - When you have a chance, [read the Get Started section](https://code.visualstudio.com/docs/getstarted/userinterface) of the manual.
5. With the project open in VS Code, [open a terminal](https://code.visualstudio.com/docs/terminal/basics) (From the menu, use the *Terminal* > *New Terminal* or *View* > *Terminal* menu commands) 
  - Type `npm -v` into the terminal. 
  - If you get a version number (looks something like `v10.7`, great! _Node.js_ is installed correctly.
  - If instead you get a `Command 'npm' not found` error, then your installation of _Node.js_ is incorrect and you need to install it again, carefully. Ask me for help!

6. Into the terminal, type `npx http-server -a localhost ./public`. This runs a little webserver on your computer.
7. Open <http://localhost> in your browser and you should see Heidi's website!

Congratulations, you have everything you need to code!

### Coding

1. Open `index.html` in VS Code editor. This is Heidi's site.
   - It is written in HTML (Hyper Text Markup Language). When you have a chance, [read more about HTML](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics).
2. Make a small change to the `index.html` page. For instance, replace the word `hevosten` with `omenan`. Save your change in VS Code and then refresh the browser. You should see your change on your local website.
   - Don't worry. These changes aren't permanent and they do not affect the _production_ website. You only affect your local version of the site. Go ahead and undo that change.

Use your new-found ability to change the website as a way to explore and learn about [HTML](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics) and [CSS](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics). Add content like text and pictures. Change colors. Make mistakes. If you have a goal in mind, like adding a gallery or a new announcement, try to implement your goal. Ask for help! Have fun!

### Pushing live

#### Credentials

In order to push your changes to the internet, you need to let GitHub know who you are. Download and install the [Github Command-line-interface (CLI)](https://cli.github.com/).

1. Go here <https://cli.github.com>
1. If your operating system is not listed, then go here <https://github.com/cli/cli?tab=readme-ov-file#github-cli> and choose how to install it.
1. When it's installed, open a terminal and type `gh auth login`
   1. Make sure `Github.com` is highlighted and press _Enter_
   1. `HTTPS` then _Enter_
   1. _Authenticate Git with your GitHub credentials?_  Type `Y` and press _Enter_
   1. `Login with a web browser` then _Enter_
   1. Copy the code that looks like *6CE4-4C6D* and _Enter_
   1. Paste the code into the browser.
   1. Follow the directions in the browser.

Great! Now you are credentialed with GitHub.

#### Committing changes

When your changes to the website are ready ready and your goal is met, then you can push your changes live so they show up on <https://wanhantuukkalantalli.fi/>. Here is how:

1. First, make sure you really want these changes live. Don't accidentally turn the horse farm into an apple orchard, for instance!
2. Open the _Source Control panel_ in VS Code
   - (Click **View** on the menu bar and then **Source Control**).
3. In the _Message_ field, the placeholder text should say (something like) _Message (Ctrl+Enter to commit on "master")_. It has to mention _"master"_.
4. In that _Message_ field, add a _short_ (under 50 character) description of your changes.
5. Click _Commit_.
6. You might have to click _Push_ or _Sync changes_.

#### Messed up website

If somehow the production website is messed up, do not panic! Just fix your changes and follow steps 1 through 3 above.

However, if the website is just so messed up that you don't know how to go forward, then go back. This is how:

1. Type in the terminal `git checkout master && git pull`
   - If git tells you that you have unsaved changes type `git stash` and repeat step 1.
   - `git stash` stores your changes in the `stash` which is a kind of temporary list of changes you want to get back to.
   - Later, recover your changes with `git stash pop`
2. Get a local version of the website up and running. Make sure it's the messed-up version.
3. Type in the terminal `git reset --hard HEAD~1`
4. Refresh the browser. If the website is back to normal, great. If not, repeat step 3 and 4 until the website looks good.
5. Type in the terminal `git push --force`
   - This reverts all of the messed up changes back to what it was before.

#### Pushing live with a Pull Request (the recommended way)

Rather than pushing right to production, you could have other people look at your changes first and either approve the changes or they could point out errors or ask you to do something different. It's a way to share responsibility and make sure no errors creep in. You do this by creating a [_Pull Request_](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) (often shortened to _PR_) which is a kind of temporary forum to discuss your proposed changes. From there you can also see how your changes would look on the production site.

Make sure your latest changes are saved then follow these steps:

1. Add your changes to a _git branch_. There are two ways. Pick whichever is easiest for you:
   1. _either_: Type `git checkout -b new-branch` into the terminal.
      - `new-branch` can be anything descriptive instead of `new-branch`, like `update-price-list`. It should only be lower-case letters and - dashes.
      - Type `git commit -m "Describe your changes"`
        - The "Describe your changes" part should be a description of your changes inside of quotes `""` and should be less than 50 characters.
   2. _or_: Open the _Source Control panel_.
      - Mouse-over just above the _Message_ field.
      - You should see three dots appear `...` to the right of other icons with the tooltip _More actions_. Click that.
        - Be careful, because there is _another_ three dots at the top, and that one is not the correct one.
      - Select `Checkout to...`
      - Enter a branch name. See Step 1 for naming ideas.
      - Make sure that `+ Create new branch...` is highlighted and press _Enter_.
      - Fill in the Message field as normal and click _Publish branch_
2. Create a _Pull Request_. You are requesting to _pull_ your changes in to the `master` branch. There at least two ways to do this. Pick the easiest for you.

   1. _either_: In the _Source Control panel_ mouse over just above the _Message_ field.
      - Find the icon for _Create pull request_ and click it.
      - Fill in the _Title_ and _Descripion_ fields.
      - Click `Create`
   2. _or_: Click [here](https://github.com/rendall/wanhatuukkala/compare) <https://github.com/rendall/wanhatuukkala/compare>
      - In the `compare:` drop-down, select your new branch name.
      - Click _Create pull request_
      - Fill in the title and description
      - Click _Create pull request_

3. Get other coders to review your changes. The Pull Request page will [look like this](https://github.com/rendall/wanhatuukkala/pull/2).

   - Let other coders know about the pull request. They can review your code, download it, make sure it works, make comments, and then either _approve_ the Pull Request or _request changes_.
   - The Netlify bot will have a "Deploy Preview" link and you can see how your changes will look when pushed live.
   - There is a big green _Merge pull request_ button. When you push it, your changes will go live.

### Further Reading

- git: <https://docs.github.com/en/get-started/getting-started-with-git/set-up-git>
- git branches: <https://www.atlassian.com/git/tutorials/using-branches>
- pull requests: <https://docs.github.com/en/pull-requests>
- HTML basics: <https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics>
  - CSS basics: <https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics>
  - JavaScript basics: <https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics>
- Netlify, our hosting platform: <https://docs.netlify.com/get-started/>

### Development philosophy

The horse farm does not need a complicated or heavy website. Resist the urge to add React or other heavy frameworks or services. Just show basic information and links.

Everything appearing on the website must be in Finnish, while all source code and documentation must be in English.
