<html lang="en" >
<head>
  <meta charset="UTF-8">
  <title>Random Quote Machine</title>

<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous" />

<link rel="stylesheet" href="./styles.css" />
  <style>

  body {




   body {

  background-color: grey;
}

h1 {
  color: red;
}

#quote-box {
  padding-top: 10vh;
  width: 40vw;
  margin-left: auto;
  margin-right: auto;
}

button {
  font-family: monospace;
  font-size: 0.8em;
}

#buttons {
  font-size: 2em;
  text-align: right;
}

#tweet {
  background-color: #f3f7fa;
  border: 1px solid DarkGrey;
}

a {
  text-decoration: none;
}

img {
  height: 0.7em;
}
</style>

</head>
<body>

<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous" />


  <div id="quote-box">
    <article id="text"></article>
    <article id="author"></article>
      <div id="buttons">
        <span id="new-quote"></span>
      </div>
  </div>

  <script src='https://cdnjs.cloudflare.com/ajax/libs/react/18.2.0/umd/react.production.min.js'></script>
  <script type="module" src="./script.js"></script>

</body>
</html>
