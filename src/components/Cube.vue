<template>
  <div>
    <input id="input" placeholder="enter your number" />
    <button id="button" @click="computeResult()" type="button">Submit!</button>
    <h3>The cube of the number is: {{results}}</h3>
  </div>
</template>

<script>
export default {
  data() {
    return {
      results: ""
    };
  },
  methods: {
    computeResult() {
      var str = document.getElementById("input").value;
      var charCode = str.charCodeAt(0);
      if (
        charCode > 31 &&
        (charCode < 48 || charCode > 57) &&
        charCode !== 46
      ) {
        alert("Please enter the integer");
      } else {
        this.results = Math.pow(document.getElementById("input").value, 3);
      }
    }
  }
};
</script>

<style scoped>
input {
  position: static;
  margin: 4px 50px;
  left: 50px;
  top: 150px;
  flex: auto;
  padding: 5px;
  display: inline-block;
}

button {
  background-color: #318e63;
  border: none;
  color: black;
  padding: 5px 10px;
  border-radius: 4px;
  text-align: center;
  display: inline-block;
  font-size: 20px;
  font-weight: bold;
  margin: 4px 50px;
  cursor: pointer;
}

button:hover {
  background: #666;
}

h3 {
  margin: 10px 5px 15px 50px;
}
</style>