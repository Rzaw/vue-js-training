<template>
    <h1>Directives Lesson</h1>
    <div>
        <!-- v-once -->
        <p v-once>{{name}}</p>
        <button @click="name = 'Anna'">Change a name</button>
    </div>

    <div>
        <!-- v-pre - asks Vue to not complie the element -->
        <p v-pre>{{name}}</p>
    </div>
</template>

<script>
export default {
    name: 'DirectivesLessonComponent',
    data() {
        return {
            name: 'Matijs'
        }
    }
}
</script>

<style>

</style>