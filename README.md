# learn-php

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
</ol>









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
    
    
    
    
    
    
    
    
    
    
    
    
    
    
