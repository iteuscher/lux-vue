<template>
  <div class="create">
    <h1> Create your Lux </h1>

    <div class="form-style-5">
      <form class="CreateLuxForm">
        <fieldset>
          <legend><span class="number">1</span> Admin Info</legend>
          <!-- <label class="form5label" for="personalinfo">This info will be used to send you the link to your Lux</label> -->
          <input
            type="text"
            class="adminname"
            placeholder="Your Name *"
            style="
              background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAAAAXNSR0IArs4c6QAAAfBJREFUWAntVk1OwkAUZkoDKza4Utm61iP0AqyIDXahN2BjwiHYGU+gizap4QDuegWN7lyCbMSlCQjU7yO0TOlAi6GwgJc0fT/fzPfmzet0crmD7HsFBAvQbrcrw+Gw5fu+AfOYvgylJ4TwCoVCs1ardYTruqfj8fgV5OUMSVVT93VdP9dAzpVvm5wJHZFbg2LQ2pEYOlZ/oiDvwNcsFoseY4PBwMCrhaeCJyKWZU37KOJcYdi27QdhcuuBIb073BvTNL8ln4NeeR6NRi/wxZKQcGurQs5oNhqLshzVTMBewW/LMU3TTNlO0ieTiStjYhUIyi6DAp0xbEdgTt+LE0aCKQw24U4llsCs4ZRJrYopB6RwqnpA1YQ5NGFZ1YQ41Z5S8IQQdP5laEBRJcD4Vj5DEsW2gE6s6g3d/YP/g+BDnT7GNi2qCjTwGd6riBzHaaCEd3Js01vwCPIbmWBRx1nwAN/1ov+/drgFWIlfKpVukyYihtgkXNp4mABK+1GtVr+SBhJDbBIubVw+Cd/TDgKO2DPiN3YUo6y/nDCNEIsqTKH1en2tcwA9FKEItyDi3aIh8Gl1sRrVnSDzNFDJT1bAy5xpOYGn5fP5JuL95ZjMIn1ya7j5dPGfv0A5eAnpZUY3n5jXcoec5J67D9q+VuAPM47D3XaSeL4AAAAASUVORK5CYII=');
              background-repeat: no-repeat;
              background-attachment: scroll;
              background-size: 16px 18px;
              background-position: 98% 50%;
            "
          />
          <input type="email" class="adminemail" placeholder="Your Email *" />
        </fieldset>
        <fieldset>
          <legend><span class="number">2</span> Lux Info</legend>
          <input type="text" class="luxname" placeholder="Name of your Lux" />
          <textarea
            class="luxdescription"
            placeholder="Description of your Lux"
          ></textarea>
        </fieldset>
        <fieldset>
          <legend><span class="number">3</span> Questions</legend>
          <!-- <label class="form5label" for="questions">Use as many boxes as you have questions (one per box)</label> -->

          <div id="dynamicInput">
            <textarea class="q1" placeholder="Question 1"></textarea>
            <textarea class="q2" placeholder="Question 2"></textarea>
          </div>
          <!-- <input
            class="button addInputButton"
            value="Add question"
            onclick="addInput('dynamicInput');"
          /> -->
          <!-- <input class="button addInputButton" value="Remove question" onclick="removeInput('dynamicInput');"/> -->
        </fieldset>
        <input type="submit" value="Create Lux" />
      </form>
    </div>
  </div>
</template>
<style scoped>
/* form css */
.form-style-5 {
  max-width: 500px;
  padding: 10px 20px;
  background: #f4f7f8;
  margin: 10px auto;
  padding: 20px;
  border-radius: 8px;
  /* font-family: Georgia, "Times New Roman", Times, serif; */
}

.form-style-5 fieldset {
  border: none;
}
.form-style-5 legend {
  font-size: 1.4em;
  margin-bottom: 10px;
}
.form-style-5 label {
  display: block;
  margin-bottom: 8px;
}

/*.form5label {
  display: block;
  margin-bottom: 8px;
  color: black;
}*/

.form-style-5 input[type="text"],
.form-style-5 input[type="date"],
.form-style-5 input[type="datetime"],
.form-style-5 input[type="email"],
.form-style-5 input[type="number"],
.form-style-5 input[type="search"],
.form-style-5 input[type="time"],
.form-style-5 input[type="url"],
.form-style-5 textarea,
.form-style-5 select {
  /* font-family: Georgia, "Times New Roman", Times, serif; */
  background: rgba(255, 255, 255, 0.1);
  border: none;
  border-radius: 4px;
  font-size: 18px;
  margin: 0;
  outline: 0;
  padding: 7px;
  width: 100%;
  box-sizing: border-box;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  background-color: #e8eeef;
  color: rgb(20, 20, 20);
  -webkit-box-shadow: 0 1px 0 rgba(0, 0, 0, 0.03) inset;
  box-shadow: 0 1px 0 rgba(0, 0, 0, 0.03) inset;
  margin-bottom: 20px;
}
.form-style-5 input[type="text"]:focus,
.form-style-5 input[type="date"]:focus,
.form-style-5 input[type="datetime"]:focus,
.form-style-5 input[type="email"]:focus,
.form-style-5 input[type="number"]:focus,
.form-style-5 input[type="search"]:focus,
.form-style-5 input[type="time"]:focus,
.form-style-5 input[type="url"]:focus,
.form-style-5 textarea:focus,
.form-style-5 select:focus {
  border: 1px solid #1abc9c;
  padding: 6px;
}
.form-style-5 select {
  -webkit-appearance: menulist-button;
  height: 35px;
}
.form-style-5 .number {
  background: #1abc9c;
  color: #fff;
  height: 30px;
  width: 30px;
  display: inline-block;
  font-size: 0.8em;
  margin-right: 4px;
  line-height: 30px;
  text-align: center;
  text-shadow: 0 1px 0 rgba(255, 255, 255, 0.2);
  border-radius: 15px 15px 15px 0px;
}

