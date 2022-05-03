<template>
  <h1>Form Lesson</h1>
  <div>
      <h6>Live preview</h6>
      <pre>
          {{JSON.stringify(formValues, null, 2)}}
      </pre>
  </div>
  <form action="">
      <div>
          <label for="input-name">Name</label>
          <input type="text" id="input-name" v-model="formValues.name">
      </div>
      <div>
          <label for="input-profile">Profile Summary</label>
          <textarea id="input-profile" cols="30" rows="10" v-model="formValues.profileSummary" />
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
              <option value="lithania">Lithania</option>
          </select>
      </div>
  </form>
</template>

<script>
export default {
    name: 'FormLessonComponent',
    data(){
        return {
            formValues:
            {
                name: '',
                profileSummary: '',
                country: '',
                jobLocation: []
            }
        }
    },
    methods:
    {

    },
}
</script>

<style>
    form, pre, h6 {
        text-align: left;
    }
</style>