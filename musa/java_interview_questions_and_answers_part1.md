1. What would you rate your Java experience out of 10? 
    * Never rate yourself 10.
    * Best range is 6-8

---

2. What is your Java level? Do you use it in terms of testing only or in terms of development as well?
    * Either answer is correct
    * Because every single function added to the framework is considered development.
    * There will be more Java questions (especially OOP) when you say also for development.

---

3. OOP concepts and how you used them in your last project? 
    * Encapsulation, Inheritance, Abstraction, Polymorphism.
    * Be able to explain each of them one by one, and what you used them for
    * You cannot create objects out of Interfaces
    * Interfaces:
        - WebDriver
        - TakeScreenShot
        - JavaScriptExecutor
    * Polymorphism:
        - In Driver class, we return WebDriver; not ChromeDriver or FirefoxDriver
        - List being referenced to ArrayList
    * Abstraction:
        - WebElement
        - WebDriver
        - List
    * Encapsulation:
        - To get a driver in Driver class

---

4. What do you know about Interface? 
    * An abstraction concept
    * Pure abstraction
    * One class can only inherit from one abstract class, but from multiple interfaces

---

5. What is the benefit of Interface?
    * Interfaces allows us to have multiple Inheritance

---

6. What kind of collections you used in Java? 
    * 3 data structures in Java:
        - Array: I used a List of WebElements
        - Collections: I used Set for getWindowHandles (to handle multiple tabs), checkboxes, dropdownbox. It avoids duplicated elements.
        - Map: For properties file, in database testing.

---

7. How to call the last stored variable in an Array?
    * .length - 1

---

8. Where do you use Set, HashMap, List in your framework? 
    * Set:
        - To get unique options from dropdown
        - To handle multiple tabs
    * Hashmap:
        - Get data from two columns
        - Get data from properties, json file
    * Set does not have index number

---

9. What is the difference between iterator and for/for each loops?
    * Iterator:
        - An Interface
        - Can be used if an object is implementing this Interface
        - For ArrayList, you can use; for arrays, you cannot
        - Main purpose and advantage is to remove the objects
    * For/each loop:
        - As long as there is a data structure, you can use for each loop

---

10. What iterator methods do you use? 
    * hasNext() -> whether there is a next element or not
    * next() -> go to next
    * remove() -> removes the current element

---

11. How do you write or read data from or to file with Java? 
    * Apache library -> Excel
    * FileReader class -> to read a file
    * BufferedReader
        - This is suggested to be explained in interviews
        - a FileReader object needs to be passed
        - readLine(): As you write, skips to the next line
    * Scanner:
        - Instead of System.in, pass the FileReader object
        - hasNextLine() -> whether has a next line or not
        - nextLine() -> gets the next line
        - Reading file is not its only functionality
    * BufferedWriter
        - to write to a file
        - a FileWriter object needs to be passed
        - write() -> To write to a file (accept \n)

---

12. Difference between Heap and Stack? 
    * They are memory locations.

        | Stack                                  | Heap                    |
        | ---                                    | ---                     |
        | Only those within the block are stored | All objects are stored  |
        | Local variables                        | Instances (If a variable written inside class its an instance, not a local one; it belongs to the object)              |

---

13. You have a list of fruits which some of them repeats. How would you write a method which will return a fruit that repeats the most? 
    * Collections.frequency() method

---

14. Java version you are using?
    * 8 is the safest to mention, because it's been there for a long time and an LTS version
    * 11 can also be said
    * Don't say anything below 8, they are no longer in use
    * 12, 9: Outdated, cannot be downloaded anymore

---

15. Abstraction vs Interface? 

    * You can inherit from both at the same time

    |                                                     | Abstraction  | Interface
    |  ---                                                | ---          | ---
    | Is it a class?                                      | Yes          | No
    | Can have constuctor, instance methods & variables?  | Yes          | No, pure abstraction
    | Multiple inheritance?                               | No           | Yes
    | Access modifier?                                    | Any          | only public
    | Access modifier?                                    | Any          | only public
    | Inheritance is done by                              | extends      | implements

---

16. Java generics? 
    * Generics = types
    * Helping us to assure type-safety.

---

17. What is HashMap explain, how do you use in your framework?
    * A class
    * For pair of data
    * Get data from json, properties file, etc.

---

18. What is thread-safe? How do you make your code thread-safe? 
    * Thread is a subsequence of one process. In one subsequence, there can be multiple threads.
    * One action at the time means thread-safety
    * In Java, to achieve thread-safety we use synchronize method or block
        ```java
        public synchronized void method1() { }

        public void method2() {
            synchronized(this) { }
        }

        public static void method3() {
            synchronized(ClassName.class) { }
        } 
        ```

---

19. String builder/buffer differences? 
    * They are both char sequences

    ```java
    // Immutable
    String s1 = new String("A");

    // Mutable
    // Not thread-safe
    StringBuilder s2 = new StringBuilder("B");

    // Mutable
    // Synchorinized: Thread-safe
    // Because of thread-safety, it's slower
    StringBuffer s3 = new StringBuffer("C");
    ```

---

