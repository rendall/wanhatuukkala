# Wanhan-Tuukkalan tallin kotisivu

<https://wanhatuukkala.fi>

Tämä repositorio sisältää Wanhan-Tuukkalan Tallin verkkosivuston lähdekoodin. Jos huomaat sivustolla ongelmia, ole hyvä ja ilmoita niistä Heidille, niin voimme korjata ne.

Voit myös [luoda uuden tukipyynnön täällä](https://github.com/rendall/wanhatuukkala/issues/new). Huomaathan, että tukipyynnön luominen vaatii uuden tilin luomisen tälle sivustolle. [Rekisteröidy tästä](https://github.com/signup?return_to=https%3A%2F%2Fgithub.com%2Frendall%2Fwanhatuukkala%2Fissues%2Fnew&source=login).

## Development

Have `npm` installed, probably via `Node.js`. Run a local instance by:

```bash
npx http-server -a localhost ./public
```

Then open a browser at <http://localhost:8080>

If it says _Hello world! Tip: Check your console_ then you need to hard refresh the browser: `CTRL + SHIFT + r`

Push your changes to `master` and those changes will be reflected on the production website.

### Development philosophy

The horse farm does not need a complicated or heavy website. Resist the urge to add React or other heavy frameworks or services. Just show basic information and links.
