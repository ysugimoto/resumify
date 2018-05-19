# resumify

Capture screenshot and make PDF on your HTML presentation.

## Requirements

- `node.js`: main program  ( recommend 4.2.x, at least 4.x )
- `electron`: Capturing screenshot ( this package has dependency installtion `electron-prebuilt` )
- `ImageMagick`: PDF creation ( install and set PATH )

## Installation

Use `npm` simply, we recommend global install:

```
$ npm install -g resumify
```

## Usage

### 1. Local Presentation

Change to directory to slide-HTML file existing, run the command:

```
$ cd /path/to/presentation/
$ resumify
```

`resumify` will auto detecting HTML file, and processing.

### 2. Remote Presentation

If slide has remote server (e.g. AWS S3), supply URL with `-u` or `--url` option:

```
$ resumify -u http://example.com/path/to/presentation/index.html
```

Note that URL must be fully format ( including .html ).

## Options

`resumify` has some options to manage processing:

| option        | description                                         | default   |
|---------------|-----------------------------------------------------|-----------|
| -t, --type    | Slide control type. Can accepts `url` or `scroll`.  | url       |
| -s, --size    | Capture screen size with `[width]x[height]` format. | 1280x800  |
| -s, --size    | Capture screen size with `[width]x[height]` format. | 1280x800  |
| --skip        | Skip capturing slide number like `2,3,4,...` format | -         |
| -e, --end     | End of slide number                                 | 1         |
| -u, --url     | Remote slide URL                                    | -         |
| -h, --help    | Show help                                           | -         |
| -v, --version | Show program version                                | -         |
| -o, --output  | Determine output PDF filename                       | slide.pdf |

### Slide Type

The new option of `-t, --type`, which is determine how slide is controlled.
If type is `url`, slide will move by URL hash like `#1`, `#2`, ...
Other type is `scroll`, slide will move by page scrolling.

## Author

Yoshiaki Sugimoto

## License

MIT
