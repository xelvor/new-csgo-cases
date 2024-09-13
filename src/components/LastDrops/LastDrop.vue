<script>
const lastDrops = [
  {
    name: "HOWL",
    time: "9 godzin temu",
    user: "IQ65",
    userAvatar: "https://cdn.discordapp.com/attachments/1027275122626797630/1233853198033354813/3e3a034404c711ef93981b18f44c25fd.png?ex=662e9ad6&is=662d4956&hm=d58a5f701af98b6caa9aeb6969f5519084873260c96cef3341650ee25fb78183&",
    image: "https://steamcommunity-a.akamaihd.net/economy/image/-9a81dlWLwJ2UUGcVs_nsVtzdOEdtWwKGZZLQHTxDZ7I56KU0Zwwo4NUX4oFJZEHLbXH5ApeO4YmlhxYQknCRvCo04DEVlxkKgpou-6kejhjxszFJTwT09S5g4yCmfDLP7LWnn8f6pIl2-yYp9SnjA23-BBuNW-iLI-XJgFsZQyG_VW2lOq918e8uszLn2wj5HeAvkVdtQ",
    rarity: "gold"
  },
  {
    name: "HOWL",
    time: "10 godzin temu",
    user: "IQ65",
    userAvatar: "https://cdn.discordapp.com/attachments/1027275122626797630/1233853198033354813/3e3a034404c711ef93981b18f44c25fd.png?ex=662e9ad6&is=662d4956&hm=d58a5f701af98b6caa9aeb6969f5519084873260c96cef3341650ee25fb78183&",
    image: "https://steamcommunity-a.akamaihd.net/economy/image/-9a81dlWLwJ2UUGcVs_nsVtzdOEdtWwKGZZLQHTxDZ7I56KU0Zwwo4NUX4oFJZEHLbXH5ApeO4YmlhxYQknCRvCo04DEVlxkKgpou-6kejhjxszFJTwT09S5g4yCmfDLP7LWnn8f6pIl2-yYp9SnjA23-BBuNW-iLI-XJgFsZQyG_VW2lOq918e8uszLn2wj5HeAvkVdtQ",
    rarity: "gold"
  },
  {
    name: "HOWL",
    time: "10 godzin temu",
    user: "IQ65",
    userAvatar: "https://cdn.discordapp.com/attachments/1027275122626797630/1233853198033354813/3e3a034404c711ef93981b18f44c25fd.png?ex=662e9ad6&is=662d4956&hm=d58a5f701af98b6caa9aeb6969f5519084873260c96cef3341650ee25fb78183&",
    image: "https://steamcommunity-a.akamaihd.net/economy/image/-9a81dlWLwJ2UUGcVs_nsVtzdOEdtWwKGZZLQHTxDZ7I56KU0Zwwo4NUX4oFJZEHLbXH5ApeO4YmlhxYQknCRvCo04DEVlxkKgpou-6kejhjxszFJTwT09S5g4yCmfDLP7LWnn8f6pIl2-yYp9SnjA23-BBuNW-iLI-XJgFsZQyG_VW2lOq918e8uszLn2wj5HeAvkVdtQ",
    rarity: "gold"
  },
  {
    name: "DRAGON LORE",
    time: "12 godzin temu",
    user: "Chwyto",
    userAvatar: "https://media1.tenor.com/m/TChTx3WOUBYAAAAd/playboi-carti-playboi-carti-cute.gif",
    image: "https://steamcommunity-a.akamaihd.net/economy/image/-9a81dlWLwJ2UUGcVs_nsVtzdOEdtWwKGZZLQHTxDZ7I56KU0Zwwo4NUX4oFJZEHLbXH5ApeO4YmlhxYQknCRvCo04DEVlxkKgpot621FAR17P7NdTRH-t26q4SZlvD7PYTQgXtu5cB1g_zMu9Wk2ATh_0tkMWrzLY7BIQM2NArQq1O9kL_qgJTt6Ziam3Bh6SR3sHfD30vgriIWFx4",
    rarity: "red"
  },
  {
    name: "HEDGE MAZE",
    time: "15 godzin temu",
    user: "IQ65",
    userAvatar: "https://cdn.discordapp.com/attachments/1027275122626797630/1233853198033354813/3e3a034404c711ef93981b18f44c25fd.png?ex=662e9ad6&is=662d4956&hm=d58a5f701af98b6caa9aeb6969f5519084873260c96cef3341650ee25fb78183&",
    image: "https://steamcommunity-a.akamaihd.net/economy/image/-9a81dlWLwJ2UUGcVs_nsVtzdOEdtWwKGZZLQHTxDZ7I56KU0Zwwo4NUX4oFJZEHLbXH5ApeO4YmlhxYQknCRvCo04DAQ1JmMR1osbaqPQJz7ODYfi9W9eOxhoWOmcj5Nr_Yg2Yf6sYkie-UptWi0A3sqhdta2H0LNDEc1NsNV_W-Va-l73q1Ja96p6dz2wj5HevREuBKg",
    rarity: "red"
  },
  {
    name: "THE PRINCE",
    time: "16 godzin temu",
    user: "IQ65",
    userAvatar: "https://cdn.discordapp.com/attachments/1027275122626797630/1233853198033354813/3e3a034404c711ef93981b18f44c25fd.png?ex=662e9ad6&is=662d4956&hm=d58a5f701af98b6caa9aeb6969f5519084873260c96cef3341650ee25fb78183&",
    image: "https://steamcommunity-a.akamaihd.net/economy/image/-9a81dlWLwJ2UUGcVs_nsVtzdOEdtWwKGZZLQHTxDZ7I56KU0Zwwo4NUX4oFJZEHLbXH5ApeO4YmlhxYQknCRvCo04DEVlxkKgpot621FABz7PLfYQJH4t27kYy0mvLwOq7c2D4B7cQl3byS89um2Ffh_RE-Yzz3IYHDd1BoZ1yC_FLqyL2-gpa7u5jXiSw0eTyRlhg",
    rarity: "red"
  },
  {
    name: "HOWL",
    time: "9 godzin temu",
    user: "IQ65",
    userAvatar: "https://cdn.discordapp.com/attachments/1027275122626797630/1233853198033354813/3e3a034404c711ef93981b18f44c25fd.png?ex=662e9ad6&is=662d4956&hm=d58a5f701af98b6caa9aeb6969f5519084873260c96cef3341650ee25fb78183&",
    image: "https://steamcommunity-a.akamaihd.net/economy/image/-9a81dlWLwJ2UUGcVs_nsVtzdOEdtWwKGZZLQHTxDZ7I56KU0Zwwo4NUX4oFJZEHLbXH5ApeO4YmlhxYQknCRvCo04DEVlxkKgpou-6kejhjxszFJTwT09S5g4yCmfDLP7LWnn8f6pIl2-yYp9SnjA23-BBuNW-iLI-XJgFsZQyG_VW2lOq918e8uszLn2wj5HeAvkVdtQ",
    rarity: "gold"
  },
  {
    name: "HOWL",
    time: "10 godzin temu",
    user: "IQ65",
    userAvatar: "https://cdn.discordapp.com/attachments/1027275122626797630/1233853198033354813/3e3a034404c711ef93981b18f44c25fd.png?ex=662e9ad6&is=662d4956&hm=d58a5f701af98b6caa9aeb6969f5519084873260c96cef3341650ee25fb78183&",
    image: "https://steamcommunity-a.akamaihd.net/economy/image/-9a81dlWLwJ2UUGcVs_nsVtzdOEdtWwKGZZLQHTxDZ7I56KU0Zwwo4NUX4oFJZEHLbXH5ApeO4YmlhxYQknCRvCo04DEVlxkKgpou-6kejhjxszFJTwT09S5g4yCmfDLP7LWnn8f6pIl2-yYp9SnjA23-BBuNW-iLI-XJgFsZQyG_VW2lOq918e8uszLn2wj5HeAvkVdtQ",
    rarity: "gold"
  },
  {
    name: "HOWL",
    time: "10 godzin temu",
    user: "IQ65",
    userAvatar: "https://cdn.discordapp.com/attachments/1027275122626797630/1233853198033354813/3e3a034404c711ef93981b18f44c25fd.png?ex=662e9ad6&is=662d4956&hm=d58a5f701af98b6caa9aeb6969f5519084873260c96cef3341650ee25fb78183&",
    image: "https://steamcommunity-a.akamaihd.net/economy/image/-9a81dlWLwJ2UUGcVs_nsVtzdOEdtWwKGZZLQHTxDZ7I56KU0Zwwo4NUX4oFJZEHLbXH5ApeO4YmlhxYQknCRvCo04DEVlxkKgpou-6kejhjxszFJTwT09S5g4yCmfDLP7LWnn8f6pIl2-yYp9SnjA23-BBuNW-iLI-XJgFsZQyG_VW2lOq918e8uszLn2wj5HeAvkVdtQ",
    rarity: "gold"
  },
  {
    name: "DRAGON LORE",
    time: "12 godzin temu",
    user: "Chwyto",
    userAvatar: "https://media1.tenor.com/m/TChTx3WOUBYAAAAd/playboi-carti-playboi-carti-cute.gif",
    image: "https://steamcommunity-a.akamaihd.net/economy/image/-9a81dlWLwJ2UUGcVs_nsVtzdOEdtWwKGZZLQHTxDZ7I56KU0Zwwo4NUX4oFJZEHLbXH5ApeO4YmlhxYQknCRvCo04DEVlxkKgpot621FAR17P7NdTRH-t26q4SZlvD7PYTQgXtu5cB1g_zMu9Wk2ATh_0tkMWrzLY7BIQM2NArQq1O9kL_qgJTt6Ziam3Bh6SR3sHfD30vgriIWFx4",
    rarity: "red"
  },
  {
    name: "HEDGE MAZE",
    time: "15 godzin temu",
    user: "IQ65",
    userAvatar: "https://cdn.discordapp.com/attachments/1027275122626797630/1233853198033354813/3e3a034404c711ef93981b18f44c25fd.png?ex=662e9ad6&is=662d4956&hm=d58a5f701af98b6caa9aeb6969f5519084873260c96cef3341650ee25fb78183&",
    image: "https://steamcommunity-a.akamaihd.net/economy/image/-9a81dlWLwJ2UUGcVs_nsVtzdOEdtWwKGZZLQHTxDZ7I56KU0Zwwo4NUX4oFJZEHLbXH5ApeO4YmlhxYQknCRvCo04DAQ1JmMR1osbaqPQJz7ODYfi9W9eOxhoWOmcj5Nr_Yg2Yf6sYkie-UptWi0A3sqhdta2H0LNDEc1NsNV_W-Va-l73q1Ja96p6dz2wj5HevREuBKg",
    rarity: "red"
  },
  {
    name: "THE PRINCE",
    time: "16 godzin temu",
    user: "IQ65",
    userAvatar: "https://cdn.discordapp.com/attachments/1027275122626797630/1233853198033354813/3e3a034404c711ef93981b18f44c25fd.png?ex=662e9ad6&is=662d4956&hm=d58a5f701af98b6caa9aeb6969f5519084873260c96cef3341650ee25fb78183&",
    image: "https://steamcommunity-a.akamaihd.net/economy/image/-9a81dlWLwJ2UUGcVs_nsVtzdOEdtWwKGZZLQHTxDZ7I56KU0Zwwo4NUX4oFJZEHLbXH5ApeO4YmlhxYQknCRvCo04DEVlxkKgpot621FABz7PLfYQJH4t27kYy0mvLwOq7c2D4B7cQl3byS89um2Ffh_RE-Yzz3IYHDd1BoZ1yC_FLqyL2-gpa7u5jXiSw0eTyRlhg",
    rarity: "red"
  },
  {
    name: "HOWL",
    time: "9 godzin temu",
    user: "IQ65",
    userAvatar: "https://cdn.discordapp.com/attachments/1027275122626797630/1233853198033354813/3e3a034404c711ef93981b18f44c25fd.png?ex=662e9ad6&is=662d4956&hm=d58a5f701af98b6caa9aeb6969f5519084873260c96cef3341650ee25fb78183&",
    image: "https://steamcommunity-a.akamaihd.net/economy/image/-9a81dlWLwJ2UUGcVs_nsVtzdOEdtWwKGZZLQHTxDZ7I56KU0Zwwo4NUX4oFJZEHLbXH5ApeO4YmlhxYQknCRvCo04DEVlxkKgpou-6kejhjxszFJTwT09S5g4yCmfDLP7LWnn8f6pIl2-yYp9SnjA23-BBuNW-iLI-XJgFsZQyG_VW2lOq918e8uszLn2wj5HeAvkVdtQ",
    rarity: "gold"
  },
  {
    name: "HOWL",
    time: "9 godzin temu",
    user: "IQ65",
    userAvatar: "https://cdn.discordapp.com/attachments/1027275122626797630/1233853198033354813/3e3a034404c711ef93981b18f44c25fd.png?ex=662e9ad6&is=662d4956&hm=d58a5f701af98b6caa9aeb6969f5519084873260c96cef3341650ee25fb78183&",
    image: "https://steamcommunity-a.akamaihd.net/economy/image/-9a81dlWLwJ2UUGcVs_nsVtzdOEdtWwKGZZLQHTxDZ7I56KU0Zwwo4NUX4oFJZEHLbXH5ApeO4YmlhxYQknCRvCo04DEVlxkKgpou-6kejhjxszFJTwT09S5g4yCmfDLP7LWnn8f6pIl2-yYp9SnjA23-BBuNW-iLI-XJgFsZQyG_VW2lOq918e8uszLn2wj5HeAvkVdtQ",
    rarity: "gold"
  }
]


