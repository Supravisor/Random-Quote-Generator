<!DOCTYPE html>
<html lang="en" >
<head>
  <meta charset="UTF-8">
  <title>Random Quote Generator</title>
  <link rel="stylesheet" href="./style.css">
<!--- add Post button -->

</head>
<body>

<!-- align *POST* button -->

<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous" />

<style>
   body {
  background-color: grey;
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
 

  <div id="quote-box">
    <article id="text"></article>
    <article id="author"></article>
      <div id="buttons">
        <span id="new-quote"></span>
      </div>
  </div>

  


<script src='https://cdnjs.cloudflare.com/ajax/libs/react/18.2.0/umd/react.production.min.js'></script>

<script type="module">
import ReactDOM from "https://esm.sh/react-dom";

const quotes = [
{
  quote: "Act as if what you do makes a difference. It does.",
  author: "William James" },

{
  quote: "Believe you can and you're halfway there.",
  author: "Theodore Roosevelt" },

{
  quote:
  "Life is like riding a bicycle. To keep your balance, you must keep moving.",
  author: "Albert Einstein" },

{
  quote:
  "You are never too old to set another goal or to dream a new dream.",
  author: "C.S. Lewis" },

{
  quote: "It is never too late to be what you might have been.",
  author: "George Eliot" },

{
  quote:
  "Some people look for a beautiful place. Others make a place beautiful.",
  author: "Hazrat Inayat Khan" },

{
  quote:
  "We must be willing to let go of the life we planned so as to have the life that is waiting for us.",
  author: "Joseph Campbell" },

{
  quote: "Happiness is not by chance, but by choice.",
  author: "Jim Rohn" },

{
  quote:
  "If I cannot do great things, I can do small things in a great way.",
  author: "Martin Luther King, Jr." },

{
  quote: "My mission in life is not merely to survive, but to thrive.",
  author: "Maya Angelou" },

{
  quote: "You are enough just as you are.",
  author: "Meghan Markle" },

{
  quote: "The bad news is time flies. The good news is you're the pilot.",
  author: "Michael Altshuler" },

{
  quote: "You make a life out of what you have, not what you're missing.",
  author: "Kate Morton" },

{
  quote: "There are years that ask questions and years that answer.",
  author: "Zora Neale Hurston" },

{
  quote:
  "All we have to decide is what to do with the time that is given us.",
  author: "JRR Tolkein" },

{
  quote:
  "Do the difficult things while they are easy and do the great things while they are small. A journey of a thousand miles must begin with a single step.",
  author: "Lao Tzu" },

{
  quote: "Each of us is more than the worst thing we've ever done.",
  author: "Bryan Stevenson" },

{
  quote:
  "That is one good thing about this world ... there are always sure to be more springs.",
  author: "LM Montgomery" },

{
  quote: "These things are good things.",
  author: "Dr. Seuss" },

{
  quote: "Pay attention to the present, you can improve upon it.",
  author: "Paulo Coelho" }];



const colors = [
"GreenYellow",
"Gold",
"Orange",
"Aqua",
"CornSilk",
"BlanchedAlmond",
"CornflowerBlue",
"DeepSkyBlue",
"HotPink",
"Khaki",
"LawnGreen",
"Orchid",
"PowderBlue",
"SpringGreen",
"LightSkyBlue",
"LightBlue",
"Thistle",
"Coral",
"Yellow",
"SeaShell"];



class MyQuotes extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      randomIndex: Math.floor(Math.random() * 20) };

    this.handleChange = this.handleChange.bind(this);
  }
  handleChange() {
    this.setState(state => ({
      randomIndex: Math.floor(Math.random() * 20) }));

  }
  render() {

    const quoteStyle = {
      backgroundColor: colors[this.state.randomIndex],
      fontFamily: "Segoe Print",
      fontSize: "2em",
      padding: "1em",
      border: "1px solid black",
      borderRadius: "1em" };

    const quoteMarks = {
      fontFamily: "Candara",
      fontStyle: "italic" };


    return /*#__PURE__*/(
      React.createElement("div", null, /*#__PURE__*/
      React.createElement("article", { style: quoteStyle }, /*#__PURE__*/React.createElement("i", { style: quoteMarks }, "\u201C"), quotes[this.state.randomIndex].quote, /*#__PURE__*/React.createElement("i", { style: quoteMarks }, "\u201D")), /*#__PURE__*/
      React.createElement("br", null), /*#__PURE__*/
      React.createElement(Author, { random: this.state.randomIndex }), /*#__PURE__*/
      React.createElement("button", { className: "btn btn-primary", onClick: this.handleChange }, "New Quote")));
      React.createElement("button", { id: "tweet", class: "btn", type: "button" }, /*#__PURE__*/
      React.createElement("a", { id: "tweet-quote", target: "_blank", href: "https://twitter.com/intent/tweet" }, /*#__PURE__*/
      React.createElement("img", { src: "https://upload.wikimedia.org/wikipedia/commons/thumb/5/53/X_logo_2023_original.svg/240px-X_logo_2023_original.svg.png" }), " Post"));

      React.createElement("span", { style: post }, /*#__PURE__*/
      React.createElement("button", { id: "tweet", class: "btn", type: "button" }, /*#__PURE__*/
      React.createElement("a", { target: "_blank", href: "https://twitter.com/intent/tweet" }, /*#__PURE__*/
      React.createElement("img", { src: "https://upload.wikimedia.org/wikipedia/commons/thumb/5/53/X_logo_2023_original.svg/240px-X_logo_2023_original.svg.png" }), " Post"))))));



class Author extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    var number = this.props.random;
    return /*#__PURE__*/(
      React.createElement("article", { style: authorStyle },
      quotes[number].author));


  }}
;


const authorStyle = {
  fontFamily: "Arial",
  fontSize: "1.7em",
  textAlign: "right" };



ReactDOM.render( /*#__PURE__*/React.createElement(MyQuotes, null), document.getElementById("text"));</script>

</body>
</html>