20. How can you achieve abstraction? 
    * Abstract class
    * Interface

---

21. What is the difference between List, Queue and Set? 
    * All are Interfaces
    * Queue has a special order: first-in/first-out order (FIFO)
    * Last-in/First-out: Stack

    |                                                     | List                | Queue                     | Set
    |  ---                                                | ---                 | ---                       | ---
    | Can be implemented by                               | ArrayList, Vector   | LinkedList, PriorityQueue | HashSet, LinkedHashSet, etc.
    | Are duplicates accepted?                            | Yes                 | Yes                       | No
    | Has index number?                                   | Yes                 | No                        | No
    | Has index number?                                   | Yes                 | No                        | No

    ```java
    Queue<String> storeLine = new LinkedList<String>();

    storeLine.add("Johnson");
    storeLine.add("Omar");
    storeLine.add("Matthew");

    System.out.println(bbqline.peek()); // Johnson (shows without deleting from the list)
    System.out.println(bbqline.poll()); // Johnson

    System.out.println(bbqline); // [Omar, Matthew]
    ```

---

22. What is Map?
    * Data structure for pair of data (key-value) 

---

23. How do you iterate over HashMap?
    * values() : All the values
    * keySet() : All the keys
    * Creating an entry: For both
    ```java
    for (Map.Entry<String, Object> entry : map.entrySet()) {
        String key = entry.getKey();
        Object value = entry.getValue();
    }
    ```

---

24. What is garbage? 
    * The object that is not gonna be used anymore
    * Eligible for garbage collection
    * Eligible if does not have a reference
    * Garbage Collector is the process to collect and destroy the object
    * Implicitly done in Java
    * finalize() method is called by Garbage Collector right before collecting any garbage
    ```java
    Boolean b = true;
    b1 = null; // eligible for Garbage Collector

    ArrayList<Integer> list1 = new ArrayList<>(Arrays.asList(1,2,3));
    list1 = new ArrayList<>(); // The one above collected by Garbage Collector

    System.out.println(list1); // []
    ```
---

25. What is class in Java? 
    * Template of the objects
    * Can create (multiple) objects from it
    * Cannot have an object without the class

---

26. What kind of exception you faced and how you handled? 
    * They will ask both for Java and Selenium
    * In Java:
        - ArithmeticException
        - IndexOutOfBoundException
        - NullPointerException
        ```java
        String r1 = null; // No object is created here

        System.out.println(r1.toLowerCase());
        ```
    * In Selenium:
        - In Selenium, you only see Unchecked Exceptions
        - NoSuchElementFound
        - NoSuchWindowFound
        - NoSuchFrameFound

---

27. What is the difference between a HashMap and HashTable? 
    |                         | HashMap  | HashTable
    |  ---                    | ---      | --- 
    | Is synchronized?        | No       | Yes
    | Can take null keyword?  | Yes      | No

---

28. What is Polymorphism? What is Runtime Polymorphism?
    * Focusing on the forms and behaviours of the object
    ```java
    WebDriver driver = new ChromeDriver();
    driver.get(url); // get() method here is the overwritten one (of ChromeDriver)
    ```
    * runtime polymorphism: Method overriding is an example of it

---

29. Give me an example from your framework where you used OOP concepts?
    * Polymorpishm:
        - Driver class
    * Abstraction:
        - WebElement
        - WebDriver
        - List
    * Encapsulation
        - To get a driver in Driver class

---

30. What is global variable?
    * static variable
    * called global because value can be accessed from anywhere
    * cannot call instance variable inside a static method; other way around is doable
    * you don't need an object to access it, just the class

---

31. How do you handle exceptions?
    * try-catch block, and throws keyword if it's a Checked Exception

---

32. Difference between protected and default?
    |                                           | protected                     | default
    | ---                                       | ---                           | --- 
    | Is visible within the same package?       | yes                           | yes
    | Is visible outside of the same package?   | yes, if there is Inheritance  | no

---

33. Can you give “public" access modifier where you are overriding a protected method?
    * Access modifiers has to be same or more visible
        - Because it would be against the is-a relationship: the child class is a fully-fledged instance of the parent class, and must therefore present at least the same interface as the parent class. Making protected/public things less visible would violate this idea
    * In this scenario, only public or protected itself can be given
    * If default: default, protected, or public
    * If private: you cannot override a private method

---

34. How can you find max value in an int array? 
    * Usually, usual sorting methods are not allowed in the interview
    * Create a variable "max", loop through items of the array, replace max as greater is found.

---

35. Can class be final?
    * If it is going to be a super class, it cannot be
    * So, an abstract class cannot be final

---

36. Static methods? 
    * They belong to the class
    * You don't need an object to use it
    * In the framework, these were static:
        - get method in Driver
        - getProperty method in ConfigurationReader
        - all the methods in BrowserUtilities
    * Instance variable cannot be used in a static method

---

37. Static, non-static methods? 
    |                                                | static method    | non-static (instance) method
    | ---                                            | ---              | --- 
    | Belongs to object?                             | no               | yes
    | Static and non-static variables can be used?   | no, only static  | yes
    | Can be overridden?                             | no               | yes

