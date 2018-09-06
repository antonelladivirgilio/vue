<template>
    <div class="bear" @mouseleave="mouseOut" @mouseover="mouseOver">
        <div class="ears">
            <div class="ear">
                <div class="ear-left">
                    <div class="pink"></div>
                </div>
            </div>
            <div class="ear">
                <div class="ear-right">
                    <div class="pink"></div>
                </div>
            </div>
        </div>
        <div class="eyes">
            <div class="eye-left">
                <div class="pupil"></div>
            </div>
            <div class="eye-right">
                <div class="pupil"></div>
            </div>
        </div>
        <div class="mouth">
            <div class="nose"></div>
            <div class="union"></div>
            <div class="smile"></div>
        </div>
        <div class="cheek" v-bind:style="{ opacity: opacityVar }">
            <div class="cheek-left">
                <div class="round"></div>
            </div>
            <div class="cheek-right">
                <div class="round"></div>
            </div>
        </div>
    </div>
</template>

<script>


export default {
    name: "Shy bear (／(ｴ)＼)",
    data() {
        return {
            opacityVar: 0
        };
    },
    methods: {
        mouseOver () {      
            this.opacityVar = 1;
        },
        mouseOut () {
            this.opacityVar = 0;
        }
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

    html, body {
        margin: 0;
        width: 100%;
        height: 100%; 
    }

    .ears {
        width: 350px;
        margin: auto; 
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        height: 60px;
        margin-top: -20px;
        font-size: 0;
        z-index: -1;
    }

    .ears .ear {
        width: 50%;
        display: inline-block;
    }

    .ear-left, .ear-right {
        font-size: 14px;
        width: 50px;
        height: 50px;
        margin: auto;   
        background: #eee8da;
        border-radius: 45%; 
        border: 4px solid #603d29;
        position: relative;
    }

    .pink {
        background-color: rgba(227,164,181,1);
        width: 30px;
        height: 30px;
        position: absolute;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        margin: auto;
        border-radius: 50%;

    }

    .bear {
        width: 350px;
        height: 250px;
        position: absolute;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        margin: auto;    
        border-radius: 47%;
        background-color: #eee8da;
        border: 4px solid #603d29;
    }

    .eyes {
        height: 100px;
        font-size: 0;
        margin-top: 30px;
    }

    .eyes .eye-left, .eyes .eye-right {
        height: 100%;
        display: inline-block;
        width: 50%;
        font-size: 14px;    
    }

    .pupil {
        background-color: #603d29;
        width: 20px;
        height: 30px;
        border-radius: 50%;
        margin: auto;
        animation: eyes 5s infinite;
    }

    .mouth {
        background-color: #e3c392;
        margin: auto;
        width: 91px;
        height: 130px;
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        border-radius: 45%;
        margin-top: 30px;
    }

    .mouth .nose {
        width: 15px;
        height: 20px;
        border-radius: 50%;
        margin: auto;
        background-color: #603d29;
        margin-top: 10px;
    }

    .union {
        background-color: #603d29;
        margin: auto;
        width: 3px;
        height: 70px;
    }

    .smile {
        width: 60px;
        height: 40px;
        border: 3px solid;
        border-color: transparent transparent #603d29 transparent;
        border-radius: 42%;
        margin: -45px auto auto auto;
    }

    .cheek {
        font-size: 0;
        width: 100%;
        height: 50px;
        margin-top: -40px;
        transition: opacity .5s;
        opacity: 0;
    }

    .cheek .cheek-left {
        font-size: 14px;
        height: 100%;
        width: 50%;
        display: inline-block;
    }

    .cheek .cheek-right {
        font-size: 14px;
        height: 100%;
        width: 50%;
        display: inline-block;
    }

    .round {
        width: 40px;
        height: 60px;
        background: rgba(227,164,181,0.4);
        border-radius: 50%;
        box-shadow: 0px 0px 60px rgba(227,164,181,1);
        margin: auto;
    }

    @keyframes eyes {
        0% {
            transform: scale(1, 1);
        }
        48% {
            transform: scale(1, 1);
        }
        50% {
            transform: scale(1, .1);
        }
        52% {
            transform: scale(1, 1);
        }
        60% {
            transform: scale(1, 1);
        }
        78% {
            transform: scale(1, 1);
        }
        80% {
            transform: scale(1, .1);
        }
        82% {
            transform: scale(1, 1);
        }
        90% {
            transform: scale(1, 1);
        }    
    }
</style>
