# learn-php
-------------------------------------------------------------

## php variable handlinng functions
<ol>
    <li>is_scalar()--------scalar variable: int, float, string, bool  ----- not scalar variable: array, object, null, resource</li>
    <li>is_array()</li>
    <li>is_object()</li>
    <li>is_null()</li>
    <li>is_resource()-------is a variable a file or not like .txt,.pdf</li>
    <li>is_int() / is_integer() / is_long()</li>
    <li>is_float() / is_double() / is_real()</li> 
    <li>is_string()</li>
    <li>is_bool()</li>
    <li>is_numeric()------4.3,3,0,-9,3.e4</li>     
    <li>gettype()----------return the type of a variable</li>
    <li>settype($a, "integer")-----------set/change the data type of a variable----$a=12; settype($a, "string"); now $a is string</li>
    <li>print_r()-------------mainly it is used to read an array</li>
    <li>var_dump() / var_export() -----------show detailed(datatype(number of char)data) result of a variable</li>
    <li>isset($a)--------------Checks whether a value is set into the variable------set: $a = 0, $a = 'dasd'----not set $a=null</li>
    <li>empty($a)--------------check a variable is empty or not----------emptyp: $a=0/"" not empty: $a=" "------</li>
    <li>unset()------------unset a variable------$a=4----unset($a)----echo $a---now $a is empty</li>
    <li>is_iterable()------------an array is iterable,--------string,int,float are not iterable</li>
    <li>is_countable()-----------array is countable----------string,int,float are not countable</li>
    <li>is_callable("add")----function add(){}</li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
</ol>


