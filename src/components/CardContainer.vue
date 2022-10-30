<script setup>
import Card from "./Card.vue";
</script>

<template>
    <div class="flex flex-col px-5 py-5">
        <card 
            card-title="About Me"
            description="This is the description text"
        ></card>

        <card 
            card-title="Past Work"
            description="This is the past work description text"
        ></card>

        <card 
            card-title="Resume"
            description="This is the resume description text"
        ></card>

        <card 
            card-title="Contact Me"
            description="This is the contact me description text"
        ></card>
    </div>
</template>