# Notes

  - Indexing of array, arraylist starts from 0.
  - The length or the size of the array, arraylist, linkedlist, string starts with 1. 

#### Array:
  - Initiating array of size 20: 
  ```sh
    int[] intArray = new int[20];
  ```
  
  - In a situation where the size of the array and variables of the array are already known, array literals can be used: 
  ```sh
    int[] intArray = new int[]{ 1,2,3,4,5,6,7,8,9,10 };
  ```
  
  - Get length of the array by using `length`:
  ```sh
    string[] strArray = new string[]{ "one", "two", "three", "four", "five", "six", "seven" };
    int size = strArray.length
    // size will be 7
  ```
  
  - Accessing Array Elements using for Loop:
  ```sh
  for (int i = 0; i < arr.length; i++) {
    System.out.println("Element at index " + i + " : "+ arr[i]);
  }
  ```
  
  #### ArrayList:
  `import java.util.ArrayList;`
  

  
  > We cannot specify int as the type of an ArrayList. 
 An int is not a "ReferenceType." 
 We have to use Integer as the type because ArrayLists can only hold objects, not primitive values.
 Infact we cannot use any primitive type in ArrayList.
 Primitive types are the most basic data types available within the Java language. 
 There are 8: boolean , byte , char , short , int , long , float and double

  - Initiate an ArrayList
  ```sh
  ArrayList<Integer> cars = new ArrayList<Integer>();
  ```
  ```sh
  ArrayList<String> cars = new ArrayList<String>();
  ```
  - Add elements 
  >   Syntax: add(object)
  ```sh
        cars.add("Honda");
  ```
 > Syntax: add(int index, object)
  ```sh
        cars.add(2, "Toyota");
  ```
  
  - Add elements while initializing
  ```sh
  List<String> places = Arrays.asList("Buenos Aires", "Córdoba", "La Plata");
  ```
  > Or if you have only one element:
  ```sh
  List<String> places = Collections.singletonList("Buenos Aires");
  ```
  > This would mean that above list is immutable (trying to change it will cause an UnsupportedOperationException exception to be thrown).
  > To make a mutable list that is a concrete ArrayList you can create an ArrayList from the immutable list:
  ```sh
  ArrayList<String> places = new ArrayList<>(Arrays.asList("Buenos Aires", "Córdoba", "La Plata"));
  ```
  > And import the correct package:
`import java.util.Arrays;`
 
#### Linked List Implementation:
- Initiate a Linked List
```sh
LinkedList<String> cars = new LinkedList<String>();
```





#### Queue Implementation:


#### Stack Implementation: 


#### Basic SQL:
- Select all the rows from a table
```sh
SELECT * FROM table_name;
```
>These will select all the rows from the given table. It will better to use WHERE clause or LIMIT,
```sh
SELECT * FROM stores WHERE store_id = 200;
```
```sh
SELECT * FROM reports WHERE store_id = 200 LIMIT 10; 
```

- Alter table to add a column
```sh
ALTER TABLE table_name ADD column_name VARCHAR (255) NOT NULL DEFAULT 'default_name' AFTER some_column_name; 
```
> That is, to add a settings to a  `stores` table we can add a column called `has_analytics` with default value of `0`, which represents `False`

```sh
ALTER TABLE stores ADD has_analytics tinyint NOT NULL DEFAULT 0;
```

### We are using React.js for the frontend and ASP.NET for the backend.
#### React.js
  - Using react.js with TypeScript and JavaScript
  - Using Material UI's component, [MUI](https://mui.com/)
  - Using [constate](https://github.com/diegohaz/constate) for the state management
  
  - In React we need to use useMemo to stop rerendering every time. 
  - Even if we change a value in the react, it would rerender all the components.
  - When we change a value, React rerenders all the components eventhough those components are not using that value.
  - So, it is little bit difficult to stop rerendering each time. 


### We are using Ember.js for the frontend and spring boot for the backend.
#### Ember.js
  - In Ember the page doesn't rerender like it does in React.





# --------------------------------------------------------------------------

# Dillinger
## _The Last Markdown Editor, Ever_

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Dillinger is a cloud-enabled, mobile-ready, offline-storage compatible,
AngularJS-powered HTML5 Markdown editor.

- Type some Markdown on the left
- See HTML in the right
- ✨Magic ✨

## Features

- Import a HTML file and watch it magically convert to Markdown
- Drag and drop images (requires your Dropbox account be linked)
- Import and save files from GitHub, Dropbox, Google Drive and One Drive
- Drag and drop markdown and HTML files into Dillinger
- Export documents as Markdown, HTML and PDF

Markdown is a lightweight markup language based on the formatting conventions
that people naturally use in email.
As [John Gruber] writes on the [Markdown site][df1]

> The overriding design goal for Markdown's
> formatting syntax is to make it as readable
> as possible. The idea is that a
> Markdown-formatted document should be
> publishable as-is, as plain text, without
> looking like it's been marked up with tags
> or formatting instructions.

This text you see here is *actually- written in Markdown! To get a feel
for Markdown's syntax, type some text into the left window and
watch the results in the right.

## Tech

Dillinger uses a number of open source projects to work properly:

- [AngularJS] - HTML enhanced for web apps!
- [Ace Editor] - awesome web-based text editor
- [markdown-it] - Markdown parser done right. Fast and easy to extend.
- [Twitter Bootstrap] - great UI boilerplate for modern web apps
- [node.js] - evented I/O for the backend
- [Express] - fast node.js network app framework [@tjholowaychuk]
- [Gulp] - the streaming build system
- [Breakdance](https://breakdance.github.io/breakdance/) - HTML
to Markdown converter
- [jQuery] - duh

And of course Dillinger itself is open source with a [public repository][dill]
 on GitHub.

## Installation

Dillinger requires [Node.js](https://nodejs.org/) v10+ to run.

Install the dependencies and devDependencies and start the server.

```sh
cd dillinger
npm i
node app
```

For production environments...

```sh
npm install --production
NODE_ENV=production node app
```

## Plugins

Dillinger is currently extended with the following plugins.
Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantaneously see your updates!

Open your favorite Terminal and run these commands.

First Tab:

```sh
node app
```

Second Tab:

```sh
gulp watch
```

(optional) Third:

```sh
karma test
```

#### Building for source

For production release:

```sh
gulp build --prod
```

Generating pre-built zip archives for distribution:

```sh
gulp build dist --prod
```

## Docker

Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the
Dockerfile if necessary. When ready, simply use the Dockerfile to
build the image.

```sh
cd dillinger
docker build -t <youruser>/dillinger:${package.json.version} .
```

This will create the dillinger image and pull in the necessary dependencies.
Be sure to swap out `${package.json.version}` with the actual
version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on
your host. In this example, we simply map port 8000 of the host to
port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=dillinger <youruser>/dillinger:${package.json.version}
```

> Note: `--capt-add=SYS-ADMIN` is required for PDF rendering.

Verify the deployment by navigating to your server address in
your preferred browser.

```sh
127.0.0.1:8000
```

## License

MIT

**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
