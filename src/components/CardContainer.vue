<template>
    <div class="flex flex-col px-5 py-5">
        <card 
            card-title="About Me"
            :card-type="'aboutMe'"
            :open="true"
        ></card>

        <card 
            card-title="Past Work"
            :card-type="'pastWork'"
        ></card>

        <card 
            card-title="Resume"
            :card-type="'resume'"
        ></card>

        <card 
            card-title="Contact Me"
            :card-type="'contactMe'"
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