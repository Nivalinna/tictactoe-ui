<template>
    <div class="game-container">
        <game-score-board v-model="score" />
        <game-grid ref="gameGrid" @winner="updateScore" />
        <button class="button" @click="playAgain">Play again</button>
    </div>
</template>
<style scoped>
    .game-container {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    
    }
    .button {
        background-color: #555555; 
        color: white;
        padding: 15px 32px;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        align-items: center;
        justify-content: center;
    }
</style>
<script>

import GameScoreBoard from './GameScoreBoard'
import GameGrid from './GameGrid'

export default {
    name: 'GameView',

    components: {
        GameScoreBoard,
        GameGrid,
    },

    data: () => ({
        score: {
            O: 0,
            X: 0,
        }
    }),

    methods: {
        updateScore(winner) {
            this.score[winner] = this.score[winner] + 1
            alert('fag')
            window.variable = ('yeet'),
            window.variable.push['x']
        },

        playAgain() {
            this.$refs.gameGrid.resetGame()
        }
    }
}
</script>