const sorts = [
  {
    icon: '<svg aria-hidden="true" focusable="false" data-prefix="far" data-icon="clock" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path fill="#ffffff" d="M464 256A208 208 0 1 1 48 256a208 208 0 1 1 416 0zM0 256a256 256 0 1 0 512 0A256 256 0 1 0 0 256zM232 120V256c0 8 4 15.5 10.7 20l96 64c11 7.4 25.9 4.4 33.3-6.7s4.4-25.9-6.7-33.3L280 243.2V120c0-13.3-10.7-24-24-24s-24 10.7-24 24z" class=""></path></svg>',
    type: 'time',
    active: true
  },
  {
    icon: '<svg aria-hidden="true" focusable="false" data-prefix="far" data-icon="thumbs-up" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path fill="#ffffff" d="M323.8 34.8c-38.2-10.9-78.1 11.2-89 49.4l-5.7 20c-3.7 13-10.4 25-19.5 35l-51.3 56.4c-8.9 9.8-8.2 25 1.6 33.9s25 8.2 33.9-1.6l51.3-56.4c14.1-15.5 24.4-34 30.1-54.1l5.7-20c3.6-12.7 16.9-20.1 29.7-16.5s20.1 16.9 16.5 29.7l-5.7 20c-5.7 19.9-14.7 38.7-26.6 55.5c-5.2 7.3-5.8 16.9-1.7 24.9s12.3 13 21.3 13L448 224c8.8 0 16 7.2 16 16c0 6.8-4.3 12.7-10.4 15c-7.4 2.8-13 9-14.9 16.7s.1 15.8 5.3 21.7c2.5 2.8 4 6.5 4 10.6c0 7.8-5.6 14.3-13 15.7c-8.2 1.6-15.1 7.3-18 15.2s-1.6 16.7 3.6 23.3c2.1 2.7 3.4 6.1 3.4 9.9c0 6.7-4.2 12.6-10.2 14.9c-11.5 4.5-17.7 16.9-14.4 28.8c.4 1.3 .6 2.8 .6 4.3c0 8.8-7.2 16-16 16H286.5c-12.6 0-25-3.7-35.5-10.7l-61.7-41.1c-11-7.4-25.9-4.4-33.3 6.7s-4.4 25.9 6.7 33.3l61.7 41.1c18.4 12.3 40 18.8 62.1 18.8H384c34.7 0 62.9-27.6 64-62c14.6-11.7 24-29.7 24-50c0-4.5-.5-8.8-1.3-13c15.4-11.7 25.3-30.2 25.3-51c0-6.5-1-12.8-2.8-18.7C504.8 273.7 512 257.7 512 240c0-35.3-28.6-64-64-64l-92.3 0c4.7-10.4 8.7-21.2 11.8-32.2l5.7-20c10.9-38.2-11.2-78.1-49.4-89zM32 192c-17.7 0-32 14.3-32 32V448c0 17.7 14.3 32 32 32H96c17.7 0 32-14.3 32-32V224c0-17.7-14.3-32-32-32H32z" class=""></path></svg>',
    type: 'likes'
  },
  {
    icon: '<svg  aria-hidden="true" focusable="false" data-prefix="far" data-icon="star" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512"><path fill="#ffffff" d="M287.9 0c9.2 0 17.6 5.2 21.6 13.5l68.6 141.3 153.2 22.6c9 1.3 16.5 7.6 19.3 16.3s.5 18.1-5.9 24.5L433.6 328.4l26.2 155.6c1.5 9-2.2 18.1-9.7 23.5s-17.3 6-25.3 1.7l-137-73.2L151 509.1c-8.1 4.3-17.9 3.7-25.3-1.7s-11.2-14.5-9.7-23.5l26.2-155.6L31.1 218.2c-6.5-6.4-8.7-15.9-5.9-24.5s10.3-14.9 19.3-16.3l153.2-22.6L266.3 13.5C270.4 5.2 278.7 0 287.9 0zm0 79L235.4 187.2c-3.5 7.1-10.2 12.1-18.1 13.3L99 217.9 184.9 303c5.5 5.5 8.1 13.3 6.8 21L171.4 443.7l105.2-56.2c7.1-3.8 15.6-3.8 22.6 0l105.2 56.2L384.2 324.1c-1.3-7.7 1.2-15.5 6.8-21l85.9-85.1L358.6 200.5c-7.8-1.2-14.6-6.1-18.1-13.3L287.9 79z" class=""></path></svg>',
    type: 'best'
  }
]

