# learn-php

<h1>template using heredoc</h1>
    <!-- 1. the syntex of here doc -->
    <?php
    echo <<<MYCV
                my name is junaid
            MYCV
    ?>
    <!-- 2. we can use html tag in heredoc -->
    <?php
    echo <<<MYCONTENT
                <h3>this is the heading</h3>
                <p>this is the content of the heredoc</p>
            MYCONTENT;
    ?>
    <!-- 3. we can use variable -->
    <?php
    $name = "junaid";
    $age = 24;
    $university = "Uttara University";

    echo <<<MYRESUME
                My name is $name and i am $age old. I am doing BSc in CSE forom $university;

            MYRESUME;

    ?>
    <!-- 4. we can put the heredoc into a variable -->
    <?php
        $content = <<<CONTENT
                        <p>here is the content of the content</p>
                      CONTENT;
                      echo $content;
    
    ?>
