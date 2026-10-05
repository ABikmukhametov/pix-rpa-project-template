# PIX RPA Project Template

A transaction-oriented starter project for PIX Studio. It integrates the reusable framework, structured logging, retry and error handling, reporting, maintenance windows, and optional multi-clone execution.

## Requirements

- PIX Studio 3.0 or newer; the current project metadata targets PIX 3.2.
- The `pix-rpa-framework` repository.
- Dependencies restored from `src/nuget.config` and `src/packages.config`.

## Quick start

1. Clone or copy the template for a new robot.
2. Open `src/rpa_project_template.pixproj` in PIX Studio and restore packages.
3. In the `main.pix` Variables panel, replace `PIX_RPA_FRAMEWORK_ROOT` with a valid C# string expression containing the framework repository path.
4. Replace `PIX_RPA_PROJECT_ROOT` with a valid C# string expression containing this project root.
5. Review `data/configs/config.json`; replace placeholder recipients and credential names before enabling notifications.
6. Implement business logic under `src/process`.

The optional `clones_root` behavior remains available and overrides the normal project root for a configured Windows user clone.

The two `PIX_RPA_*` values are deliberate compile-time placeholders, not operating-system environment variables. A fresh copy is intentionally non-compilable until both paths are configured for the target machine.

Detailed Russian-language documentation is available in [docs/readme.md](docs/readme.md).

## Author and license

Aidar Bikmukhametov — ARBikmuhametov@yandex.ru

Released under the [MIT License](LICENSE).
