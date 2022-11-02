<template>
    <div 
        class="w-full p-5 mb-4 rounded-2xl text-white"
        :class="[expanded ? 'bg-gray-600 shadow-xl' : 'shadow-lg bg-gray-700']"
        @click="toggle"
    >
        <div class="w-full flex flex-row justify-between items-center mb-2"> 
            <h1 class="text-3xl font-bold" style="color: #00eeff;">{{ cardTitle }}</h1>
            <img 
                src="chevron-down.svg" 
                class="h-5 invert cursor-pointer duration-100"
                :class="[expanded ? 'rotate-180' : '']"
                >
        </div>

        <div v-if="this.cardType==='aboutMe'" :class="{ hidden: !expanded}"> 
            <p class="text-justify"> 
                Hello! 👋 I'm a full-stack web developer located in the Phoenix metro area. I create websites and business solutions for all kinds of clients. Whether you are a small business or an industry leader, I can build web applications for any problem you face and create modern, SEO-friendly websites for any purpose. Expand the other sections to see some of my recent work!
            </p>
        </div>

        <div v-if="this.cardType==='pastWork'" :class="{ hidden: !expanded}"> 
            pw
        </div>

        <div v-if="this.cardType==='resume'" :class="{ hidden: !expanded}"> 
            <ul class="mt-4">
                Programming Languages and Tools:
                <li>HTML, CSS, and JS</li>
                <li>Vue and React</li>
                <li>Node, particularly with Express</li>
                <li>TailwindCSS</li>
                <li>PHP Laravel</li>
                <li>MongoDB, Firebase, and mySQL</li>
            </ul>
            <hr />
            <ul>
                Work Experience:
                <li>QA Manager & Software Developer
                    <ul>
                        <li>iVisa.com | 2022-Present</li>
                    </ul>
                </li>
                <li>Freelance Web Designer
                    <ul>
                        <li>2020-Present</li>
                    </ul>
                </li>
                <li>High School English Teacher
                    <ul>
                        <li>2018-2022</li>
                    </ul>
                </li>
            </ul>
            <hr />
            <ul class="mb-4">
                Education:
                <li> Bachelors of Art - SIUe, 2018</li>
            </ul>
        </div>

        <div v-if="this.cardType==='contactMe'" :class="{ hidden: !expanded}"> 
            <ul>
                If you want to get in touch...
                <li class="mt-4">Tweet me <a href="https://www.twitter.com/BryceStabenow" target="_blank" rel="noopener noreferrer">@BryceStabneow</a></li>
                <li><a href="mailto: brycestabenow617@gmail.com">Email me</a></li>
                <li>Follow me on <a href="https://github.com/Bryce-Stabenow">Github</a></li>
                <li>Send a raven to <a href="https://www.youtube.com/watch?v=SkWbkcm0WA8" target="_blank" rel="noopener noreferrer">Winterfell</a></li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        cardTitle: String,
        open: {
            type: Boolean,
            default: false,
        },
        cardType: {
            type: String,
            default: 'aboutMe',
        }
    },

    data() {
        return {
            expanded: this.open,
        };
    },

    methods: {
        toggle(){
            this.expanded = !this.expanded;
        }
    },
}
</script>

<style scoped>
ul{
    list-style: circle inside;
    font-weight: bold;
}
li{
    font-weight: normal;
}
li > ul {
    list-style: square inside;
    margin-left: 2rem;
}
a{
    text-decoration: underline;
    font-weight: bold;
}
a:hover{
    cursor: pointer;
}
hr{
    margin: 2rem auto;
    width: 40px;
}
</style>