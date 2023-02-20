# Notes

### Java Basic:
  - Indexing of array, arraylist starts from 0.
  - The length or the size of the array, arraylist, linkedlist, string starts with 1.

#### Array:
  - Initiating array of size 20: 
  ```
    int[] intArray = new int[20];
  ```
  
  - In a situation where the size of the array and variables of the array are already known, array literals can be used: 
  ```
    int[] intArray = new int[]{ 1,2,3,4,5,6,7,8,9,10 };
  ```
  
  - Get length of the array by using `length`:
  ```
    string[] strArray = new string[]{ "one", "two", "three", "four", "five", "six", "seven" };
    int size = strArray.length
    // size will be 7
  ```
  
  - Accessing Array Elements using for Loop:
  ```
  for (int i = 0; i < arr.length; i++) {
    System.out.println("Element at index " + i + " : "+ arr[i]);
  }
  ```
  
  #### ArrayList:
  

  
#### Linked List Implementation:


#### Queue Implementation:


#### Stack Implementation:

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
