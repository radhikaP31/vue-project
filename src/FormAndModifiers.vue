<template>
  <div> Hello {{greet }}, You are viewing {{ name }},Here is some example of Form Handling and Modifiers </div>
  <p> trim, number, lazy, prevent,  </p>
  <hr>
  <div>
    <pre>
      {{ JSON.stringify(formValues, null, 2)}}
    </pre>
  </div>
  <form @submit.prevent="submitForm">
    <div>
      <label for="name">Name</label>
      <input type="text" name="name" v-model.trim.lazy="formValues.name"/>
    </div>
    <div>
      <label for="profile">Profile Summary</label>
      <input type="text" name="profile" v-model="formValues.profileSummary"/>
    </div>
    <div>
      <label for="country">Country</label>
      <select name="country" id="country" v-model="formValues.country">
        <option value="">Select Country</option>
        <option value="India">India</option>
        <option value="USA">USA</option>
        <option value="UK">UK</option>
      </select>
    </div>
    <div>
      <label for="job-location">Job Location</label>
      <select name="job-location" id="job-location" multiple v-model="formValues.jobLocation">
        <option value="">Select Job Location</option>
        <option value="India">India</option>
        <option value="USA">USA</option>
        <option value="UK">UK</option>
      </select>
    </div>
    <div>
      <input type="checkbox" id="remote-work" v-model="formValues.remoteWork" true-value="yes" false-value="no"/>
      <label for="remote-work">Open to remote work?</label>
    </div>
    <div>
      <label>Skill set</label>
      <input type="checkbox" id="html " value="html" v-model="formValues.skillSet"/>
      <label for="html ">HTML</label>
      <input type="checkbox" id="css" value="css" v-model="formValues.skillSet"/>
      <label for="css ">CSS</label>
      <input type="checkbox" id="javascript" value= "javascript" v-model="formValues.skillSet"/>
      <label for="javascript">JavaScript</label>
    </div>
    <div>
      <label>Years of Experience </label>
      <input type="radio" id="0-2" value="0-2" v-model="formValues.yearsOfExperience" />
      <label for="0-2">0-2</label>
      <input type="radio" id="3-5" value="3-5" v-model="formValues.yearsOfExperience" />
      <label for="3-5">3-5</label>
      <input type="radio" id="6-10" value="6-10" v-model="formValues.yearsOfExperience" />
      <label for="6-10">6-10</label>
      <input type="radio" id="10+" value="10+" v-model="formValues.yearsOfExperience" />
      <label for="10+">10+</label>
    </div>
     <div>
      <label for="name">Age</label>
      <input type="number" age="age" v-model="formValues.age"/>
      <!-- <input @keyup.enter="submitForm" type="number" age="age" v-model="formValues.age" v-model.number="formValues.age" /> its for submit form when press enter-->
    </div>
    <div>
      <button>Submit</button>
    </div>
  </form>
</template>

<script>
export default {
  name: 'App',
  data() {    
    return {
      'greet': 'Good Afternoon',
      name:' Vue App',
      formValues: {
        name: '',
        profileSummary: '',
        country: '',
        jobLocation: [],
        remoteWork: "no",
        skillSet: [],
        yearsOfExperience: '',
        age: '',
      }
    };
  },
  methods: {
   submitForm(event){
     event.preventDefault()
     console.log('Form Values', this.formValues)
   }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}

hr{
  border: 2px solid #035891;
}

label{
      padding-top: 16px;
    font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}
input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}
input [ type= ' text' ],
textarea,
select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height : 1.42857143;
  color:#555;
  background-color: #fff;
  background-image: none;
}
</style>
