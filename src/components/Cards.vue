<template>
<div style="margin:auto">
    <div class="cards-wrap">
        <div>
            <div class="card">
                <p>{{firstCardLetters[firstCardNum].title}}</p>
            </div>
            <button @click="changeFirstCard">Change Card</button>
        </div>

        <div>
            <div class="card">
                <p>{{midCardLetters[midCardNum].title}}</p>
            </div>
            <button @click="changeMidCard">Change Card</button>
        </div>

        <div>
            <div class="card">
                <p>{{lastCardLetters[lastCardNum].title}}</p>
            </div>
            <button @click="changeLastCard">Change Card</button>
        </div>
    </div>
</div>
</template>

<script>

export default {
    name:"Card",
    data(){
        return{
            firstCardLetters:[
                {
                    id:1,
                    title:"b"
                },
                {
                    id:2,
                    title:"c"
                },
                {
                    id:3,
                    title:"d"
                },
                {
                    id:4,
                    title:"f"
                },
                {
                    id:5,
                    title:"g"
                },
                {
                    id:6,
                    title:"h"
                },
            ],
            firstCardNum:1,
            midCardLetters:[
                {
                    id:1,
                    title:"a"
                },
                {
                    id:2,
                    title:"e"
                },
                {
                    id:3,
                    title:"i"
                },
                {
                    id:4,
                    title:"o"
                },
                {
                    id:5,
                    title:"u"
                }
            ],
            lastCardNum:1,
            lastCardLetters:[
                {
                    id:1,
                    title:"z"
                },
                {
                    id:2,
                    title:"t"
                },
                {
                    id:3,
                    title:"g"
                },
                {
                    id:4,
                    title:"b"
                },
                {
                    id:5,
                    title:"f"
                }
            ],
            midCardNum:1,
        }
    },
    props:["letters"],
    methods: {
        changeFirstCard(){
            var num = Math.floor(Math.random()*this.firstCardLetters.length)
            this.firstCardNum = num
        },
        changeMidCard(){
            var num = Math.floor(Math.random()*this.midCardLetters.length)
            this.midCardNum = num
        },
        changeLastCard(){
            var num = Math.floor(Math.random()*this.lastCardLetters.length)
            this.lastCardNum = num
        }
    },
}
</script>


<style>


</style>