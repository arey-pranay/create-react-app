Okay so whenever you create-react-app, you mainly get the following folders: node_modules, public, and src.

The node_modules folder doesn't need to be interacted with, in most cases. It is like a place where all the necessary basic modules for the creation of your app are stored.

Then comes the public folder. It has some basic png, svg, etc, which are not very significant. The significant thing in this folder is your index.html file, the only code-based file of this folder. This index.html has the simplest possible structure. It has a head with some meta tags, links, and a title. And the body of this file contains only a single div, with the id of 'root'.

Then finally comes the src folder. It contains all the logic and actual content of your app. The first thing here is the index.js file, it is the only file that needs the ReactDOM import, coz it is responsible for rendering your entire App to the div with 'root' id. So where does this App come from? It comes from the App.js file. Whatever components you make, you can call them in your App.js file like <Component_Name/>
How do you create component? Well, if you want to create a testimonial card, create Testimonial.js in your src, import React at the top, code the component using JSX, and export that component at the end of the file. The abbreviation for the functional components is 'rfce' in VS Code. 
One way of styling react apps using vanilla CSS, is creating a separate CSS file for every JS file. This is why you have App.css and index.css.

A little extra: 
*To use operations, variables, expressions or any kinda logic, you can use {} inside your elements, e.g., <p> My age is {3+16} </p> will result in - My age is 19.

*And yeah, adjacent JSX elements must be enclosed in fragments,
e.g., <> <h1>A</h1>  <h2>B</h2>  </>

*useState hook. It is used by destructuring it into an array, the first member of the array is the state variable, while the second member is the setter function for that variable.
e.g., const [count, setCount] = useState(0). through this the count will be initially equal to 0. Now to change the count you can use something like, <button onClick = {() => setCount((prevCount)=>prevCount-1)} Decrease_Count </button>

*useEffect hook. It is used as: useEffect(() => {what you want to do},[the trigger for this task])
e.g., useEffect(() => {alert("Count changed to"+count)},[count])
