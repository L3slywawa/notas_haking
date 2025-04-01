#### Description

Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/61864/` or http://jupiter.challenges.picoctf.org:61864

````
 curl -s https://jupiter.challenges.picoctf.org/problem/61864/ -H "Cookie: jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJ
IUzI1NiJ9.eyJ1c2VyIjoibGVzbHkifQ.x7cppWGWTeeJBAyLklwc0NX0s-hiNBc6uaisuRR33Rw" | grep pico



curl -s https://jupiter.challenges.picoctf.org/problem/61864/ -H "Cookie: jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoibGVzbHkifQ.x7cppWGWTeeJBAyLklwc0NX0s-hiNBc6uaisuRR33Rw" | grep pico

`````



```
patoCosmico-picoctf@webshell:~$ ^C
patoCosmico-picoctf@webshell:~$ curl -s https://jupiter.challenges.picoctf.org/problem/61864/ -H "Cookie:eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1
> NiJ9.eyJ1c2VyIjoibGVzbHkifQ.x7cppWGWTeeJBAyLklwc0NX0s-hiNBc6uaisuRR33Rw" | grep pico
patoCosmico-picoctf@webshell:~$ curl -s https://jupiter.challenges.picoctf.org/problem/61864/ -H "Cookie:eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1
> NiJ9.eyJ1c2VyIjoibGVzbHkifQ.x7cppWGWTeeJBAyLklwc0NX0s-hiNBc6uaisuRR33Rw" | grep picurl -s https://jupiter.challenges.picoctf.org/problem/61864/ -H "Cookie:eyJ0eXAiOiJ> curl -s https://jupiter.challenges.picoctf.org/problem/61864/ -H "Cookie:eyJ0eXAiOie: jwt=V1QiLCJhbGciOiJIUzI1kifQ.x7cppWGWTeeJBAyLklwc0NX0s-hiNBc6uaisuRR33Rw" | grep

<!doctype html>
<html>

        <title> JaWT - an online scratchpad </title>
        <link rel="stylesheet" href="/static/css/stylesheet.css">
        <body>
                <header><h1>JaWT</h1> <br> <i><small>powered by <a href="https://jwt.io/">JWT</a></small></i></header>

                <div id="main">

                        <article>
                                <h1>Welcome to JaWT!</h1>

                                <p>
                                        JaWT is an online scratchpad, where you can "jot" down whatever you'd like! Consider it a notebook for your thoughts. <b style="color:blue "> JaWT works best in Google Chrome for some reason. </b>
                                </p>



                                        <p>
                                                You will need to log in to access the JaWT scratchpad. You can use any name, other than <code>admin</code>... because the <code>admin</code> user gets a special scratchpad!
                                        </p>
                                        <br>
                                        <form action="#" method="POST">
                                                <input type="text" name="user" id="name">
                                        </form>
                                        <br>



                                <h2> Register with your name! </h2>

                                <p>
                                        You can use your name as a log in, because that's quick and easy to remember! If you don't like your name, use a short and cool one like <a href="https://github.com/magnumripper/JohnTheRipper">John</a>!
                                </p>

                        </article>
                        <nav></nav>
                        <aside></aside>

                </div>
                <script> window.onload = function() { document.getElementById("name").focus(); }; </script>
        </body> 
</html>> NiJ9.eyJ1c2VyIjoibGVzbHkifQ.x7cppWGWTeeJBAyLklwc0NX0s-hiNBc6uaisuRR33Rw" | grep pico
```