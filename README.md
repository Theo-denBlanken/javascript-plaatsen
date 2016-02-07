#JavaScript op verschillende plaatsen in HTML
###Maar wel met veschilende consequenties!
Test dit script maar uit in je browser en kijk telkens wat het gevolg is!

```
<!DOCTYPE html>
<html>
<head>
    <title>demo scriptvolgorde</title>
    <meta charset="UTF-8">
    <meta name="description" content="de volgorde en plaats van javaScript maakt wel degelijk uit">
    <meta name="keywords" content="">
    <meta name="author" content="Theo den Blanken">
    <script>
       window.onload = init;
       function init() {
          document.body.style.color= '#fff';  // tekst wit
       }
       alert('De tekst wordt NIET rood. \nWel een foutmelding in console!');
      document.body.style.color= '#f00';  // tekst rood
       
   </script>
</head>
<body>
   <h1>Je kunt op verschillende plaatsen JavaScript invoegen</h1>
   <script>
      alert('Kijk goed naar de pagina: hij is nog wit, en alleen kop tekst.')
   </script>
   <p>Maar het geeft wel een verschillend resultaat!!</p>
   <p>
      <input type="button" value="klik maar" onclick="alert('Je kon deze knop niet eerder klikken. \nVervelend die alerts!')">
   </p>
<script>
      document.write('Kijk goed naar de pagina: hij is nu oranje, en een paragraaf.');
   document.body.style.backgroundColor= '#f90';
   alert('Bijna klaar met het laden van het hele document. \nDe tekst is nog zwart');
   
   </script>
</body>
</html>
```
[Theo den Blanken](http://blanken5.home.xs4all.nl/)