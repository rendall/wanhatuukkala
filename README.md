# Wanhan-Tuukkalan tallin kotisivu

<https://wanhatuukkala.fi>

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

1. Find or create a "workspace" folder on your computer. It can be in your documents folder or somewhere else convenient. Name it "websites" or "projects" or "workspace".
2. Open _VS Code_. You should see a "Welcome" tab, and with a "Start" headline, and somewhere under that a _Clone Git Repository_ link. Click that.
3. A text field will pop up. Enter this `https://github.com/rendall/wanhatuukkala`. This should download all of the source code into a `wanhatuukkala` folder _inside_ your workspace folder from step 1.

#### More directions soon!

### Development philosophy

The horse farm does not need a complicated or heavy website. Resist the urge to add React or other heavy frameworks or services. Just show basic information and links.

Everything appearing on the website must be in Finnish, while all source code and documentation must be in English.
