<template>
    <div class="profile-content">
      <div class="profile-details">
        <div class="profile-image">
          <img :src="imageSrc" alt="Profile Image">
        </div>
        <h2 class="h2 style3">{{ fullName }}</h2>
        <div class="button-container">
            <a class="button style1" href="#portfolio">portfolio</a>
            <a class="button style1" href="https://drive.google.com/file/d/1ouPciTT6QWkT53NmgSB-9RuKphFIIr0Z/view?usp=drive_link">resume</a>
        </div>
        <h1 class="h1 style2">{{ contactDetails }}</h1>
      </div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const fullName = ref('Name');
const imageSrc = ref('/profile.jpeg');
const contactDetails = ref('Information')

const handlePortfolioClick = () => {
  // Handle Portfolio button click
};

const handleResumeClick = () => {
  // Handle Resume button click
};
</script>

<style scoped>
.profile-content {
  width: 100%; /* Occupy full width of parent */
  height: 100%; /* Occupy full height of parent */
  background-color: #ededed;
  display: flex;
  align-items: center;
  justify-content: center;
}

.profile-details {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.profile-image img {
  width: 240px;
  height: 240px;
  border-radius: 50%;
  border: 10px solid #cedaf0;
  transform: translate(-2%, 5%);
}

.full-name {
  font-size: 5.35em;
  font-family: 'Source Sans Pro';
  letter-spacing: -0.075rem;
  text-align: center;
  color: rgba(0, 0, 0, 0.69);
  font-weight: 800;
  margin-top: 20px;
}

.h1.style2 {
    text-align: center;
    color: rgba(0, 0, 0, 0.69);
    font-family: 'Source Sans Pro', sans-serif;
    letter-spacing: 0.05rem;
    width: calc(100% + 0.05rem);
    font-size: 0.75em;
    line-height: 1.75;
    font-weight: 400;
}

.h2.style3 {
    text-align: center;
    color: rgba(0, 0, 0, 0.69);
    font-family: 'Source Sans Pro', sans-serif;
    letter-spacing: -0.075rem;
    width: 100%;
    font-size: 3.25em;
    line-height: 0.5;
    font-weight: 700;
}

.button-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 1rem;
}

.button {
  background-color: #ff82c5;
  color: black;
  height: 70px;
  padding: 0 20px;
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 1em;
  font-weight: 400;
  letter-spacing: 0.1rem;
  border-radius: 35px;
  margin-right: 10px;
}

.button.style1 {
  display: inline-block;
  width: auto;
  height: 2.5rem;
  line-height: 2.5rem;
  padding: 0 1.25rem;
  vertical-align: middle;
  text-transform: lowercase;
  font-family: 'Source Sans Pro', sans-serif;
  letter-spacing: 0.025rem;
  padding-left: calc(0.025rem + 1.25rem);
  font-size: 1em;
  font-weight: 400;
  border-radius: 2.5rem;
  direction: var(--site-language-direction);
  overflow: hidden;
  text-overflow: ellipsis;
  transition: transform 0.25s ease, color 0.25s ease, background-color 0.25s ease, border-color 0.25s ease;
  text-decoration: none;
}

.button.style1:hover {
  transform: scale(1.05); /* Example: Increase button size on hover */
  background-color: #ff82c5; /* Example: Change background color on hover */
  color: black; /* Example: Change text color on hover */
  cursor: pointer;
}
</style>
