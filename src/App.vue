<template>
  <div>
    <!-- 공통 이벤트 영역 -->
    <common-event-component />
    
    <!-- header 영역 -->
    <header-component />
   
    <!-- about me 영역 -->
    <about-component />

    <!-- projects 영역 -->
    <project-component />

    <!-- footer -->
    <footer-component />
  </div>
  <div class="game">
    <div class="cards">
      <div v-for="(card, index) in cards" :key="index" class="card" @click="cardClick(index)" :class="{ reverse: card.reverse, matched: card.matched }">
        <div class="card-info">
          <div class="card-front"></div>
          <div class="card-back">
            <img :src="card.image" alt="Card" />
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="button-container">
    <button @click="gameStartClick()">게임 시작</button>&nbsp;
    <button @click="resetCards()">다시 시작</button>
  </div>
  
</template>

<script>
export default {
  name: 'App',
}
</script>

<script setup>
import CommonEventComponent from './components/commonEvent-component.vue'
import HeaderComponent from './components/header-component.vue'
import AboutComponent from './components/about-component.vue'
import ProjectComponent from './components/project-component.vue'
import FooterComponent from './components/footer-component.vue'
import { ref, reactive, watch, nextTick } from 'vue';

const imageContext = require.context(
  '../public/assets/img/png',
  false,                       
  /\.png$/                     
);

const imageFilenames = imageContext.keys().map(key => key.slice(2));
const reverseCardList = ref([]);
const gameStart = ref(false);
const gameEnd = ref(false);
const gameLv = ref(0);

const shuffleArray = (array) => {
  const shuffled = array.slice();
  for (let i = shuffled.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [shuffled[i], shuffled[j]] = [shuffled[j], shuffled[i]];
  }
  return shuffled;
};

const cardsList = () => {
  const shuffledFilenames = shuffleArray(imageFilenames);
  const duplicatedImages = shuffledFilenames.flatMap((filename) => ([
    {
      image: imageContext(`./${filename}`),
      reverse: false,
      matched: false,
    },
    {
      image: imageContext(`./${filename}`),
      reverse: false,
      matched: false,
    }
  ]));
  
  if(gameLv.value === 0){
    return duplicatedImages.slice(0, 12);
  }

  return duplicatedImages
}

const cards = reactive(
  cardsList()
);

const shuffleCard = (array) => {
  for (let i = array.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [array[i], array[j]] = [array[j], array[i]];
  }
};

shuffleCard(cards);

const cardClick = (index) => {
  if(!gameStart.value){
    alert('게임 시작을 눌러주세요.');
    return
  }

  if (reverseCardList.value.length < 2) {
    const card = cards[index];

    if (!card.reverse && !card.matched) {
      card.reverse = true;
      reverseCardList.value.push(card);

      if (reverseCardList.value.length === 2) {
        checkMatchingCards();
      }
    }
  }
};

const checkMatchingCards = () => {
  const [card1, card2] = reverseCardList.value;

  if (card1.image === card2.image) {
    card1.matched = true;
    card2.matched = true;
  }

  setTimeout(() => {
    noSameCard();
  }, 500);
};

const noSameCard = () => {
  reverseCardList.value.forEach((card) => {
    card.reverse = false;
  });
  reverseCardList.value = [];
};

const resetCards = async () => {
  gameEnd.value = false;
  gameStart.value = false;

  cards.forEach((card)=>{
    card.reverse = false;
    card.matched = false;
  })

  const newCards = cardsList();
  cards.splice(0, cards.length, ...newCards);
  shuffleCard(cards);
  
  setTimeout(() => {
    gameStartClick();
  }, 1000);
};

const gameStartClick = async () => {
  if(gameStart.value){
    return
  }

  cards.forEach((card,index)=>{
    setTimeout(function() {
      card.reverse = true;
    }, 1000 + 100 * index);
  })

  setTimeout(() => {
    cards.forEach((card) => {
      if (!card.matched) {
        card.reverse = false;
      }
    });
  }, 3000);

  gameStart.value = true;
}

watch(cards, () => {
  const matchedCards = cards.filter((card) => card.matched);

  if (matchedCards.length === cards.length && !gameEnd.value) {
    gameEnd.value = true;
    setTimeout(() => {
      cards.forEach((card,index)=>{
        setTimeout(function() {
          card.reverse = false;
          card.matched = false;
        }, 1000 + 100 * index);
      });

      alert('카드 게임 -완-');

      nextTick(() => {
        resetCards();
      })
    }, 500);
  }
});
</script>

<style scoped>
.game {
  width: 100vw;
  height: 80vh;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.cards {
  width: 50rem;
  height: 50rem;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  align-content: center;
  padding-left: 10px;
}

.card {
  display: inline-block;
  margin-right: 10px;
  margin-bottom: 10px;
  width: 90px;
  height: 130px;
}

@media (min-width: 300px)
{
    .card {
      width: 60px;
      height: 100px;
    }
}

@media (min-width: 360px)
{
    .card {
      width: 75px;
      height: 115px;
    }
}

@media (min-width: 420px)
{
    .card {
      width: 90px;
      height: 130px;
    }
}

@media (min-width: 500px)
{
    .card {
      width: 110px;
      height: 150px;
    }

    
}

@media (min-width: 550px)
{
    .card {
      width: 120px;
      height: 160px;
    }
}

@media (min-width: 650px)
{
    .card {
      width: 130px;
      height: 170px;
    }
}

@media (min-width: 700px)
{
    .card {
      width: 150px;
      height: 190px;
    }
}

@media(min-width:800px) {
    .card {
      width: 180px;
      height: 220px;
    }
}

.card-info {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}

.card.reverse .card-info {
  transform: rotateY(180deg);
}

.card-front {
  background-size: cover;
  background-position:center;
  background-image: url('../public/assets/img/gameFront.png');
  cursor: pointer;
}

.card-front,
.card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
}

.card-back {
  transform: rotateY(180deg);
}
.card-back img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.matched .card-info {
  transform: rotateY(180deg);
}
/* 
.buttonCss {
  position: absolute;
  bottom: 3rem;
  left: 50%;
  transform: translate(-50%);
  padding: 0.5rem 1rem;
  background: #fd8a69;
  color: #f1efed;
  border-radius: 5px;
} */

.button-container {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
