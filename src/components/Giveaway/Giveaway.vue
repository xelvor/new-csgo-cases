<script>
import { ref } from 'vue';

const circles = ref(['1', '2', '3', '4', '5', '6', '7', '8', '9', '10', '11', '12', '13', '14', '15', '16', '17', '18'])

const giveaways = ref([
  {
    award: "USP-S | Cyrex",
    state: "Minimal Wear",
    end: 1714350233 - 10000,
    image: "https://steamcommunity-a.akamaihd.net/economy/image/-9a81dlWLwJ2UUGcVs_nsVtzdOEdtWwKGZZLQHTxDZ7I56KU0Zwwo4NUX4oFJZEHLbXH5ApeO4YmlhxYQknCRvCo04DEVlxkKgpoo6m1FBRp3_bGcjhQ09-jq5WYh8j3KqnUjlRd4cJ5nqfErduj3VK3_0tlZzyiLNPHd1BtNQnVqAe2xOy-jJC675XLnHpr63Yq-z-DyATLGvGU",
    price: "10.08zł",
    circles: [],
    lastWinner: {
      nick: "chwyto",
      avatar: "https://media1.tenor.com/m/TChTx3WOUBYAAAAd/playboi-carti-playboi-carti-cute.gif"
    }
  },
  {
    award: "M4A1-S | Nightmare",
    state: "Minimal Wear",
    end: 1714350233,
    image: "https://steamcommunity-a.akamaihd.net/economy/image/-9a81dlWLwJ2UUGcVs_nsVtzdOEdtWwKGZZLQHTxDZ7I56KU0Zwwo4NUX4oFJZEHLbXH5ApeO4YmlhxYQknCRvCo04DEVlxkKgpou-6kejhz2v_Nfz5H_uO1gb-Gw_alIITfn2xZ_MhwmOz--YXygED6rkFvaj37INXEdwI-YlmD-gK9l-u815C7vs-fziQ1uiQgtHnfmBCx0AYMMLI3JBWfRQ",
    price: "114.16zł",
    circles: [],
    lastWinner: {
      nick: "IQ",
      avatar: "https://cdn.discordapp.com/attachments/1027275122626797630/1233853198033354813/3e3a034404c711ef93981b18f44c25fd.png?ex=662e9ad6&is=662d4956&hm=d58a5f701af98b6caa9aeb6969f5519084873260c96cef3341650ee25fb78183&"
    }
  }
])

giveaways.value.forEach(giveaway => {
    const remainingTimeInSeconds = giveaway.end - Math.floor(Date.now() / 1000);
    const maxCircles = 18;
    const remainingCircles = Math.ceil((remainingTimeInSeconds / 86400) * maxCircles);
    const circles = Array.from({ length: maxCircles }, (_, i) => i + 1);
    giveaway.circles = circles.slice(0, remainingCircles);
})

setInterval(() => {
  giveaways.value.forEach(giveaway => {
    const now = Math.floor(Date.now() / 1000);
    const remainingTime = giveaway.end - now;

    const days = Math.floor(remainingTime / 86400);
    const hours = Math.floor((remainingTime % 86400) / 3600);
    const minutes = Math.floor((remainingTime % 3600) / 60);
    const seconds = remainingTime % 60;

    let text = ''
    if (days > 0) text += `${days}d `;
    if (hours > 0) text += `${hours} godz. `;
    if (minutes > 0) text += `${minutes} min. `;
    text += `${seconds} sek.`;

    giveaway.remainingTime = text;
  })
}, 1000);

export default {
  setup() {
    return {
      giveaways,
      circles
    }
}
}
</script>

<template>
    <div class="giveaways">
    <div v-for="giveaway in giveaways" :key="giveaway.id" class="giveaway">
      <div class="giveaway-info">
        <span class="giveaway-award">{{ giveaway.award }}</span>
        <span class="giveaway-state">{{ giveaway.state }}</span>
        <div class="giveaway-bottom">
            <span class="giveaway-time">{{ giveaway.remainingTime }}</span>
            <div class="giveaway-circles">
                <div v-for="circle in circles" :key="circle" class="giveaway-circle"></div>
                <div class="circle-active">
                    <div v-for="circle in giveaway.circles" :key="circle" class="giveaway-circle-active"></div>
                </div>
            </div>
            <div class="giveaway-image">
                <img :src="giveaway.image" alt="giveaway-img">
            </div>
        </div>
        <div class="giveaway-under">
          <button class="giveaway-join">Dołącz</button>
          <div class="giveaway-last-winner">
            <span class="last-winner-nick">Ostatni zwycięzca: {{ giveaway.lastWinner.nick }}</span>
            <img class="last-winner-avatar" :src="giveaway.lastWinner.avatar" alt="giveaway-winner">
          </div>
        </div>
      </div>
      <div class="giveaway-price">{{ giveaway.price }}</div>
    </div>
    </div>
