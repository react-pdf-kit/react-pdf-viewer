<div align="center">
  <a href="https://www.react-pdf-kit.dev/?utm_source=github&utm_medium=referral" target="_blank">
    <picture>
      <source srcset="./assets/img/react-pdf_cover.webp" width="100%">
      <img alt="React PDF Kit" src="./assets/img/react-pdf_cover.webp width="100%">
    </picture>
  </a>
</div>

<br/>
<div align="center">
  Works seamlessly on your React or Next.js websites. Fast, Customizable and Web Responsive PDF viewer. Save you weeks of development time.
</div>  
<br/>

<div align="center">
  
  [React PDF Kit Home][reactpdf] - [License](#page_facing_up-license) - [Documentation][reactpdf-docs]

[![NPM Version](https://img.shields.io/npm/v/%40react-pdf-kit%2Fviewer)][npm]
[![Twitter](https://img.shields.io/twitter/follow/ReactPDF?label=ReactPDF&style=social)][twitter]

</div>

# :star: Why React PDF Kit

- **Save Weeks of Development Time**: React PDF Kit simplifies PDF integration with ready-to-use tools, minimizing the need for custom development and saving you valuable time.
- **Tailored for React.js**: React PDF is native to React.js, ensuring smooth integration into your projects.
- **Customizability at Its Core**: Built with flexibility in mind, allowing you to match your application’s unique style and functionality.
- **High-Performance & Rapid Rendering**: Optimized for rendering large PDFs efficiently, React PDF delivers lightning-fast load times with features like virtual scrolling.
- **Accessibility**: Designed with inclusivity in mind, React PDF Kit supports ARIA attributes, catering to diverse user bases.
- **Modern Browser Compatibility**: The React PDF Viewer components seamlessly across modern browsers, eliminating compatibility headaches.
- **Active Development & Support**: With regular updates and a responsive support team, React PDF Kit evolves to meet developer needs.

<p align="center">
  <img src="https://github.com/user-attachments/assets/8803229a-2f59-48d1-aecc-628ae759862f" alt="React PDF Kit demo">
</p>

# 📜 Background

As developers ourselves, we faced many issues such as browser incompatibility and customizability while trying to render a PDF document or working with PDF libraries. Having faced issues using PDF libraries, we want the solution to be flexible for React.js developers and teams. More importantly, the technical document must be easy to use!

# :sparkles: Features

- 🎯 **Interactive & Immersive Viewing Experience** with features like rotation, zoom, and keyboard navigation.
- 📱 **Responsive Across All Devices** for a consistent experience on desktops, tablets and mobile devices.
- 🎨 **Customizable UI and Styling** to tailor the viewer’s appearance to match your website’s theme.
- 🧭 **Advanced Navigation Options** to browse documents easily with table of contents, hyperlinks, and a powerful search tool.
- ⚡ **High-Performance Rendering** to load large PDF documents quickly and handle complex elements like vector graphics with ease.
- 🔧 **Programmatic Control with Hooks and Props**, allowing you to interact with the viewer programmatically.
- 📂 **Document Management Tools**, including features like downloading and printing.
- 👁️ **Accessibility Support** to built-in support for ARIA attributes and tooltips, catering to diverse user bases.

For the full feature set, visit [React PDF Kit Features](https://www.react-pdf-kit.dev/features?utm_source=github&utm_medium=referral).

# :zap: Quick Start Guide

Here’s how to get started with React PDF Kit in your React.js project:

## 1. Check Prerequsities

Here are the basic system requirements to run the React PDF Viewer component:

- React version: >= 18.0
- React version: >= 19.0

If you are working with a React framework such as Next.js (App Router and Pages Router) or Gatsby, React PDF can run smoothly as long as you are using React 18 and above.

React PDF also works well with other React.js UI libraries such as MUI, Ant Design and Chakra UI.

Although React PDF Kit can run on most JavaScript module bundlers, it is more vigorously tested on Vite and Webpack.

_Remark: <br/>- If using TypeScript, it requires >= TypeScript 4.6._

### Browser support

Starting from [`@react-pdf-kit/viewer@^2.0.0`](https://www.npmjs.com/package/@react-pdf-kit/viewer), we officially support PDF.js 5 and default to PDF.js `5.4.530`.

As newer PDF.js versions rely on more modern browser APIs, minimum supported browser versions have changed. Please review the compatibility details below before choosing a PDF.js version.

#### Default (PDF.js 5.4.530)

React PDF Kit v2.0.0 defaults to PDF.js `5.4.530`.

| Chrome | Firefox | Edge | Safari | Safari iOS | Chrome Android |
| ------ | ------- | ---- | ------ | ---------- | -------------- |
| 126+   | 126+    | 126+ | 18.4+  | 18.4+      | 126+           |

<Aside>
It's currently not recommended to use a PDF.js worker version beyond `5.4.530` because it will support fewer browser versions.
</Aside>    

#### Using PDF.js 4.10.38

If you need broader browser compatibility, you can continue using PDF.js `4.10.38`, which supports:

| Chrome | Firefox | Edge | Safari | Safari iOS | Chrome Android |
| ------ | ------- | ---- | ------ | ---------- | -------------- |
| 119+   | 115+    | 115+ | 17.4+  | 17.4+      | 126+           |

To change the version of PDF.js used, refer to [Dependency Override](https://docs.react-pdf-kit.dev/usage-guide/overriding-dependency?utm_source=github&utm_medium=referral) guide.

## 2. Install the Package

There are a few ways you can install React PDF Kit, namely `bun`, `npm`, `pnpm` or `yarn`.

### Using bun:

```bash
bun add @react-pdf-kit/viewer
```

##### Caching of previous Worker version with `bun`

To clear cache, try running `bun pm cache rm` to remove cache in the global cache directory. If the error remains, try executing the following steps:

```shell
rm bun.lockb
rm -R node_modules
```

### Using npm:

```bash
npm install @react-pdf-kit/viewer
```

### Using yarn:

```bash
yarn add @react-pdf-kit/viewer
```

### Using pnpm:

```bash
pnpm add @react-pdf-kit/viewer
```

For more information on how to use different package managers, please visit our [installation guide](https://docs.react-pdf-kit.dev/introduction/getting-started/#installation?utm_source=github&utm_medium=referral).

## 3. Import and Use the Component

The following structure demonstrates how to build a React PDF viewer by importing and assembling components. This modular approach gives you the flexibility to customize the viewer as needed.

```tsx
<RPConfig>                {/* Configuration license and pdfjs-dist worker */}
  <RPTheme>               {/* Theme customization (optional) */}
    <RPProvider>          {/* Viewer context provider */}
      <RPLayout toolbar>  {/* Provide the default toolbar structure */}
        <RPPages />       {/* Render the actual PDF content */}
      </RPLayout>
    </RPProvider>
  </RPTheme>
</RPConfig>
```

_Remark: For more information on each component, please refer to [Component](https://docs.react-pdf-kit.dev/components/overview?utm_source=github&utm_medium=referral)._

### Basic Usage

The most basic usage of React PDF viewer needs four components, namely: `RPConfig`, `RPProvider`, `RPLayout`, and `RPPages`.

Here's how to implement a basic PDF viewer in a React application:

```jsx
import { RPProvider, RPLayout, RPPages, RPConfig } from '@react-pdf-kit/viewer'

const App = () => {
  return (
    <RPConfig>
      <RPProvider src="https://cdn.codewithmosh.com/image/upload/v1721763853/guides/web-roadmap.pdf">
        <RPLayout toolbar style={{ height: '660px' }}>
          <RPPages />
        </RPLayout>
      </RPProvider>
    </RPConfig>
  )
}
export default App
```

The PDF viewer will automatically adjust to fit its container's dimensions. You can control the size by setting the `style` prop on `RPLayout`. For more information on using React PDF, visit our [basic usage guide](https://docs.react-pdf-kit.dev/introduction/basic-usage?utm_source=github&utm_medium=referral)

You may also check out our [Starter Toolkit](#pushpin-starter-toolkit) for examples to get you started.

### 4. Customize with Hooks and Props

To enhance React PDF Kit further, we offer built-in hooks and props that let you fine-tune functionality, adjust appearance, and integrate custom behaviors into your application.

For detailed usage, refer to our [Documentation][reactpdf-docs].

# :pushpin: Starter Toolkit

Here are some sample projects to get started on React PDF quickly:

1. [React (webpack) - JavaScript](https://github.com/react-pdf-kit/starter-rp-react-js-webpack)
2. [React (webpack) - TypeScript](https://github.com/react-pdf-kit/starter-rp-react-ts-webpack)
3. [React (vite) - JavaScript](https://github.com/react-pdf-kit/starter-rp-react-js-vite)
4. [React (vite) - TypeScript](https://github.com/react-pdf-kit/starter-rp-react-ts-vite)
5. [React (vite) - TypeScript - Turborepo](https://github.com/react-pdf-kit/starter-rp-react-vite-ts-turborepo)
6. [Next.js - JavaScript (App Router)](https://github.com/react-pdf-kit/starter-rp-nextjs-app-router-js)
7. [Next.js - TypeScript (App Router)](https://github.com/react-pdf-kit/starter-rp-nextjs-app-router-ts)
8. [Next.js - JavaScript (Pages Router)](https://github.com/react-pdf-kit/starter-rp-nextjs-pages-router-js)
9. [Next.js - TypeScript (Pages Router)](https://github.com/react-pdf-kit/starter-rp-nextjs-pages-router-ts)
10. [Next.js - TypeScript - Turborepo](https://github.com/react-pdf-kit/starter-rp-next-ts-turborepo)
11. [Remix - JavaScript](https://github.com/react-pdf-kit/starter-rp-remix-js)
12. [Remix - TypeScript](https://github.com/react-pdf-kit/starter-rp-remix-ts)
13. [Gatsby - JavaScript](https://github.com/react-pdf-kit/starter-rp-gatsby-js)
14. [Gatsby - TypeScript](https://github.com/react-pdf-kit/starter-rp-gatsby-ts)
15. [Docusaurus - JavaScript](https://github.com/react-pdf-kit/starter-rp-docusaurus-js)
16. [Docusaurus - TypeScript](https://github.com/react-pdf-kit/starter-rp-docusaurus-ts)
17. [Electron - JavaScript](https://github.com/react-pdf-kit/starter-rp-electron-js-vite)
18. [Electron - TypeScript](https://github.com/react-pdf-kit/starter-rp-electron-ts-vite)
21. [React Router - JavaScript](https://github.com/react-pdf-kit/starter-rp-react-router-js)
22. [React Router - TypeScript](https://github.com/react-pdf-kit/starter-rp-react-router-ts)
23. [TanStack - JavaScript](https://github.com/react-pdf-kit/starter-rp-tanstack-router-js)
20. [TanStack - TypeScript](https://github.com/react-pdf-kit/starter-rp-tanstack-router-ts)


# 📝 Changelog

Check out our latest release [v2.1.0 (11 March 2026)](https://docs.react-pdf-kit.dev/introduction/changelog/#v210-11-march-2026?utm_source=github&utm_medium=referral)


# :raising_hand: Need Help?

We are more than happy to help you. If you have any questions, run into any errors or face any problems, please feel free to create an issue in [Issues](../../issues) or PM us directly in [Twitter][twitter]. Anything related to React PDF is on the table!

# :page_facing_up: License

React PDF Kit is distributed under our proprietary license. Please refer to our [License page](https://www.react-pdf-kit.dev/license-agreement?utm_source=github&utm_medium=referral) file for more details.

If you would like to use React PDF commercially, please purchase a license from [our website][reactpdf] or reach out to us directly at [https://www.react-pdf-kit.dev/contact-us](https://www.react-pdf-kit.dev/contact-us?utm_source=github&utm_medium=referral).


# Acknowledgement

- [pdf.js](https://github.com/mozilla/pdf.js)
- [Img Shields](https://shields.io)
- [React.js](https://reactjs.org/)

[reactpdf]: https://www.react-pdf-kit.dev/?utm_source=github&utm_medium=referral
[reactpdf-docs]: https://docs.react-pdf-kit.dev/?utm_source=github&utm_medium=referral
[npm]: https://www.npmjs.com/package/@react-pdf-kit/viewer
[twitter]: https://www.x.com/ReactPDF
