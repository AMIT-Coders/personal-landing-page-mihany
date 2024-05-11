<h1 align="center">Welcome to Web-Dev Workshop</h1>

![a](https://raw.githubusercontent.com/AMIT-Coders/res/main/Colored%20logo.png)
***
# Workshop Agenda :page_with_curl:
- [Day :one:](#Day-1)
- [Day :two:](#Day-2)
- [Day :three:](#Day-3)

***



## Day-1
#### Tools installation
1- Google Chrome [Download from here](https://www.google.com/chrome/)  
2- VS Code [Download from here](https://code.visualstudio.com/download)  
3- Node.js [Download from here](https://nodejs.org/en/download)  

HTML and CSS are the fundamental blocks of any website.
![html-and-css](https://raw.githubusercontent.com/AMIT-Coders/res/main/HTML-and-CSS-768x453.jpg)

###### What is HTML?
![example](https://raw.githubusercontent.com/AMIT-Coders/res/main/HTML-Output-768x286.png)

The following image shows the tree-like structure of the above HTML code. <html> tag is the root element and then we have two child elements <head> and <body>. Inside the <head> tag we have a <title> tag and inside <body> tag we have its 4 child elements as shown in the image. 

![html-tree](https://raw.githubusercontent.com/AMIT-Coders/res/main/HTML-Tree-Structure-768x453.jpg)

###### More explanation:
![example-2](https://raw.githubusercontent.com/AMIT-Coders/res/main/1_WXLuqlDFP0kOrLhPGqFNoQ.webp)
## Day-2
###### An Introduction to TailWind CSS
In the dynamic world of web development, the way we craft user interfaces has seen a profound shift, evolving at an unprecedented rate. Enter TailwindCSS: a utility-first CSS framework that has surged in popularity, reshaping the paradigms of frontend design. Rather than contending with obscure class names or battling specificity wars, Tailwind empowers developers to build responsive, maintainable, and scalable user interfaces with ease. This article dives deep into the intricacies of TailwindCSS, unveiling its transformative potential and elucidating why it has become the go-to choice for many contemporary web developers and designers.

###### Utility-First Approach
The utility-first approach, as championed by TailwindCSS, revolves around building UI components using small, single-purpose utility classes directly in the HTML, rather than predefining fixed styles in separate CSS files. This methodology promotes speed, flexibility, and customizability, as developers compose complex designs from these granular utilities rather than overriding built-in styles. In contrast, traditional frameworks like Bootstrap rely heavily on predefined component classes — think `.btn` or `.card—which` often require modifications or additional classes to achieve specific designs. For instance, to create a blue button with rounded corners in Bootstrap, one might use a combination of classes like `.btn .btn-primary .rounded`. In Tailwind, the same button can be achieved more explicitly and flexibly with utilities such as `bg-blue-500 hover:bg-blue-700 text-white py-2 px-4 rounded`. While the utility-first approach may initially seem verbose, it fosters a higher degree of control and consistency, reducing the need for custom CSS and making design intent more transparent.


###### Creating our Project with TailWind
Let’s create our first project with TailWind CSS. First create a brand new React TypeScript Project

```
npx create-react-app my-project --template typescript
```

Now follow the instructions on the TailWind CSS reference to install TailWind CSS into your react project which starts with running the following in my-project directory:
```
npm install -D tailwindcss
npx tailwindcss init
```

And also altering the content of the generated tailwind.config.js file:
```
/** @type {import('tailwindcss').Config} */
module.exports = {
content: [
    "./src/**/*.{js,jsx,ts,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
Finally add the tailwind references in your index.css file:
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

In order to get the most out of coding with Tailwind, I encourage you to use Visual Studio code to develop your react app and install the Tailwind CSS Intellisense in order to help you autocomplete your Tailwind classes.

#image here vscode plugin

Now let’s see Tailwind in action, We’ll start with a simple hello world in App.tsx:
```
import React from "react";
import logo from "./logo.svg";
import "./App.css";

function App() {
  return (
    <h1 className="text-3xl font-bold underline text-purple-300">
      TailWind Rocks!
    </h1>
  );
}

export default App;
```

These changes in App.tsx will render the following in the browser:

#image here

######  Create a GitHub Account [Sign up](https://github.com/)
Click Sign up button.  
![image](https://github.com/AMIT-Coders/personal-landing-page/assets/60690890/5bd0aa8e-95a3-4b6e-8d35-0f58bf41f64b)  
Use email that has not been used for other GitHub account.  
![image](https://github.com/AMIT-Coders/personal-landing-page/assets/60690890/3ab5caf7-3897-4899-a041-a4c4f9741bc2)  
Type email address and click Continue.  
![image](https://github.com/AMIT-Coders/personal-landing-page/assets/60690890/4c775bb5-ab92-4eb7-bb4d-0a1072c477fa)  
Fill password and try until it says that Password is strong, then click Continue.  
![image](https://github.com/AMIT-Coders/personal-landing-page/assets/60690890/2873189b-5e85-4db5-8f3d-185534a1875f)  
Enter a unique username and click Continue.  
![image](https://github.com/AMIT-Coders/personal-landing-page/assets/60690890/7010ef8d-82b0-427e-9697-95027a497d37)  
Choose option in receiving product updates and announcement via email, then click Continue.  
![image](https://github.com/AMIT-Coders/personal-landing-page/assets/60690890/9c566fa8-83c1-4cb3-baf5-b11433297cce)  
Click Start puzzle to verify as a human.  
![image](https://github.com/AMIT-Coders/personal-landing-page/assets/60690890/d2090f6a-6391-4fcf-9cc0-af8a240be8a4)  
Solve first puzzle.  
![image](https://github.com/AMIT-Coders/personal-landing-page/assets/60690890/96b80a79-ab98-4c1a-925c-78f370006620)  
Solve second puzzle.  
![image](https://github.com/AMIT-Coders/personal-landing-page/assets/60690890/b8d1c9e4-e260-4849-8108-a52e44f0da36)  
Receive message that account is verified, then click Create account.  

## Day-3

Below is a simple example of a personal landing page using HTML and Tailwind CSS. You'll need to include the Tailwind CSS library in your HTML file to use the utility classes provided by Tailwind. Here's a basic implementation:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Name - Personal Landing Page</title>
    <!-- Include Tailwind CSS from CDN -->
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="bg-gray-100 text-gray-800">
    <div class="container mx-auto px-4">
        <header class="text-center py-10">
            <h1 class="text-4xl font-bold text-purple-700">Your Name</h1>
            <p class="text-md text-gray-600">Web Developer | Tech Enthusiast</p>
        </header>
        
        <section class="my-5">
            <h2 class="text-2xl text-gray-700 font-semibold">About Me</h2>
            <p class="mt-3 text-gray-600">
                I am a full-stack web developer with a passion for building beautiful and functional websites. I specialize in HTML, CSS, JavaScript, and have experience with Node.js and React.
            </p>
        </section>

        <section class="my-5">
            <h2 class="text-2xl text-gray-700 font-semibold">Projects</h2>
            <ul class="list-disc pl-5 mt-3 text-gray-600">
                <li>Project One - A brief description of your project.</li>
                <li>Project Two - A brief description of your project.</li>
                <li>Project Three - A brief description of your project.</li>
            </ul>
        </section>

        <footer class="text-center py-10">
            <p>Contact me at <a href="mailto:your.email@example.com" class="text-purple-600 hover:text-purple-800">your.email@example.com</a></p>
        </footer>
    </div>
</body>
</html>
```
