<template>
    <div class="flex flex-col px-5 py-5">
        <card 
            card-title="About Me"
            description="Hello! 👋 I'm a full-stack web developer located in the Phoenix metro area. I create websites and business solutions for all kinds of clients. Whether you are a small business or an industry leader, I can build web applications for any problem you face and create modern, SEO-friendly websites for any purpose. Expand the other sections to see some of my latest work!"
            :open="true"
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

<script>
import Card from "./Card.vue";

export default{
    components: {
        Card: Card
    },
}

</script>