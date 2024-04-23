<template lang="">
<div class="home">
    <h1>{{ title }}</h1>
    <p>{{ disc }}</p>
</div>
<button v-on:click="onClickButton('clicked')">Save</button>
<button v-on:dblclick="onClickButton('double click noticed')">Doubled</button>
<!-- <div>
    <h1>Log in:</h1>
    <h3>enail</h3>
    <input type="email" placeholder="enter your email" v-model="email" />
    <h3>password</h3>
    <input type="password" placeholder="enter your password" v-model="password" />
</div> -->
<div>
    <button v-on:click="onClickLogIn()">
        login
    </button>
</div>
<div>
    <h1>Form</h1>
    <h3>Highest education</h3>
    <div class='edu-fields'>
        <div class='edu-fields-row'>
            <input type="checkbox" value="hsc" id="hsc" v-model="eduction" />
            <label for="hsc"> HSC</label>
        </div>
        <div class='edu-fields-row'>
            <input type="checkbox" value="bachelors" id="bachelors" v-model="eduction" />
            <label for="bachelors"> Bachelors</label>
        </div>
        <div class='edu-fields-row'>
            <input type="checkbox" value="masters" id="masters" v-model="eduction" />
            <label for="masters"> Masters</label>
        </div>
    </div>
    <p>selected education --- {{eduction}}</p>
    <div>
        <button v-on:click="onClickSubmitEduInfo()">
            login
        </button>
    </div>
</div>
</template>

<script>
export default {
    name: 'HomePage',
    props: {
        title: String,
        disc: String,
        data: Object,
    },
    data() {
        return {
            email: null,
            password: null,
            eduction: [],
        };
    },
    methods: {
        onClickSubmitEduInfo() {
            console.log('eduction', this.eduction);
        },
        onClickLogIn() {
            console.log('email', this.email);
            console.log('password', this.password);
        },
        onClickButton(name) {
            console.log(name)
        }
    },
}
</script>

<style scoped>
edu-fields {
    display: flex;
    flex-direction: column;
}

edu-fields-row {
    display: flex;
    flex-direction: row;
}
</style>