## php string handling function
<ol>
    <li>strlen(string)---------return the length of an string-</li>
    <li>strtolower()</li>
    <li>lcfirst() - converts the first character of a string to lowercase</li>
    <li>strtoupper()</li>
    <li>ucfirst()-  converts the first character of a string to uppercase</li>
    <li>ucwords() - converts the first character of each word in a string to uppercase</li>
    <li>addcslashes("Hello World!","W");---------output: Hello \World!</li>
    <li>substr(string, start_index, length)
        <ul>
            <li>echo substr("this is junaid and i am a student",3,20);----start 0 end 20</li>
            <li>substr(string, 20)------start 20 index to end</li>
        </ul>
    </li>
    <li>echo strstr("junaidhossain@gmail.com", "ho");------output:hossain@gmail.com------startstring</li>
    <li>strpos(string,find,start)------------return the position of the first occurrence------echo strpos("I love php, I love php too!","php");-----output: 7</li>
    <li>strrpos() - find the position of the last occurrence---------echo strrpos("I love php, I love php too!","php");-----output: 19</li>
    <li>str_replace(find,replace,string,count)---------str_replace("world","Peter","Hello world!")------Hello Peter--</li>
    <li>trim(string)-------Removes whitespace or other predefined characters from both side ---ltrim()/rtrim()</li>
    <li>explode(seperator, string, limit)------breaks/convert a string into an array, here limit means, how many array item we want-------$str = "Hello world. It's a beautiful day.";--------print_r (explode(" ",$str));---------meaning: string er jei khane space pabe seikhane ekti array item dore array ti banabe-------output: Array ( [0] => Hello [1] => world. [2] => It's [3] => a [4] => beautiful [5] => day. )</li>
    <li>implode(separator, $arr)/join()---------returns a string from the elements of an array.--------$arr =['Hello','World!','Beautiful','Day!']---------output:Hello, World!, Beautiful, Day!;</li>
</ol>


## array methods
<ol>
    <li>count(array)------------return the length of an array</li>
</ol>





## connstant variable in php
- constant variable are global variable
- we can't change the constant variable value

### define(name,value,case_insensitive)
    - Names should be in uppercase letters; name can be start with _(like: _DB)
    - case_insensitive : true- case_insensitive false: case_sensitive(default)
    
    example
    ------------
    define("DB", "localhost");
    echo DB;
    

    
### const
    
    example
    -----------
    const DB = "localhost_localhost";
    echo DB;
#### difference between const and define
| const     | define |
| ------------- | ------------- |
| define constant at compile time  | define constant at run time |
| only hold scalar values(int,float,string,bool) or array  | any php valid expression including scalar,array,function |

```
-------------
compile time
-----------
<?php
    $a=10;
if($a===10){
    const X = 13;
}
echo X;
// it will give a syntex error
?>
-----------
run time
-----------
<?php
    $a=10;
if($a===10){
    define("X", 12);
}
echo X;
// output: 12
?>
    

```

## Data  types and type casting

#### 4 scalar types
    - int
    - float
    - string
    - bool
#### 4 compound type
    - array
    - object
    - callable
    - iterable
#### 2 special types
    - resource
    - null


### type casting refers to convert one data type to another. PHP supports several type casting methods, including implicit and explicit type casting.

#### implicit type casting / type juggling : php engine automatically convert one data type to another, which is known as implicit type casting
    - echo 2 + 3.4  /// 2.0 + 3.4
    - echo "10junaid" + 10   /// 10 + 10 (because php engine first get 10 and ignore the string then add with 10)
    - echo "junaid10" + 10   /// 0 + 10 (because php engine first get string and php take string as 0 and php does not read 10 that with junaid)
    
    
#### explicit type casting is done by programmer

    syntext
    ------------
    (data type) value
    - echo (int / integer) 3.2111            //// 3
    -(float / double / real) "3.323"       ////3.323
    - (boolean / bool) 32       //// 1
    - (string) 32.32  //"32.32"
    

## heredoc
    <!-- 1. the syntex of here doc -->
    ```php
    <?php
    echo <<<MYCV
                my name is junaid
            MYCV
    ?>
    ```
    
    <!-- 2. we can use html tag in heredoc -->
    ```php
    <?php
    echo <<<MYCONTENT
                <h3>this is the heading</h3>
                <p>this is the content of the heredoc</p>
            MYCONTENT;
    ?>
    ```
    <!-- 3. we can use variable -->
    ```php
    <?php
    $name = "junaid";
    $age = 24;
    $university = "Uttara University";

    echo <<<MYRESUME
                My name is $name and i am $age old. I am doing BSc in CSE forom $university;

            MYRESUME;

    ?>
    ```
    <!-- 4. we can put the heredoc into a variable -->
    ```php
    <?php
        $content = <<<CONTENT
                        <p>here is the content of the content</p>
                      CONTENT;
                      echo $content;
    
    ?>
    ```
    
    
    
## array
### indexed array
```
1 
----------
<?php
$arr = ['junaid', 'arman', 'hossain', 'saber'];
foreach($arr as $item){
    echo "name: $item <br>";
}
?>
output: 
name: junaid
name: arman
name: hossain
name: saber
```



```
2 indexed array with index number
--------------------------------
<?php
$arr = ['junaid', 'arman', 'hossain', 'saber'];
foreach($arr as $key=> $item){
    echo "$key ------> name----> $item <br>";
}
?>
output:
0 ------> name----> junaid
1 ------> name----> arman
2 ------> name----> hossain
3 ------> name----> saber

```

### associative array

```
<?php
$arr = [
    'name'=> 'junaid',
    'age'=> '24',
    'religion'=> 'islam',
];
foreach($arr as $key=> $item){
    echo "$key----->$item <br>";
}
?>
output:
name----->junaid
age----->24
religion----->islam
```


---------------------------------------------
# PHP advanced
---------------------------------------------
## Date andTime

### date(format, timestamp)
    date
    ------
    echo date('Y-m-d');   // 2023-12-09
    // Y----year like 2023
    // y----year like 23
    // m----month like 12
    // d----day   like 03
    // l-----day name like wednessday
    |
    |
    time
    -------
    echo date('h:i:s a'); // 12:29:34 am----- take time from server. this is not real time
    // h-----hour like 1-12
    // H------hour like 0-23
    // i ----- minutes like 00-59
    // s-------seconds like 00-59
    //a---------like am/pm
    //A--------like AM/PM
    |
    |
    get time of a specific location with date_default_timezone_set(timezone);
    ----------------------------------
    date_default_timezone_set("asia/dhaka");
    echo "The time is " . date("h:i:sa");
    now, it will give us a proper time  timezones: https://www.php.net/manual/en/timezones.php" 
    |
    |
    make a date time using mktime(hour, minute, second, month, day, year)
    -----------------------
    $d=mktime(11, 14, 54, 8, 12, 2014);
    echo "Created date is " . date("Y-m-d h:i:sa", $d);
    

    
    
 
 
## File include

| include  | require |
| ------------- | ------------- |
| execution of the script continues when an error occured  | execution of the script stops when an error occured   |
| we will use this | not |

once---- amra ekta file jotobar ei include_once ba require_once kori na keno, just ekbar ei file ti pabe. sobar uporer file ti beshi priority pabe.
    
    
## File handling
#### readfile("filename.ext")
   
        echo readfile("info.txt");
        
  
    
    
    
    
    
    
    
    
    
    
    
## super global variable in php
   

   
### $_SERVER[]
### $_REQUEST["input_name"]--> which is used to collect data after submitting an HTML form. method: get/post
### $_POST["input_name]--> used to collect data after submitting html form . method: post
### $_POST["input_name]--> used to collect data after submitting html form . method: post
    
    
    
    
    
    
    
    
    
    
