# pantomime-site

This repository contains the source code to Pantomime's website.

## Setup

You'll need the following tools

* [fsw](https://github.com/longshorej/fsw)
* [csi](https://github.com/longshorej/csi/)

To build the site each time you change a file:

```bash
fsw csi src target/dist --ext .html
```

You can find the rendered files in `target/dist`.

To start a webserver at [http://localhost:8000](http://localhost:8000):

```bash
python -m http.server --directory target/dist --bind localhost 8000
```

## Publishing

To publish this website, push a tag in the format of vYYYY.MM.DD.R where
R is the revision number for the particular day.

### Prism

This project uses [Prism](https://prismjs.com) for syntax highlighting of
  example code. A custom build is created using the website's tool:

* Theme: Funky
* Languages: ONLY Rust, TOML. Make sure to remove default languages.

## License

This repository is provided under the [MIT License](LICENSE).
