<template>
<h3>Form submission</h3>
<ul>
    <li v-for="item in error" :key="item">
        {{ item }} not valid
    </li>
</ul>
<form>
    <label>First Name : </label>
    <input type="text" name="first_name" v-model="form.first_name"><br><br>
    <label>Last Name : </label>
    <input type="text" name="last_name" v-model="form.last_name"><br><br>
    <label>Country : </label>
    <select v-model="form.country">
        <option>India</option>
        <option>China</option>
        <option>USA</option>
    </select><br><br>
    <p>Technology</p>
    <input type="checkbox" v-model="form.technology" value="java">
    <label>Java</label>
    <input type="checkbox" v-model="form.technology" value="c++">
    <label>C++</label>
    <p>Gender</p>
    <input type="radio" v-model="form.gender" value="female">
    <label>Female</label>
    <input type="radio" v-model="form.gender" value="male">
    <label>Male</label><br><br>
    <button type="button" v-on:click="submitForm">Save</button>
</form>
</template>

<script>
export default {
    name: "FormSubmission",
    data() {
        return {
            form: {
                first_name: '',
                last_name: '',
                country: '',
                technology: [],
                gender: '',
            },
            error : [], 
        }
    },
    methods: {
        submitForm() {
            this.error = [];
            for(const item in this.form){
                if(this.form[item] === '' || this.form[item].length == 0 ){
                    this.error.push(item);
                }
            } 
            if(this.error.length === 0){
                alert('Data has been submitted')
            }
            console.warn(this.error, this.form)
        }
    }
}
</script>
