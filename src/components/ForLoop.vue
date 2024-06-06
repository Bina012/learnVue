<template>
<h1>For Loop in Vue js</h1>
<ul>
    <li v-for="value in technology" :key="value">{{ value }}</li>
</ul>
<br>
<ul>
    <li v-for="item in users" :key="item">
        Name is : {{ item.name }} and age is : {{ item.age }}
    </li>
</ul>
</template>

<script>
export default {
    name: "ForLoop",
    data() {
        return {
            technology: ['Java', 'php', 'node', 'react'],
            users: [{
                    name: 'Ram',
                    age: 36
                },
                {
                    name: 'Shyam',
                    age: 23
                },
            ]
        }
    },
    methods: {

    }
}
</script>
