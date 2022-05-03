<template>
  <h1>Form Lesson</h1>
  <div>
    <h6>Live preview</h6>
    <pre>
          {{ JSON.stringify(formValues, null, 2) }}
      </pre
    >
  </div>
  <form @submit="submitForm">
    <div>
      <label for="input-name">Name</label>
      <input type="text" id="input-name" v-model="formValues.name" />
    </div>
    <div>
      <label for="input-profile">Profile Summary</label>
      <textarea
        id="input-profile"
        cols="30"
        rows="10"
        v-model="formValues.profileSummary"
      />
    </div>
    <div>
      <label for="input-country">Country</label>
      <select id="input-country" v-model="formValues.country">
        <option value="" disabled selected>Select your option</option>
        <option value="latvia">Latvia</option>
        <option value="estonia">Estonia</option>
        <option value="lithania">Lithania</option>
      </select>
    </div>

    <div>
      <label for="input-jobLocation">Job Locations</label>
      <select id="input-jobLocation" multiple v-model="formValues.jobLocation">
        <option value="" disabled selected>Select your option</option>
        <option value="latvia">Latvia</option>
        <option value="estonia">Estonia</option>
        <option value="lithuania">Lithuania</option>
      </select>
    </div>

    <div>
        <input type="checkbox" name="" id="input-remoteWork" v-model="formValues.remoteWork" true-value="Yes" false-value="No">
        <label for="input-remoteWork">Open to remote work?</label>
    </div>

    <div>
        <label>Skill Set</label>
        <input type="checkbox" name="" id="input-html" v-model="formValues.skillSet" value="html">
        <label for="input-html">HTML</label>
        <input type="checkbox" name="" id="input-css" v-model="formValues.skillSet" value="css">
        <label for="input-css">CSS</label>
        <input type="checkbox" name="" id="input-javascript" v-model="formValues.skillSet" value="javascript">
        <label for="input-javascript">JavaScript</label>
    </div>

    <div>
        <label>Years of Experience</label>
        <input type="radio" id="0-2" value="0-2" v-model="formValues.yearsOfExperience">
        <label for="0-2">0-2</label>

        <input type="radio" id="3-5" value="3-5" v-model="formValues.yearsOfExperience">
        <label for="3-5">3-5</label>

        <input type="radio" id="6-10" value="6-10" v-model="formValues.yearsOfExperience">
        <label for="6-10">6-10</label>
    </div>

    <div>
        <button type="submit">Submit</button>
    </div>
  </form>
</template>

<script>
export default {
  name: "FormLessonComponent",
  data() {
    return {
      formValues: {
        name: "",
        profileSummary: "",
        country: "",
        jobLocation: [],
        remoteWork: 'No',
        skillSet: [],
        yearsOfExperience: ''
      },
    };
  },
  methods: {
      submitForm(event){
          event.preventDefault();
          console.log('Form values', this.formValues);
      }
  },
};
</script>

<style>
form,
pre,
h6 {
  text-align: left;
}

form > div {
    margin-bottom: 1rem;;
}

input[type="text"],
textarea,
select {
  display: block;
  width: 25rem;
  padding: 0.31rem 0.75rem;
  font-size: 14px;
  line-height: 1.42857143;
  color: #555;
  background-color: #fff;
  border: 1px solid #ccc;
  border-radius: 4px;
}

label {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}

input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 1.25rem;

}
</style>