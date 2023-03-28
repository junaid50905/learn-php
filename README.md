# learn-php

## php variable handlinng functions
<ol>
    <li>is_array()</li>
    <li>is_bool()</li>
    <li>
        is_callable("add")
        ```php
        function add(){}        
        ```
    </li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
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