.form-style-5 input[type="submit"],
.form-style-5 input[type="button"] {
  position: relative;
  display: block;
  padding: 19px 39px 18px 39px;
  color: #fff;
  margin: 0 auto;
  background: #1abc9c;
  font-size: 18px;
  text-align: center;
  font-style: normal;
  width: 100%;
  border: 1px solid #1abc9c;
  border-width: 1px 1px 3px;
  margin-bottom: 10px;
  transition: all 0.5s ease;
}
.form-style-5 input[type="submit"]:hover,
.form-style-5 input[type="button"]:hover {
  background: #1dd2af;
}

/* sign up / log in form */
/* @import "compass/css3"; */
*,
*:before,
*:after {
  box-sizing: border-box;
}

.logform_a {
  text-decoration: none;
  color: #1abc9c;
  transition: 0.5s ease;
}
.logform_a:hover {
  color: #1dd2af;
}
.form {
  color: #8a97a0;
  max-width: 500px;
  padding: 10px 20px;
  background: #f4f7f8;
  margin: 10px auto;
  padding: 20px;
  border-radius: 8px;
  /* font-family: Georgia, "Times New Roman", Times, serif; */
  /*background: rgba(19, 35, 47, .9);
  padding: 40px;
  max-width: 600px;
  margin: 40px auto;
  border-radius: 5px;
  box-shadow: 0 4px 10px 4px rgba(19, 35, 47, .3);*/
}
.tab-group {
  list-style: none;
  padding: 0;
  margin: 0 0 40px 0;
}
.tab-group:after {
  content: "";
  display: table;
  clear: both;
}
.tab-group li a {
  display: block;
  text-decoration: none;
  padding: 15px;
  background: #f4f7f8;
  color: #a0b3b0;
  font-size: 20px;
  float: left;
  width: 50%;
  text-align: center;
  cursor: pointer;
  transition: 0.5s ease;
}
.tab-group li a:hover {
  background: #1dd2af;
  color: #fff;
}
.tab-group .active a {
  background: #1abc9c;
  color: #fff;
}
.tab-content > div:last-child {
  display: none;
}
.logform_h1 {
  text-align: center;
  color: rgb(20, 20, 20);
  font-weight: 300;
  margin: 0 0 40px;
}
label {
  position: absolute;
  transform: translateY(6px);
  left: 13px;
  /*color: rgba(255, 255, 255, .5);*/
  transition: all 0.25s ease;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  pointer-events: none;
  font-size: 22px;
}
label .req {
  margin: 2px;
  color: #1abc9c;
}
label.active {
  transform: translateY(50px);
  left: 2px;
  font-size: 14px;
}
label.active .req {
  opacity: 0;
}

input,
textarea {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  background: rgba(255, 255, 255, 0.1);
  border: none;
  border-radius: 4px;
  font-size: 18px;
  margin: 0;
  outline: 0;
  padding: 8px;
  width: 100%;
  box-sizing: border-box;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  background-color: #e8eeef;
  color: rgb(20, 20, 20);
  -webkit-box-shadow: 0 1px 0 rgba(0, 0, 0, 0.03) inset;
  box-shadow: 0 1px 0 rgba(0, 0, 0, 0.03) inset;
  margin-bottom: 10px;
}
input:focus,
textarea:focus {
  border: 1px solid #1dd2af;
  padding: 7px;
}
textarea {
  border: 2px solid #a0b3b0;
  resize: vertical;
  background-color: #e8eeef;
}
.field-wrap {
  position: relative;
  margin-bottom: 40px;
}
.top-row:after {
  content: "";
  display: table;
  clear: both;
}
.top-row > div {
  float: left;
  width: 48%;
  margin-right: 4%;
}
.top-row > div:last-child {
  margin: 0;
}
.logform_button {
  position: relative;
  display: block;
  padding: 19px 39px 18px 39px;
  color: #fff;
  margin: 0 auto;
  background: #1abc9c;
  font-size: 18px;
  text-align: center;
  font-style: normal;
  width: 100%;
  border: 1px solid #1abc9c;
  border-width: 1px 1px 3px;
  margin-bottom: 10px;
  transition: all 0.5s ease;
}
.logform_button:hover,
.logform_button:focus {
  background: #1dd2af;
  transition: all 0.5s ease;
}
.logform_button-block {
  display: block;
  width: 100%;
}
.forgot {
  margin-top: -20px;
  text-align: right;
}
</style>

<script>
let numofquestions = 2;

// eslint-disable-next-line no-unused-vars
function addInput(divName) {
  // if (counter == limit)  { alert("You have reached the limit of adding " + counter + " inputs"); }
  // else {
  let newdiv = document.createElement("div");
  newdiv.innerHTML =
    "<textarea name='myInputs[]' class='q'+ (numofquestions + 1) + ' placeholder='" +
    "Question " +
    (numofquestions + 1) +
    "'></textarea>";
  document.getElementById(divName).appendChild(newdiv);
  numofquestions++;
} // }
// function removeInput(divname){
// if (numofquestions == 1)  { alert("You can't have zero questions!"); }
// else {
//   let questions = document.getElementById('dynamicInput')
//   console.log('numofquestions is at: ' + numofquestions);
//   questions.removeChild(questions.childNodes[numofquestions-1]);
//   numofquestions--;
//   }
// }

// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

// export default {
//   name: 'HomeView',
//   components: {
//     HelloWorld
//   }
// }
</script>
