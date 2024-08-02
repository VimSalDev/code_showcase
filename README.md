# Code Showcase

![Code Showcase](https://img.shields.io/badge/Hugo-v0.80.0-blue)
![GitHub license](https://img.shields.io/github/license/VimSalDev/code_showcase)
![GitHub last commit](https://img.shields.io/github/last-commit/VimSalDev/code_showcase)
![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/VimSalDev/code_showcase/main.yml)

## Description

`Code Showcase` is a project deployed on GitHub Pages using the Hugo framework and the [hugo-JuiceBar](https://github.com/hotjuicew/hugo-JuiceBar.git) theme, adapted to display mini projects or small projects in JavaScript, CSS, and HTML visually, like a personal blog.

## Features

- **Hugo Development**: Fast and flexible static site generator.
- **JuiceBar Theme**: Adapted to the project's needs.
- **Automated Deployment**: Using GitHub Actions to automate the build and deployment process.
- **Visual Code**: Display small projects visually and attractively.

## Project Structure

- `main`: Main branch for production.
- `develop`: Development branch.
- `gh-pages`: Branch for deployment on GitHub Pages.

## Setup and Usage

Visit the deployed project at [GitHub Pages](https://VimSalDev.github.io/code_showcase).


### Prerequisites

- Hugo v0.80.0 or higher.
- Node.js and npm (optional, for installing additional dependencies).

### Deployment

Deployment is automated using GitHub Actions. Every time a merge from `develop` to `main` is made, a workflow runs to build the site and deploy the content of the `public` folder to the `gh-pages` branch.

## Customization

You can adapt and customize the `hugo-JuiceBar` theme by editing the files in the `themes/hugo-JuiceBar` folder.

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

## Contributions

Contributions are welcome. Please open an issue or submit a pull request to improve the project.

## Contact

- GitHub: [VimSalDev](https://github.com/VimSalDev)

---

**Note**: Your feedback and contributions are essential to the growth and success of this project.
