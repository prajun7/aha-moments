# Notes

  > [Array](https://github.com/prajun7/aha-moments#array)<br>
  > [ArrayList](https://github.com/prajun7/aha-moments#arraylist)<br>
  > [Linked List](https://github.com/prajun7/aha-moments#linkedlist)<br> 
  > [HashSet](https://github.com/prajun7/aha-moments#hashset)<br>
  > [TreeSet](https://github.com/prajun7/aha-moments#treeset)<br>
  > [HashMap](https://github.com/prajun7/aha-moments#hashmap)<br>
  > [TreeMap](https://github.com/prajun7/aha-moments#treemap)<br>
  > [Queue](https://github.com/prajun7/aha-moments#queue)<br>
  > [Stack](https://github.com/prajun7/aha-moments#stack)<br>
  > [SQL](https://github.com/prajun7/aha-moments#structured-query-language-sql)<br>
  > [JavaScript](https://github.com/prajun7/aha-moments#javascript)<br>
  > [React.js](https://github.com/prajun7/aha-moments#reactjs)<br>
  > [ASP.NET](https://github.com/prajun7/aha-moments#aspnet)<br>
  > [Ember.js](https://github.com/prajun7/aha-moments#emberjs)<br>
  > [Spring Boot](https://github.com/prajun7/aha-moments#spring-boot)<br>
  > [Collection Framework](https://github.com/prajun7/aha-moments#collection-framework)<br>
  
  > [Backend to Frontend](https://github.com/prajun7/aha-moments#backend--frontend)<br>
  > [Frontend to Backend](https://github.com/prajun7/aha-moments#backend--frontend)<br>

  - Indexing of array, arraylist starts from 0.
  - The length or the size of the array, arraylist, linkedlist, string starts with 1.     
  
## Array 
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
  
  - For Each
  ```sh
   for (int value : intArray) {
    System.out.println(value);
   }
  ```
  
  ## ArrayList
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

  - Convert ArrayList to array
  ```
  // Creating an empty ArrayList of string type
  ArrayList<String> al = new ArrayList<String>();

  // Populating the ArrayList by custom elements
  al.add("Mike Tyson");
  al.add("Chuck Norris");
  al.add("Roronoa Zoro");
  al.add("Yagami Light");

  // Converting above List to array using toArray()
  // method and storing it in an string array
  String k[] = al.toArray(new String[al.size()]);
  ```
  
  ```sh
  List<Integer> list = new ArrayList<>();
  int[] arr = list.toarray(new int(list.size());
  ```
  > We need to pass in the size of ArrayList to the array.

  - Convert Array to ArrayList
  ```sh
  String[] strArray = new String[] {"house", "plane"};
  List<String> list = new ArrayList(Arrays.asList(strArray));
  ```
  
  ```sh
  Int[] arr = new int[5];
  List<Integer> list = new ArrayList(Arrays.asList(arr));
  ```
  
  - Iterate through all elements in an array list using Iterator
```sh
  Iterator<Integer> iterator = list.iterator();
  while(iterator.hasNext()){
	  Integer key = iterator.next();
	  sysout(key);
}
```

- Extract a portion of an array list
```sh
  List<Integer> portion = list.subList(start,end+1);
```

- Join two array lists
```sh
  list1.addAll(list2)
  //OR
  for(int e : list2)
	  list1.add(e)
```

- Trim the capacity of an array list to the current list size
```sh
  list.trimToSize();
```
 
## LinkedList
- Initiate a LinkedList
```sh
LinkedList<String> cars = new LinkedList<String>();
```

- Iterate through all elements in a linked list using for each remaining
```sh
  Iterator<String> iterator = list.iterator();
  iterator.forEachRemaining(System:out::println);
```

- Swap two elements in a linked list
```sh
    List<String> list = new LinkedList<>();
    list.add("Apple");
    list.add("Banana");
    list.add("Orange");
    list.add("Mango");

    String temp = list.get(1);
    list.set(1, list.get(3));
    list.set(3, temp);

    System.out.println(list);
```

- Clone an linked list to another linked list
```sh
    LinkedList<String> list2 = (LinkedList<String>) list1.clone();
```

## HashSet
- Iterate through all elements in a hash set
```sh
    Set<String> set = new HashSet<String>(); 
    for (String s : set) {
       System.out.println(s); 
    }
    //OR
    set.add("apple");
    set.add("banana");
    set.add("cherry");

    Iterator<String> itr = set.iterator();
    while (itr.hasNext()) {
      System.out.println(itr.next());
```

- Clone a hash set to another hash set
```sh
   HashSet<String> set1 = HashSet<>();
   HashSet<String> set2 = (HashSet<>) set1.clone();
```

- Convert a hash set to an array
```sh
    HashSet<String> set = new HashSet<>();
    set.add("apple");
    set.add("banana");
    set.add("cherry");

    String[] array = set.toArray(new String[set.size()]);
    System.out.println(Arrays.toString(array)); 

```

## TreeSet
- Create a reverse order view of the elements contained in a given Tree Set
    TreeSet<String> set = new TreeSet<>();
    set.add("red");
    set.add("orange");
    set.add("yellow");
    set.add("green");
    NavigableSet<String> reverseSet = set.descendingSet();
    System.out.println("Reverse set: " + reverseSet);
    
- Find the numbers less than 7 in a Tree Set
```sh
    TreeSet<Integer> set = new TreeSet<>();
    set.add(1);
    set.add(3);
    set.add(5);
    set.add(7);
    set.add(9);


    TreeSet<Integer>lessThanSeven = (TreeSet<Integer>) set.headSet(7);
    System.out.println("Numbers less than 7: " + lessThanSeven);
```

- Get the element in a tree set which is greater than or equal to the given element
```sh
    Integer great = set.ceiling(4);
```

- Get the element in a tree set which is less than or equal to the given element
```sh
    Integer great = set.floor(3);
```

- Get the element in a tree set which is strictly greater than or equal to the given element
```sh
    Integer strictlyGreat = set.higher(3);
```

- Get an element in a tree set which is strictly less than the given element
```sh
    Integer strictlyless = set.lower(5);
```
	
## HashMap
- 

## TreeMap	
- Sort keys in Treemap by using a comparator
```sh 
    TreeMap<String,Integer>map=newTreeMap<>(new Comparator<String>() {
      @Override
      public int compare(String s1, String s2) {
        return s2.compareTo(s1);
      }
    });
    map.put("A", 1);
    map.put("B", 2);
    map.put("C", 3);
    map.put("D", 4);

    System.out.println("TreeMap with sorted keys: " + map);
// TreeMap with sorted keys: {D=4, C=3, B=2, A=1}

```
	
- Get a key-value mapping associated with the greatest key and the least key in a map
```sh
          TreeMap<String, Integer> map = new TreeMap<>();
    map.put("A", 1);
    map.put("B", 2);
    map.put("C", 3);
    map.put("D", 4);

    System.out.println("Original TreeMap: " + map);
    System.out.println("Mapping for greatest key: " + map.lastEntry());
    System.out.println("Mapping for least key: " + map.firstEntry());
    
    // Original TreeMap: {A=1, B=2, C=3, D=4}
    // Mapping for greatest key: D=4
    // Mapping for least key: A=1
```
	
	- Get the first (lowest) key and the last (highest) key currently in a map
```sh
     TreeMap<String, Integer> map = new TreeMap<>();
     map.put("A", 1);
     map.put("B", 2);
     map.put("C", 3);
     map.put("D", 4);

    System.out.println("Original TreeMap: " + map);
    System.out.println("First (lowest) key: " + map.firstKey());
    System.out.println("Last (highest) key: " + map.lastKey());
    
    // Original TreeMap: {A=1, B=2, C=3, D=4}
    // First (lowest) key: A
    // Last (highest) key: D
```

- Get a reverse order view of the keys contained in a given map 
```sh
    TreeMap<String, Integer> map = new TreeMap<>();
    map.put("A", 1);
    map.put("B", 2);
    map.put("C", 3);
    map.put("D", 4);

    NavigableMap<String,Integer>reverseMap = map.descendingMap();
    System.out.println("Original TreeMap: " + map);
    System.out.println("Reverse order view of keys: " + reverseMap);
    // Original TreeMap: {A=1, B=2, C=3, D=4}
    // Reverse order view of keys: {D=4, C=3, B=2, A=1}

```

- Get a key-value mapping associated with the greatest key less than or equal to the given key
```sh
     TreeMap<String, Integer> map = new TreeMap<>();
     map.put("A", 1);
     map.put("B", 2);
      map.put("C", 3);
    map.put("D", 4);

    System.out.println("Original TreeMap: " + map);
    System.out.println("Mapping for greatest key less than or equal to 'C': " + map.floorEntry("C"));
    // Original TreeMap: {A=1, B=2, C=3, D=4}
    // Mapping for greatest key less than or equal to 'C': C=3
 ```
 
 - get the greatest key less than or equal to the given key
 ```sh
    TreeMap<String, Integer> map = new TreeMap<>();
    map.put("A", 1);
    map.put("B", 2);
    map.put("D", 3);
    map.put("E", 4);

    System.out.println("Original TreeMap: " + map);
    System.out.println("Greatest key less than or equal to 'C': " + map.floorKey("C"));
    // Original TreeMap: {A=1, B=2, D=3, E=4}
    // Greatest key less than or equal to 'C': B

 ```
 
 - Get the portion of a map whose keys are strictly less than a given key
 ```sh
      TreeMap<String, Integer> map = new TreeMap<>();
      map.put("A", 1);
      map.put("B", 2);
      map.put("C", 3);
      map.put("D", 4);

      System.out.println("Original TreeMap: " + map);
      NavigableMap<String, Integer> subMap = map.headMap("C", false);
      System.out.println("Submap with keys strictly less than 'C': " + subMap);
      // Original TreeMap: {A=1, B=2, C=3, D=4}
      // Submap with keys strictly less than 'C': {A=1, B=2}
```

- Get the portion of this map whose keys are less than (or equal to, if inclusive is true) a given key
```sh
      TreeMap<String, Integer> map = new TreeMap<>();
      map.put("A", 1);
      map.put("B", 2);
      map.put("C", 3);
      map.put("D", 4);

      System.out.println("Original TreeMap: " + map);
      NavigableMap<String, Integer> subMap = map.headMap("C", true);
      System.out.println("Submap with keys less than or equal to 'C': " + subMap);
      // Original TreeMap: {A=1, B=2, C=3, D=4}
      // Submap with keys less than or equal to 'C': {A=1, B=2, C=3}
```

- Get the least key strictly greater than the given keyReturn null if there is no such key
```sh
      TreeMap<String, Integer> map = new TreeMap<>();
      map.put("A", 1);
      map.put("B", 2);
      map.put("C", 3);
      map.put("D", 4);

      System.out.println("Original TreeMap: " + map);
      System.out.println("Least key strictly greater than 'C': " + map.higherKey("C"));
      // Original TreeMap: {A=1, B=2, C=3, D=4}
      // Least key strictly greater than 'C': D
  ```
  
  - Get a key-value mapping associated with the greatest key strictly less than the given keyReturn null if there is no such key
  ```sh 
      TreeMap<String, Integer> map = new TreeMap<>();
      map.put("A", 1);
      map.put("B", 2);
      map.put("C", 3);
      map.put("D", 4);

      System.out.println("Original TreeMap: " + map);
      System.out.println("Mapping for greatest key strictly less than 'C': " + map.lowerEntry("C"));
      // Original TreeMap: {A=1, B=2, C=3, D=4}
      // Mapping for greatest key strictly less than 'C': B=2
```
 - Get the greatest key strictly less than the given keyReturn null if there is no such key
 ```sh
      TreeMap<String, Integer> map = new TreeMap<>();
      map.put("A", 1);
      map.put("B", 2);
      map.put("C", 3);
      map.put("D", 4);

      System.out.println("Original TreeMap: " + map);
      System.out.println("Greatest key strictly less than 'C': " + map.lowerKey("C"));
      // Original TreeMap: {A=1, B=2, C=3, D=4}
      // Greatest key strictly less than 'C': B
 ```

- Get a NavigableSet view of the keys contained in a map
```sh
      TreeMap<String, Integer> map = new TreeMap<>();
      NavigableSet<String> keys = map.navigableKeySet();
```


## Queue	
- Convert a priority queue to an array containing all of the elements of the queue
``` sh
    String[] arr = queue.toArray(new String[queue.size()]);
```


## Stack
 -


## Structured query language (SQL)
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
  
## JavaScript
 - Artcle about: [If Javascript Is Single Threaded, How Is It Asynchronous?](https://dev.to/bbarbour/if-javascript-is-single-threaded-how-is-it-asynchronous-56gd)
 - Summary of the article
 > Javascript is a single threaded language. This means it has one call stack and one memory heap. As expected, it executes code in order and must finish executing a piece code before moving onto the next. It's synchronous, but at times that can be harmful. For example, if a function takes awhile to execute or has to wait on something, it freezes everything up in the meanwhile.
 > 
 - TimeOut sort :)
 ```sh
 let arr = [100,5000,500,1090,3100, 2000];

arr.forEach(item => {
    setTimeout(() => console.log(item), item);
})
 ```
 
## React.js
  	- Using react.js with TypeScript and JavaScript
  	- Using Material UI's component, [MUI](https://mui.com/)
  	- Using [constate](https://github.com/diegohaz/constate) for the state management
  	- In React we need to use useMemo to stop rerendering every time. 
  	- Even if we change a value in the react, it would rerender all the components.
  	- When we change a value, React rerenders all the components eventhough those components are not using that value.
  	- So, it is little bit difficult to stop rerendering each time. 
  
  
## ASP.NET
	-

## Ember.js
  	- In Ember the page doesn't rerender like it does in React.
  
## Spring Boot
	-

## Collection Framework 
```sh
  ArrayList has a faster access time for retrieving elements but slower insertion and deletion time, while LinkedList has faster insertion and deletion     time but slower access time.
```

## Backend to Frontend
> In Spring Boot, you can create RESTful APIs that can return data in various formats, such as JSON or XML.<br>
> JSON is the most common format used for exchanging data between a Spring Boot backend and a React.js frontend.<br<

> To pass data from a Spring Boot backend to a React.js frontend in JSON format, you can create a REST endpoint in Spring Boot that returns the data as a JSON object.
> Here's an example of a Spring Boot controller method that returns a list of books in JSON format:
```sh
@RestController
@RequestMapping("/books")
public class BookController {

    @Autowired
    private BookService bookService;

    @GetMapping
    public List<Book> getAllBooks() {
        return bookService.getAllBooks();
    }
}
```
> In this example, the @RestController annotation is used to define a REST endpoint for handling HTTP GET requests to the /books URL path. The getAllBooks() method returns a list of Book objects, which is automatically serialized into JSON format by Spring Boot.

> On the React.js side, you can use the fetch() API or a third-party library like Axios or jQuery to make an HTTP GET request to the Spring Boot endpoint and retrieve the JSON data. Here's an example of how to use the fetch() API to get the list of books from the Spring Boot endpoint:
```sh
fetch('/books')
  .then(response => response.json())
  .then(data => {
    // do something with the data
  });
```
> In this example, the fetch() function sends an HTTP GET request to the /books URL path and receives a JSON response. The response.json() method is called to parse the JSON response into a JavaScript object, which can then be used in the data variable.

#### Serialization
> Serialization is the process of converting an object into a format that can be easily transmitted over a network or stored in a file or database. In the case of sending data from a Spring Boot backend to a React.js frontend, serialization is necessary to convert the data into a format that can be transmitted as a response to an HTTP request.

> Serialization is necessary because the data being transmitted needs to be in a format that can be easily understood and interpreted by both the backend and frontend applications. In the case of Spring Boot and React.js, the data is typically serialized into a JSON format, which is a lightweight and widely-used format for transmitting data over the web.

> By serializing the data into a standardized format like JSON, it becomes possible for the backend and frontend applications to communicate with each other in a way that is platform and language independent. This means that the same data can be transmitted and interpreted by a wide variety of different systems and programming languages, which makes it much easier to build interoperable applications.

> In summary, serialization is necessary to convert data into a standardized format that can be transmitted over the web and interpreted by different systems and programming languages. This is essential for building interoperable applications, like a Spring Boot backend and a React.js frontend.

#### Deserialization
> Deserialization is the process of converting a serialized data format, such as JSON, back into an object that can be easily manipulated and understood by the application. In the case of a React.js frontend receiving data from a Spring Boot backend, the data is typically serialized as JSON by the backend and then deserialized by the frontend.

> To deserialize data in React.js, you can use the built-in JSON.parse() method or a third-party library like axios or fetch-jsonp. Here's an example of how to use JSON.parse() to deserialize a JSON response from a Spring Boot backend:
```sh
fetch('/api/books')
  .then(response => response.json())
  .then(data => {
    // parse the JSON data into a JavaScript object
    const books = JSON.parse(data);

    // do something with the deserialized data
    console.log(books);
  });
```
> In this example, the fetch() function is used to make an HTTP request to the Spring Boot backend and receive a JSON response. The response.json() method is called to convert the response into a JSON string, which can then be parsed using JSON.parse() into a JavaScript object. Once the data is deserialized, it can be manipulated and used in the React.js application as needed.

> Alternatively, if you're using a third-party library like axios or fetch-jsonp, deserialization may be handled automatically by the library, depending on how it's configured. For example, with axios, you can set the responseType property to json to automatically deserialize JSON responses:
```sh
axios.get('/api/books', {
  responseType: 'json'
})
  .then(response => {
    // the data has already been deserialized into a JavaScript object
    const books = response.data;

    // do something with the deserialized data
    console.log(books);
  });

```
> In summary, deserialization is the process of converting a serialized data format, such as JSON, back into an object that can be easily manipulated and understood by the application. In React.js, you can use the built-in JSON.parse() method or a third-party library like axios or fetch-jsonp to deserialize JSON responses from a Spring Boot backend.

- response.json()
> The response.json() method in the frontend is used to extract the JSON data from an HTTP response that was received from a server. When you make an HTTP request using the fetch() method or a similar API, you receive a response object that contains information about the response, such as the status code and any headers. However, to access the actual JSON data that was returned by the server, you need to extract it from the response body.

> The response.json() method is a built-in method in JavaScript's Response interface that extracts the JSON data from the response body and returns it as a JavaScript object. The method reads the response body and parses it as JSON, and then returns the resulting object.

> Here's an example of how to use response.json() to extract JSON data from a response object:

```sh
fetch('https://example.com/api/data')
  .then(response => response.json())
  .then(data => {
    // use the parsed JSON data here
    console.log(data);
  });
```

> In this example, we make an HTTP request to the https://example.com/api/data URL using the fetch() method. The then() method is used to handle the response once it is received. The response.json() method is called to extract the JSON data from the response body, and the resulting object is passed to the next then() method for further processing.

> Using response.json() is important because it allows you to work with the JSON data in a JavaScript-friendly format, rather than having to parse it manually or work with it as a string. Once the JSON data has been parsed into a JavaScript object, you can easily manipulate and use it in your code.

#### String is the Boss
> When sending data over the web from a backend to a frontend, the data is typically serialized into a text-based format like JSON. In JSON, all data is represented as strings, even if the original data was a number, boolean, or other type. This means that when you send an integer value from a backend to a frontend using JSON serialization, the integer value will be converted into a string representation of the number during the serialization process.

> However, this does not mean that you can only pass data in the form of strings from a backend to a frontend. When the data is received on the frontend, you can easily convert the string representation of the data back into its original type using appropriate JavaScript methods like parseInt() or parseFloat() for numbers, JSON.parse() for JSON data, or other parsing methods for other data types.

> For example, let's say you are sending a JSON object containing an integer value and a string value from a Spring Boot backend to a React.js frontend:
```sh
@GetMapping("/api/data")
public ResponseEntity<Map<String, Object>> getData() {
    Map<String, Object> data = new HashMap<>();
    data.put("intValue", 42);
    data.put("stringValue", "Hello, world!");
    return ResponseEntity.ok(data);
}
```

> In this example, we define a GET endpoint /api/data in our Spring Boot backend that returns a JSON object containing an integer value of 42 and a string value of "Hello, world!" as the response body.

> On the React.js side, you can then use the response.json() method or a third-party library like axios or fetch-jsonp to extract the JSON data from the response. Once you have the JSON data, you can access the integer value and the string value as follows:

```sh
fetch('https://example.com/api/data')
  .then(response => response.json())
  .then(data => {
    const intValue = parseInt(data.intValue); // Convert the string to an integer
    const stringValue = data.stringValue; // No conversion necessary
    console.log(intValue); // Outputs 42
    console.log(stringValue); // Outputs "Hello, world!"
  });
```

>In this example, we use parseInt() to convert the string representation of the integer back into an actual integer value, and we simply access the string value as a string.

> So, in summary: while data is typically serialized into a text-based format like JSON when sending data from a backend to a frontend, you can still send and receive data of various types, including integers, booleans, strings, arrays, and objects. While the data will be represented as strings during transmission, you can easily convert the string representation back into the original data type using appropriate JavaScript methods on the frontend.

#### Different ways to send data from backend to frontend
- Response body
> The backend can send data as the response body of a HTTP response. This is the most common way to send data from the backend to the frontend.
```sh
@GetMapping("/books/{id}")
public ResponseEntity<Book> getBookById(@PathVariable Long id) {
    Book book = bookService.getBookById(id);
    return ResponseEntity.ok(book);
}
```
> In this example, the backend sends a Book object as the response body.
```sh
fetch('/books/123')
    .then(response => response.json())
    .then(book => {
        // do something with book object
    });
```
> In this example, the frontend fetches the book with ID 123 from the backend and receives a `Book` object as the response body.

- Headers
> The backend can send data in HTTP response headers. This is less common than sending data in the response body, but can be useful in certain situations.
```sh
@GetMapping("/books/{id}")
public ResponseEntity<Book> getBookById(@PathVariable Long id) {
    Book book = bookService.getBookById(id);
    HttpHeaders headers = new HttpHeaders();
    headers.add("X-Book-Id", id.toString());
    return ResponseEntity.ok()
            .headers(headers)
            .body(book);
}
```
> In this example, the backend sends the book ID as a custom header called "X-Book-Id".
```sh
fetch('/books/123')
    .then(response => {
        const bookId = response.headers.get('X-Book-Id');
        return response.json();
    })
    .then(book => {
        // do something with book object
    });
```
> In this example, the frontend fetches the book with ID 123 from the backend and reads the book ID from the custom header.

- Cookies
> The backend can send data in cookies that are set in the HTTP response. Cookies are commonly used to store user session information.
```sh
@GetMapping("/books/{id}")
public ResponseEntity<Book> getBookById(@PathVariable Long id, HttpServletResponse response) {
    Book book = bookService.getBookById(id);
    Cookie cookie = new Cookie("bookId", id.toString());
    response.addCookie(cookie);
    return ResponseEntity.ok(book);
}
```
> In this example, the backend sends the book ID as a cookie called "bookId".
```sh
fetch('/books/123')
    .then(response => response.json())
    .then(book => {
        const cookies = document.cookie;
        const bookId = cookies.split(';').find(c => c.trim().startsWith('bookId='));
        // do something with book object and bookId
    });
```
> In this example, the frontend fetches the book with ID 123 from the backend and reads the book ID from the "bookId" cookie.

- Websockets
> The backend can use websockets to establish a two-way communication channel with the frontend. This allows the backend to send data to the frontend in real-time, without the frontend needing to send a request.
```sh
@MessageMapping("/books/{id}")
@SendToUser("/queue/book/{id}")
public Book getBookById(@PathVariable Long id) {
    Book book = bookService.getBookById(id);
    return book;
}
```
> In this example, the backend sends the book as a message to the user who requested it, using a Spring Websocket @MessageMapping annotation.

```sh
const socket = new SockJS('/websocket');
const stompClient = Stomp.over(socket);
stompClient.connect({}, function(frame) {
    stompClient.subscribe('/user/queue/book/123', function(message) {
        const book = JSON.parse(message.body);
        // do something with book object
    });
});
```
> In this example, the frontend establishes a Websocket connection with the backend, subscribes to the book with ID 123, and receives the book object as a message.


- Server-Sent Events (SSE)
> Similar to websockets, SSE allows the backend to send data to the frontend in real-time, but without the need for a two-way communication channel. The backend simply sends events to the frontend, which can be processed by an event listener.
```sh
@RestController
public class MyRestController {
    @GetMapping(value = "/my-server-sent-events", produces = MediaType.TEXT_EVENT_STREAM_VALUE)
    public Flux<String> myServerSentEvents() {
        return Flux.interval(Duration.ofSeconds(1))
                   .map(i -> "Hello from the server at " + LocalTime.now());
    }
}
```
```sh
const eventSource = new EventSource("http://localhost:8080/my-server-sent-events");

eventSource.onmessage = function(event) {
    const receivedMessage = event.data;
    // Process the received message
    console.log("Received message from server: " + receivedMessage);
};
```
> In this example, we define a REST endpoint on the backend that returns a stream of text event data using the MediaType.TEXT_EVENT_STREAM_VALUE value for the produces attribute. This REST endpoint uses a Flux to emit a message every second.

> On the frontend, we create a new EventSource object and connect to the backend's REST endpoint using the EventSource constructor. We then define an event listener for incoming messages. When a message is received, we can process it as needed.

> Note that Server-Sent Events are a one-way communication protocol, which means that the backend can send messages to the frontend, but the frontend cannot send messages back to the backend using this protocol.

- Push notifications
> The backend can send push notifications to the frontend, which are displayed as notifications on the user's device or browser. This is often used for real-time updates or alerts.
```sh
@RestController
public class MyRestController {
    private final FirebaseMessaging firebaseMessaging;

    public MyRestController(FirebaseMessaging firebaseMessaging) {
        this.firebaseMessaging = firebaseMessaging;
    }

    @PostMapping("/send-push-notification")
    public void sendPushNotification(@RequestBody PushNotificationRequest request) throws FirebaseMessagingException {
        Message message = Message.builder()
                .setNotification(Notification.builder()
                        .setTitle(request.getTitle())
                        .setBody(request.getBody())
                        .build())
                .setToken(request.getDeviceToken())
                .build();
        firebaseMessaging.send(message);
    }
}
```
```sh
const messaging = firebase.messaging();
messaging.requestPermission().then(() => {
    console.log("Notification permission granted.");

    messaging.getToken().then((token) => {
        console.log("Device token:", token);
        // Send the device token to the backend
        sendDeviceTokenToBackend(token);
    }).catch((err) => {
        console.log("Error getting device token:", err);
    });
}).catch((err) => {
    console.log("Error requesting notification permission:", err);
});

messaging.onMessage((payload) => {
    console.log("Received message from server:", payload);
    // Process the received message
});
```
> In this example, we use Firebase Cloud Messaging (FCM) to send push notifications from the backend to the frontend. On the backend, we define a REST endpoint that accepts a `PushNotificationRequest` object as the request body. This object contains the title, body, and device token of the recipient device. We use the FCM `FirebaseMessaging` object to send a message to the specified device using the `send()` method.

> On the frontend, we use the Firebase JavaScript SDK to request permission to receive push notifications and to retrieve the device token. We then send the device token to the backend so that it can send push notifications to this device in the future. When a push notification is received, the `messaging.onMessage()` event listener is triggered, and we can process the received message as needed.

## Frontend to Backend
> To send data from a React.js frontend to a Spring Boot backend, you can use HTTP methods like POST, PUT, or DELETE. Typically, you would use a form or an AJAX request to send the data to the backend.

> Here is an example of sending data from a React.js component using an AJAX request with fetch():
```sh
const data = { name: 'John Doe', age: 30 };

fetch('https://example.com/api/users', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify(data)
})
  .then(response => response.json())
  .then(data => {
    console.log('Success:', data);
  })
  .catch((error) => {
    console.error('Error:', error);
  });	
```
> In this example, we are sending a POST request to the /api/users endpoint with some data in the request body. The JSON.stringify() method is used to convert the data object to a JSON string before sending it to the backend. The headers property is set to specify that we are sending JSON data in the request body.

> On the Spring Boot backend, you can define an endpoint that handles the request and extracts the data from the request body as follows:
	
```sh 
@PostMapping("/api/users")
public ResponseEntity<User> createUser(@RequestBody User user) {
    // Handle the user data here...
    return ResponseEntity.ok(user);
}
```
	
> In this example, we define a POST endpoint /api/users in our Spring Boot backend that accepts a User object as the request body. Spring Boot will automatically deserialize the JSON data in the request body into a User object, which we can then use to create a new user in the backend. Finally, we return the User object in the response body.

> Note that you will need to ensure that the `User` class implements the `Serializable` interface in order for Spring Boot to properly deserialize the JSON data in the request body into a `User` object. Also, make sure to handle any validation or error scenarios appropriately in your backend code.
	
#### JSON.stringify(data)
> In order to send data from a frontend application to a backend API, the data needs to be in a format that can be transmitted over the network. One common format for sending data over the web is JSON (JavaScript Object Notation), which is a text-based data format that is easy to read and write.

> However, in order to send data as JSON, it needs to be converted from a JavaScript object into a JSON string. This is where the JSON.stringify() method comes in.

> The JSON.stringify() method takes a JavaScript object and returns a JSON string representation of that object. This allows us to send the data to the backend in a format that can be easily parsed and understood.

> For example, let's say we have a JavaScript object like this:
```sh
const data = { name: 'John', age: 30 };
```
	
> If we want to send this data to the backend API as JSON, we can use JSON.stringify() to convert it to a JSON string:
```sh
const jsonData = JSON.stringify(data);	
```
> This will result in a JSON string that looks like this:
```sh
{"name":"John","age":30}
```
> We can then send this JSON string to the backend API using an AJAX request, and the backend can parse the JSON data and use it as needed.

> In summary, we use JSON.stringify() to convert JavaScript objects to JSON strings so that we can send the data over the network to the backend API.
	
#### Different ways to send data from frontend to backend
- Query Parameters
> Query parameters are the key-value pairs that are appended to the end of a URL. They are typically used for GET requests and can be easily accessed on the backend using a request object. However, query parameters are limited in size and may not be the best option for sending large amounts of data.
```sh
const name = "John";
const age = 25;
fetch(`/user?name=${name}&age=${age}`)
  .then(response => response.json())
  .then(data => console.log(data));
```
```sh
@GetMapping("/user")
public User getUser(@RequestParam String name, @RequestParam int age) {
  User user = new User(name, age);
  return user;
}
```

- Form Data
> Form data is used for submitting data via a form. It is typically used for POST requests and can be accessed on the backend using a request object. Form data can be sent as key-value pairs or as a serialized string using the application/x-www-form-urlencoded content type.
```sh
const formData = new FormData();
formData.append("name", "John");
formData.append("age", 25);
fetch('/user', {
  method: 'POST',
  body: formData
})
.then(response => response.json())
.then(data => console.log(data));
```
```sh
@PostMapping("/user")
public User createUser(@RequestParam String name, @RequestParam int age) {
  User user = new User(name, age);
  // code to create a new user
  return user;
}
```
	
- JSON
> JSON is a lightweight data interchange format that is commonly used for sending data between frontend and backend. JSON can be easily serialized and deserialized on both the frontend and backend, making it a popular choice for API communication.
```sh
const data = { name: "John", age: 25 };
fetch('/user', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify(data)
})
.then(response => response.json())
.then(data => console.log(data));
```
```sh
@PostMapping("/user")
public User createUser(@RequestBody User user) {
  // code to create a new user
  return user;
}
```

- File Uploads
> When uploading files from the frontend to the backend, you can use the `multipart/form-data` content type to send the data as binary data. The backend can then parse the file data and save it to a database or file system.
```sh
const fileInput = document.querySelector('input[type="file"]');
const formData = new FormData();
formData.append("file", fileInput.files[0]);
fetch('/upload', {
  method: 'POST',
  body: formData
})
.then(response => response.json())
.then(data => console.log(data));
```
```sh
@PostMapping("/upload")
public String handleFileUpload(@RequestParam("file") MultipartFile file) {
  // code to handle file upload
  return "File uploaded successfully!";
}
```
	
- WebSockets
> WebSockets are a bidirectional communication protocol that allows for real-time communication between the frontend and backend. WebSockets can be used to send and receive data in real-time, making them a good option for applications that require real-time updates or notifications.
```sh
const socket = new WebSocket("ws://localhost:8080/chat");
socket.addEventListener("open", event => {
  socket.send("Hello, server!");
});
socket.addEventListener("message", event => {
  console.log(`Received message: ${event.data}`);
});
```
```sh
@ServerEndpoint("/chat")
public class ChatEndpoint {

  @OnMessage
  public void handleMessage(String message, Session session) throws IOException {
    System.out.println("Received message: " + message);
    session.getBasicRemote().sendText("Hello, client!");
  }
}
```
> Note that the backend example for WebSockets is using Java's built-in WebSocket support. Other languages and frameworks may have different ways of handling WebSockets.

- URL parameters
> Sending data via URL parameters or path variables, and it is commonly used to retrieve resources from the server by specifying their unique IDs.
Here's an example of how you can retrieve a book with ID 3 using path variables:
```sh
fetch('/books/3')
  .then(response => response.json())
  .then(data => console.log(data));
```
```sh
@GetMapping("/books/{id}")
public Book getBookById(@PathVariable Long id) {
  // code to retrieve book by ID
  return book;
}
```
> In this example, the {id} in the URL is a path variable that tells Spring to pass the ID value from the URL to the getBookById() method. The value of id in the method signature will be automatically set to the value specified in the URL (in this case, 3).

# To make table

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |


