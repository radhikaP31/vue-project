<template>
  <div> Hello {{greet }}, You are viewing {{ name }}, Here is some example of Binding methods.</div>
  <div v-text="practice"> </div>
  <div v-html="practice_html"> </div>
  <div v-html="view_alert"> </div>
  <h2 v-bind:id="heading"> {{ heading }}</h2>
  <button v-bind:disabled="isDisabled"> Bind </button>
  <h2 class="underline"> Static Class </h2>
  <h2 class="underline" v-bind:class="dynamic_class"> Dynamic Class </h2>
  <h2 class="underline" v-bind:class="dynamic_class"> Dynamic Class </h2>
  <h2 v-bind:class=" isPromoted && 'promoted' "> Promoted Text</h2>
  <h2 v-bind:class=" isSoldOut ? 'soldout' : 'available' "> Danger!! Warning?</h2>
  <h2 v-bind:class="['available', 'promoted']">Available and Promoted with array</h2>
  <h2 v-bind:class="[isPromoted && 'promoted', isSoldOut ? 'soldout' : 'available']">Available and Promoted With condition</h2>
  <h2 v-bind:class="{
    promoted: isPromoted,
    available: !isSoldOut,
    soldout: isSoldOut,

  }">Available and Promoted With condition array</h2>

  <h2 v-bind:style="{
    color: bindColor,
    fontSize: headerSize,
    }
    ">This is color example with color and font size</h2>

    <h2 v-bind:style="headerTemplateObject"> This is example of style object</h2>

    <h2 v-bind:style="[baseStyleObject, frontStyleObject]"> This is example of style object with array</h2>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      greet: 'Good Afternoon',
      name:' Vue App',
      practice: 'This is practice text display with <b>(v-text)</b>..',
      practice_html: 'This is practice text display with <b>(v-html)</b>..',
      view_alert: `<a href="#" onclick="alert('You are viewing vue.')"> Where am I?</a>`,
      heading: 'Vue Test App Heading (v-bind:id)',
      isDisabled: false,
      dynamic_class: 'danger',
      isPromoted: true,
      isSoldOut: false,
      bindColor: 'orange',
      headerSize: '14px',
      headerTemplateObject: {
        color: 'orange',
        'font-size': '20px',
        padding: '10px',
      },
      baseStyleObject: {
        color: '#035891',
        background: '#adc7d9',
        border: '1px solid #035891',
        padding: '10px',
      },
      frontStyleObject: {
        'font-size': '20px',
        'font-style': 'italic',
      },
    };
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.soldout {
  color: red;
}

.available {
  color: green;
}
</style>
