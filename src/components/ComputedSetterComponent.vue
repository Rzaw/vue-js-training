<template>
  <h1>Computed setters lesson</h1>
    <h2>With template litterals - {{firstName}} {{lastName}}</h2>
    <h2>With computed property - {{fullName}}</h2>
    <button @click="changeFullName">Change Full Name</button>
</template>

<script>
export default {
    name: 'ComputedSetterComponent',
    data(){
        return {
            firstName: 'Matijs',
            lastName: 'Lode'
        };
    },
    methods:{
        changeFullName(){
            this.fullName = "Anna Lode"
        }
    },
    computed: {
        fullName: {
            get() {
                return `${this.firstName} ${this.lastName}`
            },
            set(value) {
                const names = value.split(' ');
                this.firstName = names[0];
                this.lastName = names[1];
            }
        }
    }
}
</script>

<style>

</style>