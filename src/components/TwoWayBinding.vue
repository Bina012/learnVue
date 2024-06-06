<template>
<h1>Two way Binding</h1>
<input type="text" v-model="value">
<p>The data is : {{ value }}</p>

<h3 style="color:blueviolet">Get the value of Input field</h3>
<input type="text" placeholder="enter your name" v-model="name"><br><br>
<input type="password" placeholder="enter your password" v-model="password"><br><br>

<input type="checkbox" id="vehicle1" name="vehicle1" value="Bike" v-model="vehicle">
<label for="vehicle1"> I have a bike</label><br>
<input type="checkbox" id="vehicle2" name="vehicle2" value="Car" v-model="vehicle">
<label for="vehicle2"> I have a car</label><br>
<input type="checkbox" id="vehicle3" name="vehicle3" value="Boat" v-model="vehicle">
<label for="vehicle3"> I have a boat</label><br><br>

<h3 style="color:blueviolet">Who am I?</h3>

<input type="radio" id="student" value="student" name="who" v-model="who">
<label for="student">Student</label><br><br>
<input type="radio" id="developer" value="developer" name="who" v-model="who">
<label for="developer">Developer</label><br><br>

<button type="submit" v-on:click="getData()">Save</button>

<div class="form-data">
    <div>
        <p>The name is : {{ name }}</p>
        <p>The password is : {{ password }}</p>
        <p>Selected Vehicle is : {{ vehicle }}</p>
        <p>Selected Profession is : {{ who }}</p>

    </div>
</div>

<h3 style="color:blueviolet">Example of if-else condition</h3>
<p v-if="show">if-condition</p>
<p v-else>else-condition</p>
<button v-on:click="show=!show">Toogle</button>
</template>

<script>
export default {
    name: 'TwoWayBinding',
    data() {
        return {
            value: 0,
            name: '',
            password: '',
            show: true,
            vehicle: [

            ],
            who: [

            ]
        }
    },
    methods: {
        getData() {
            console.warn('The data is', this.name, this.password);
        }
    }
}
</script>

<style scoped>
h1 {
    color: grey;
    font-weight: 100px;
}
</style>