---

38. Up casting, down casting?
    * Polymorphism
    * They are for casting the referance from one type to another

    |             | upcasting          | downcasting
    | ---         | ---                | --- 
    | To type     | smaller to larger  | larger to smaller
    | It is done  | implicitly         | explicitly

    ```java
    List<Integer> l = new Stack<>();
    // List<Integer> l = (List)new Stack<>(); -> You can do upcasting, but not needed since it's automatically done

    l.addAll(Arrays.asList(1,2,3,4,5));

    l.pop(); -> cannot be called. Referance type decides the method you can call.
    ( (Stack)l ).pop(); -> after casting, it works (down-casting)
    ```
    * Referance type decides the method you can call.
    ```java
    Driver driver = new ChromeDriver();
    ( (ChromeDriver)driver.takeScreenShort(); // Down-casting is needed, because TakeScreenShot interface belongs to ChromeDriver
    ( (TakeScreenShot)driver ).takeScreenShot(); // also works
    ```

---

39. What is the difference between final, finally and finalize?
    |                 | final                            | finally              | finalize
    | ---             | ---                              | ---                  | ---
    | Is a            | keyword                          | block                | method
    | Used            | for classes, methods, variables  | if try-catch exists  | called automatically by Garbage Collector to destroy garbage objects

---

40. Tell me how do you understand immutability in java and what is the difference between mutable?
    * Immutability is not being able to change an object after creation
    * String is an immutable class, meaning it has final keyword
    * If immutable, cannot be inherited
    * There will be less memory usage, thus will be faster. Because string literals are stored in String Pool, and duplicates are not repeated.

---

41. Can we have multiple inheritance in java? If yes, how do we achieve that? 
    * For the classes, not possible
    * For Interfaces, it is allowed. By using implements keyword

---

42. How did you implement Polymorphism in your framework? 
    * Driver class -> Making WebDriver as the reference, and ChromeDriver, FirefoxDriver, etc. as the objects

---

43. What could be the reason if you are getting NullPointerException? 
    * null keyword meaning not referencing to no object or instance
    * if you try to call such reference, you will get NullPointerException

---

44. Array or ArrayList to use? Why? 
    * Array is faster

    |                                   | ArrayList                     | array
    | ---                               | ---                           | ---
    | When to use                       | if only dealing with objects  | if primitives are involved
    | Is size automatically adjusted?   | yes                           | no
    | Can adding and removal be done?   | yes                           | no

---

45. Method overloading VS Method Overriding? 
    |                    | Method Overloading              | Method Overriding
    | ---                | ---                             | ---
    | Multiple times?    | yes, same name, different args  | no, one with different implementation
    | Where?             | can also be in the same class   | In subclass
    | Difference?        | parameter must be different     | access modifier same or more visible; return type & params must be different
    | When can be done?  | Any method                      | if not final, private, static
    * abstract methods can be overridden, it's meant to be

---

46. What are the differences between Throw and Throws keyword?
    |             | throws               | throw
    | ---         | ---                  | ---
    | Used for    | handling exceptions  | creating exceptions
    | Used where  | method signature     | within the block
    * throw is used with the object of the Exception class wanted to be created

---

47. Tell me the differences between HashMap and LinkedHashMap? 
    |                              | HashMap | LinkedHashMap
    | ---                          | ---     | ---
    | Accepts null keyword?        | yes     | yes
    | Synchronized (thread-safe)?  | no      | no
    | Keeps insertion order?       | no      | yes

---

48. Tell me the differences between Static and Instance Variable/Block? 
    |                                     | Static Variable/Block | Instance Variable/Block
    | ---                                 | ---                   | ---
    | Objects have their own values for?  | no                    | yes
    | Can be used through class name?     | yes                   | no
    * From one class you can have multiple objects
    * Both static & instance blocks are designed for initializing static & instance varibles
    * Static vars are initialized in static blocks, because it is run one time only
    ```java
    static int a = 100; // Initializing here is OK
    int b;

    static int c;
    static {
        c = 100; // Also OK
    }

    { // Static block
        b = 100;
    }
    ```
---

49. What’s the use of super keyword? What’s the use for this keyword? 
    |                              | super                                  | this
    | ---                          | ---                                    | ---
    | Refers to object instances?  | yes                                    | yes
    | Refers to?                   | instance of super class                | instance of current class
    | super./this. keyword         | instance vars & methods of super class | instance vars & methods
    | super()/this()               | for constuctor of super class          | for the constructor
    * super()
        - called implicitly with no arguments for all classes that have a parent -which is every user-defined class in Java
        - may be called explicitly with arguments if the parent's constructor takes parameters, and you wish to specify them
        - if parent's constructor takes parameters, and it has no default constructor, you will need to call super() with argument(s)
        - has to be at the first line
        - cannot be called more than once

---

50. Why OOP concept is important for producing a software?
    * Reusing the object
    * Reducing the code
    * Preventing repetation
    * Easier maintainability
    * Easier to read
    * Looks cleaner
    * Inheritance is the most important OOP concept. Because, without it, Abstraction and Polymorphism would not be possible.

