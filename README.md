# Latex Document Quick Writer

A lightweight WPF desktop app to quickly create, edit and export professional LaTeX documents. Built with .NET 10 and a Fluent-style UI. The app provides ready-to-use templates (academic paper, presentation, resume, technical report) and a form-driven editor with reusable input controls.

## Key Features
- New blank LaTeX project
- Open / import local projects
- Select from built-in template library
- Form-driven editor with modular input controls
- Export / preview workflows (extendable)

## Prerequisites
- .NET 10 SDK
- Visual Studio 2026 (recommended) or `dotnet` CLI
- Restore NuGet packages before building

The project uses a Fluent UI resource dictionary in `App.xaml`. If styles fail to load, install a Fluent-style WPF package (common options):
- `FluentWPF` — `dotnet add package FluentWPF`
- or the package referenced by the project: `PresentationFramework.Fluent` — `dotnet add package PresentationFramework.Fluent`

## Quick start

1. Clone the repository:
   - `git clone <repo-url>`
2. Open the solution in Visual Studio 2026, or use CLI:
   - `cd <solution-folder>`
   - `dotnet restore`
   - `dotnet build`
3. Run:
   - From Visual Studio: Press F5
   - Or CLI: `dotnet run --project <YourProject.csproj>`

## Project layout (important files)
- `App.xaml` — application entry; merges Fluent UI resource dictionary
- `MainWindow.xaml` — main UI (template browser, quick actions)
- `Windows/Editor.xaml` — editor window
- `Controls/` — custom input controls (`AttachmentInput.xaml`, `ComboInput.xaml`, `DateTextInput.xaml`, `FormulaInput.xaml`, `OnlyTextInput.xaml`, `TableInput.xaml`, `thebibliographyInput.xaml`, etc.)
- `MainWindow.xaml.cs` — main window code-behind (event handlers)

## Troubleshooting
- Missing resource dictionary / styles: ensure the Fluent package referenced by `App.xaml` is installed and NuGet packages are restored.
- Fonts or colors not matching: system font `Segoe UI` is used in examples; replace in resources if unavailable.
- Want Acrylic or advanced Fluent effects: check the installed Fluent package docs — some effects require using a special window base class or additional settings.

## Contributing
Contributions welcome. Please:
- Fork and create a feature branch
- Keep commits small and focused
- Include a short description and test steps in PR

## License
Default: MIT. Add or update `LICENSE` in the repo root if you use a different license.

If you want, I can:
- Convert `App.xaml` to reference a specific Fluent package URI,
- Add a simple README section that documents template formats and how to add new templates,
- Or generate sample LaTeX templates to include in `Templates/`.
