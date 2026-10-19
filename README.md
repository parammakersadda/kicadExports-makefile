
# KiCad Export Automation

A simple GNU Makefile to automate exporting manufacturing files, PDFs, images, and 3D models from KiCad projects.

## Requirements

- [KiCad](https://www.kicad.org/) with `kicad-cli` available in `PATH`
- GNU Make
- `zip` command-line utility

## Usage

1. Place the `Makefile` in the root directory of your KiCad project.
2. Open a terminal in that directory.
3. Run:

   ```bash
   make
   ```

The project name is automatically determined from the directory containing the Makefile. Output directories are created automatically.

## Exports

| Directory | Generated files |
|---|---|
| `exports/` | Gerber files and ZIP archive |
| `PDFs/` | PCB and schematic PDFs |
| `images/` | PCB preview PNG and schematic/PCB SVGs |
| `3dModels/` | GLB and STL 3D models |

GNU Make rebuilds outputs when their source files change and their dependencies indicate that rebuilding is necessary.

## License

Released under the [MIT-0 License](https://spdx.org/licenses/MIT-0.html).