</template>

<style>
  .giveaways {
    display: flex;
    margin: 20px;
    width: 97.5%;
    height: 190px;
    margin-right: 15px;
    flex-direction: row;
    gap: 20px;
  }

  .giveaway {
    background: linear-gradient(rgba(136,71,255,.15),rgba(136,71,255,.15)),linear-gradient(rgba(8,27,58,.7),rgba(8,27,58,.7));
    width: 100%;
    height: 100%;
    border-radius: 10px;
    display: inline-flex;
    justify-content: flex-start;
    align-items: center;
    padding: 20px;
  }

  .giveaway-info {
    display: flex;
    flex-direction: column;
  }

  .giveaway-award {
    color: white;
    font-size: 18px;
    font-weight: bold;
    margin-left: 15px;
  } 

  .giveaway-state {
    color: rgb(255, 255, 255, 0.3);
    font-size: 14px;
    margin-left: 15px;
  }

  .giveaway-time {
    color: white;
    font-size: 14px;
    margin-left: 15px;
    width: 12rem;
    margin-top: 15px;
  }

  .giveaway-join {
    background: transparent;
    border-radius: 7px;
    border: 1px solid rgb(136,71,255, 0.3);
    cursor: pointer;
    width: 100px;
    height: 43px;
    margin-left: 15px;
    margin-top: 20px;
    font-weight: 700;
    font-size: 14px;
    color: rgb(255, 255, 255, 0.5);

    transition: all 0.3s;
  }

  .giveaway-join:hover {
    background: rgb(136,71,255, 0.3);
    border: 1px solid rgb(136,71,255);
    color: white;
  }

    .giveaway-bottom {
        display: inline-flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }

    .giveaway-circles {
        display: inline-flex;
        flex-direction: row;
        gap: 5px;
        margin-left: 15px;
        margin-top: 10px;
        position: relative;
    }

    .giveaway-circle {
        width: 7px;
        height: 7px;
        border-radius: 50%;
        background: #3B3465;
    }

    .giveaway-circle-active {
        background: #B029C9;
        width: 7px;
        height: 7px;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: row;
    }

    .circle-active {
        display: inline-flex;
        flex-direction: row;
        gap: 5px;
        position: absolute;
        top: 0;
        left: 0;
    }

    .circle-active::before {
        content: '';
        width: 7px;
        height: 7px;
        border-radius: 50%;
        background: #B029C9;
    }

    .giveaway-img {
        position: absolute;
        display: inline-flex;
        justify-content: flex-end;
        align-items: center;
        margin-left: 100px;
        width: 70%;
        height: 70%;
        scale: 0.5;
    }

    .giveaway-image {
        background-image: url(https://csgo-skins.com/images/giveaways/background.svg);
        background-position: 50%;
        background-repeat: no-repeat;
        width: 169px;
        position: absolute;
        margin-left: 700px;
    }

    .giveaway-image img {
        scale: 0.6;
        margin-left: -15px;
    }

    .giveaway-under {
        display: inline-flex;
        flex-direction: row;
        justify-content: flex-start;
        align-items: center;
    }

    .last-winner-nick {
        color: white;
        font-size: 14px;
        margin-left: 15px;
    }

    .last-winner-avatar {
        width: 30px;
        height: 30px;
        border-radius: 10px;
        margin-right: 15px;
        background-color: black;
    }

    .giveaway-last-winner {
        display: inline-flex;
        flex-direction: row;
        align-items: center;
        gap: 10px;
        margin-top: 20px;
        margin-left: 15px;
    }

    .giveaway-price {
      display: flex;
      justify-content: flex-end;
      align-items: center;
      color: white;
      font-weight: bold;
    }
</style>