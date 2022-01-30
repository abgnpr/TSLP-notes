# JSON

**JavaScript Object Notation**

- a data interchange format
- subset of JavaScript Programming Language (Standard ECMA-262 3rd Edition - December 1999)
- represents data in key-value pairs
- hierarchical
- lightweight
- easy to read and write
- machines can parse and generate
- independent of a programming language
- integrates easily with most languages
- commonly used for APIs and Configs
- used to transfers data between a server and various web applications
- `JSON-RPC` is a Remote Procedure call (RPC) protocol built on JSON, which allows system to send multiple notifications to the server.

Examples: all of the following form valid content of a JSON file

```json
{}
```

```json
[]
```

```json
"hello"
```

```json
true
```

```json
123
```

```json
[1, 2, 3]
```

```json
{
    "key1": "value1",
    "key2": "value2"
}
```

values can be of any data type; keys must be in double quotes

```json
{
    "name": "Abhigyan Prakash",
    "empId": 1987698,
    "isAllocated": true,
    "techSkills": [
        "JAVA",
        "Python",
        "C++"
    ],
    "colleagues": [
        {
            "name": "Md. Asif",
            "empId": 1987434,
            "isAllocated": true,
            "techSkills": [
                "JavaScript",
                "Python"
            ],
            "colleagues": [...]
        },
        {
            "name": "Subhadip Baisya",
            "empId": 1127467,
            "isAllocated": true,
            "techSkills": [
                "Oracle DB",
                "Bash",
                "Linux"
            ],
            "colleagues": [...]
        }
    ]
}
```

```json
[
    {
        "name": "Abhigyan Prakash",
        "empId": 1987698,
        "isAllocated": true,
        "techSkills": [
            "JAVA",
            "Python",
            "C++"
        ]
    },
    {
        "name": "Md. Asif",
        "empId": 1987434,
        "isAllocated": true,
        "techSkills": [
            "JavaScript",
            "Python"
        ],
        "colleagues": [...]
    },
    {
        "name": "Subhadip Baisya",
        "empId": 1127467,
        "isAllocated": true,
        "techSkills": [
            "Oracle DB",
            "Bash",
            "Linux"
        ],
        "colleagues": [...]
    }
]
```



### JSON Data Types

![JSON Syntax](images/6970_Json_Syntax.jpeg)

Data types available

- String
- Number
- Object
- Array
- Boolean
- Null

Data types not available

- function
- date
- Undefined

### Two Important Constructs

JSON is built on two important structures:

- **Object** - A collection of name/value pairs.
- **Array** - An ordered list of values. An array could be a combination of multiple objects.

### JSON vs JavaScript Object

| JSON                                                         | JavaScript Object                               |
| ------------------------------------------------------------ | ----------------------------------------------- |
| It is platform independent                                   | Can only be used within JS                      |
| Keys must be in double quotes                                | Keys need not have quotes                       |
| Keys can only contain `number`,  `string`, `array`  `object`, `null` and `boolean` | Keys can additionally contain `function`        |
| Need to parse JSON object before use                         | Is used directly                                |
| Any valid JSON is a valid JavaScript Object                  | Not all valid JavaScript Objects are valid JSON |

### JSON over XML

JSON is preferred because of the following two important reasons:

- JSON transfers data faster than XML because XML uses tags to describe data which increases their data size.
- JSON uses typed Objects, which can be parsed by any standard JavaScript function. Whereas, XML uses type-less strings, which must be parsed by XML parser (XPath) during run-time, which makes it more complex.

### JSON Methods

- [`JSON.parse()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse)
- [`JSON.stringify()`]()

### JSON Limitations

- JSON cannot handle large data (Need to leverage other formats).
- Not suitable for handling different multimedia formats.
- JSON does not have a feature to support 'comments'.

### JSON MIME Type

**`application/json`**

### JSON Libraries

Apart from the regular JSON, we have other versions of JSON in use as well.

- **JSON Rules Engine** There is a powerful npm package by the name `json-rules-engine`, which has rules built of simple JSON structures and it is very light-weighted.
- **Google's GSON** - Java library from Google to convert Java Objects into JSON and vice versa. In addition, it paves room for simpler implementation by not requiring to annotate your classes.
- **Oracle’s JSONP** is Java API for JSON processing. This consumes/produces streaming JSON text.
- **FasterXML’s Jackson** - Can handle both JSON/non-JSON encodings. It is a set of data processing tools powered with streaming JSON parser and generator library.

### JSON Security Concerns

- **Cross-Site Request Forgery (CSRF)**

  It is an exploit which takes advantage of a website trust in any user browser.

- **Cross-Site Scripting (XSS) attack**

  A type of injection attack that is injecting data into a web application to facilitate the execution or interpretation of malicious data that takes advantage of any normal website by a third party with a malicious script.

##### How to overcome these threats while using JSON

- **Avoid** using **Top-level arrays** which are valid JavaScript that can be linked to a script tag.
- Use **HTTP POST** instead of **HTTP GET** in JSON, because the GET request can be linked to any URL with a script tag which is a web threat.
- Use **JSON.parse()** instead of **eval()**, because eval() function will compile and execute any given set of string, which can open your code during web attacks, where JSON.parse() only parses JSON.