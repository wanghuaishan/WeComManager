# AI Coding Agent Instructions for Vue User Registration Project

## Overview
This project is a Vue.js application for user registration. It includes a registration form, a responsive design, and is built using Vite as the build tool. The project is structured to be simple and easy to extend.

## Key Files and Directories
- **`src/main.js`**: Entry point for the Vue application. Initializes the app and mounts it to the DOM.
- **`src/App.vue`**: Root component of the application.
- **`src/components/UserRegistrationForm.vue`**: Contains the user registration form logic and validation.
- **`src/views/RegistrationPage.vue`**: Page component that includes the registration form.
- **`public/index.html`**: HTML template used by Vite to serve the application.
- **`vite.config.js`**: Configuration file for Vite, specifying plugins and build options.

## Developer Workflows
### Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd vue-user-registration
   ```
3. Install dependencies:
   ```bash
   npm install
   ```

### Development
To start the development server:
```bash
npm run dev
```
The application will be available at `http://localhost:3000`.

### Build
To create a production build:
```bash
npm run build
```
The build output will be in the `dist` directory.

### Testing
Currently, no automated tests are set up. Testing is manual by running the application and verifying functionality.

## Project-Specific Conventions
- **Component Structure**: Components are organized under `src/components` for reusable UI elements and `src/views` for page-level components.
- **Styling**: Scoped styles are used within `.vue` files to encapsulate CSS.
- **Validation**: Basic form validation is implemented directly in the `UserRegistrationForm.vue` component.

## External Dependencies
- **Vue.js**: Framework for building the user interface.
- **Vite**: Build tool for development and production builds.

## Common Issues
- **Build Errors**: Ensure `index.html` is in the root directory for production builds. If moved, update the `vite.config.js` file accordingly.
- **Dependency Issues**: Run `npm install` to ensure all dependencies are installed.

## Contribution Guidelines
- Follow the existing project structure and conventions.
- Open an issue or submit a pull request for any changes.

## Examples
### Adding a New Component
1. Create a new `.vue` file in `src/components`.
2. Import and use the component in the relevant parent component.

### Updating Styles
Modify the scoped `<style>` section within the relevant `.vue` file to ensure styles are encapsulated.

---
For further questions or clarifications, refer to the [README.md](../README.md) file or open an issue in the repository.

### 项目描述
本项目是一个前端项目，是一个管理系统，用于管理企业微信群的创建、分类、查询、统计等。

### 开发语言限制
使用vue 3.5.26版本开发

### 网页样式限定
网页内容默认为中文
文字和输入表格等页面要素要合理对齐