const classes = {
  gold: {
    background: 'linear-gradient(0deg,rgba(228,174,57,.35) 0,transparent 200%),linear-gradient(0deg,rgba(8,27,58,.7) 0,rgba(8,27,58,.7) 100%)'
  },
  red: {
    background: 'linear-gradient(0deg,rgba(235,75,75,.35) 0,transparent 200%),linear-gradient(0deg,rgba(8,27,58,.7) 0,rgba(8,27,58,.7) 100%)'
  }
}

export default {
  data() {
    return {
      lastDrops,
      sorts,
      classes
    }
  }
}
</script>

<template>
  <div class="last-drops">
    <div class="left-sort">
      <button v-for="sort in sorts" :key="sort.id" class="sort-item" :class="{ 'active': sort.active }">
        <div v-html="sort.icon"></div>
      </button>
    </div>
    <div class="sort-container">
      <div v-for="drop in lastDrops" :key="drop.id" class="drop" :style="{ background: classes[drop.rarity].background }">
        <div class="user-info">
          <img class="header-avatar" :src="drop.userAvatar" alt="">
          <span class="user-name">{{ drop.user }}</span>
        </div>
        <img class="drop-image" :src="drop.image" alt="">
        <div class="drop-info">
          <span class="drop-name">{{ drop.name }}</span>
          <span class="drop-time">{{ drop.time }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
  .left-sort {
    display: flex;
    flex-direction: column;
    width: 36px;
    height: 36px;
  }

  .sort-item {
    background-color: #071329;
    border: none;
    cursor: pointer;
    padding: 10px;
    width: 36px;
    height: 36px;
    opacity: 0.5;

    transition: all 0.3s;
  }

  .sort-item.active {
    background-color: #071329;
    opacity: 1;
  }

  .sort-item:hover {
    background-color: #071329;
    opacity: 1;
  }

  .sort-item:active {
    background-color: #071329;
    opacity: 1;
  }

  .button_icon {
    width: 20px;
    height: 20px;
  }

  .last-drops {
    display: flex;
    margin: 20px;
    width: 100%;
    height: 100%;
    margin-right: 15px;
  }

  .sort-container {
    width: 95%;
    height: 107px;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    gap: 7px;
    margin-left: 10px;
  }

  .drop {
    width: 132px;
    height: 107px;
    background: rgba(228,174,57);
    border-radius: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    cursor: pointer;

    transition: all 0.3s;
  }

  .drop-image {
    width: 80px;
    height: 60px;
    margin-left: 5px;
    margin-bottom: 10px;

    transition: all 0.3s;
  }

  .drop-info {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 5px;
    gap: 2px;

    transition: all 0.3s;
  }

  .drop-name {
    color: white;
    font-size: 10px;
    font-weight: bold;
    max-width: 80px;
  }

  .drop-time {
    color: rgb(255, 255, 255, 0.4);
    font-size: 9px;
  }

  .drop:hover .drop-info {
    filter: blur(5px);
  }
  
  .drop:hover .drop-image {
    filter: blur(5px);
  }

  .user-info {
    display: flex;
    position: absolute;
    z-index: 99999;
    visibility: hidden;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    opacity: 0;

    transition: all 0.3s;
  }

  .drop:hover .user-info {
    visibility: visible;
    opacity: 1;
  }

  .user-name {
    color: white;
    font-size: 10px;
    font-weight: bold;
    margin-top: 5px;
  }
</style>