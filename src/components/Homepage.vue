<script setup>
import { ref } from 'vue'
const email = ref('')
const password = ref('')
const first = ref('')
const last = ref('')
const checkifEmpty = (value) => {
    return value === ''
}
const submit = (e) => {
    e.preventDefault()
    if(email.value === '' || password.value === '' || first.value === '' || last.value === ''){
        alert('Please fill in all fields')
    }else{
        alert('Form submitted')
    }
}
const check = (value) => {
    return value === ''
}
</script>

<template>
    <div class="container">
        <div class="flex">
            <div class="card">
                <div class="text-flex">
                    <h2>Learn to code by watching others</h2>
                    <p>See how experienced developers solve problems in real-time. Watching scripted tutorials is great, but understanding how developers think is invaluable.</p>
                </div>
            </div>
            <div class="f-card">
                <div class="header-text">
                    <h3>Try it free 7 days <span>then $20/mo. thereafter</span></h3>
                </div>
                <div>
                    <form @submit="submit" class="form">
                        <input v-model="first" type="text" name="first" id="first" placeholder="First Name">
                        <span v-if="!checkifEmpty">add the first name</span>
                        <input v-model="last" type="text" name="last" id="last" placeholder="Last Name">
                        <input v-model="email" type="email" id="email" placeholder="email@example.com">
                        <input v-model="password" type="password" name="psw" id="psw" placeholder="Password">
                        <div class="btn">
                            <button type="submit">CLAIM YOUR FREE TRIAL</button>
                            <p>By clicking the button you are agreeing to our <span>Terms and Services</span></p>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</template>
<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
body{
    font-family: 'Poppins', sans-serif;
    background-color: hsl(0, 100%, 74%);
    width: 100%;
    height: 100vh;
    
}

.container{
    width: 100%;
    height: 100dvh;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-image: url('//src/assets/images/bg-intro-desktop.png');
    background-size: cover;
    background-repeat: no-repeat;
}
.flex{
    display: flex;;
    justify-content: center;
    align-items: center;
    gap: 20px;
    width: 100%;
}
.card{
    width: 50%;
    padding: 10%;
}

.f-card{
    width: 50%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 20px;
}
.form{
    display: flex;
    flex-direction: column;
    width: 540px;
    gap: 20px;
    background-color: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 4px 4px 8px hsl(249, 10%, 26%);
}
input{
    width: 100%;
    height: 50px;
    border:  1px solid hsla(249, 10%, 26%, 0.524);
    border-radius: 5px;
}
input::placeholder{
    padding-left: 10px;
    font-family: 'Poppins', sans-serif;
    font-size: 15px;
    color: hsl(249, 10%, 26%);
}
.btn{
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    gap: 10px;
}

.header-text{
    text-align: center;
    background-color: hsl(248, 32%, 49%);
    color: white;
    font-size: 15px;
    font-weight: 700;
    padding: 15px;
    border-radius: 10px;
    box-shadow: 4px 4px 8px hsl(249, 10%, 26%);
    width: 540px;
}
.header-text span{
    font-weight: 400;
}
button{
    width: 100%;
    height: 50px;
    background-color: hsl(154, 59%, 51%);
    color: white;
    border: none;
    border-radius: 5px;
    font-family: 'Poppins', sans-serif;
    font-size: 15px;
    cursor: pointer;
}
p{
    font-family: 'Poppins', sans-serif;
    font-size: 14px;
    font-weight: 400;
    color: hsl(249, 10%, 26%);
}
.btn span{
    color: hsl(0, 100%, 74%);
    font-weight: 700;
}
.text-flex{
    display: flex;
    flex-direction: column;
    gap: 20px;
    color: white;
    text-align: start;
}
h2{
    font-family: 'Poppins', sans-serif;
    font-size: 50px;
    font-weight: 700;
    color:white
}
.text-flex p{
    font-family: 'Poppins', sans-serif;
    font-size: 16px;
    font-weight: 500;
    color: white;
}

</style>