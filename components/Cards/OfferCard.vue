<template>
    <card-component class="offer_card">
        <div class="offer_card_image">
            <img :src="image" :alt="title">
        </div>
        <div class="offer_card_information">
            <h2 class="offer_card_title">{{ title }}</h2>
            <button class="offer_card_button">
                {{button.text}}
                <img :src="button.image" :alt="button.text">
            </button>
        </div>
    </card-component>
</template>
  
<script>
import Card from './Card.vue';
import cardImage from '@/assets/girl2.png';
import buttonImage from '@/assets/arrow_right.svg';


export default {
    name: 'offer-card-component',
    props: {
        title: {
            type: String,
            default: "Заголовок"
        },
        button:{
            type: Object,
            default: () => ({
                text: "Подробнее",
                image: buttonImage,
            })
        },
        image: {
            type: String,
            default: cardImage   
        }
    },
    components: {
        "card-component": Card
    },
    data(){
      return{}
    },
    computed: {
    },
    methods : {

    }
  }
</script>
  
<style scoped>
    .offer_card {
        height: 454px;
        width: 325px;
    }
    .offer_card_image {
        max-height: 325px;
        width: 100%;
    }
    .offer_card_image img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        margin-bottom: 19px;
    }
    .offer_card_information {
        padding: 19px 40px 30px 40px;
    }
    .offer_card_title {
        font-weight: 400;
        font-size: 30px;
        color: #111;
        margin-bottom: 11px;
    }
    .offer_card_button {
        display: flex;
        align-items: center;
        column-gap: 20px;
        font-weight: 300;
        font-size: 24px;
        color: #111;
        background: transparent;
    }
</style>
