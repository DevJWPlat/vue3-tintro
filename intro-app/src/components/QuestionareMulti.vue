<template>
    <div class="question-box" :class="currentSlideColour">
        <h1>{{ currentTitle }}</h1>
        <div v-if="currentIndex < slides.length - 1">
            <input v-model="userAnswers[currentIndex]" type="text" placeholder="Your Answer"/>
        </div>
        <button @click="changeSlideColour">{{ currentButtonText }}</button>
    </div>
    <div class="overlay" v-if="showOverlay">
        <div class="overlay-content">
            <h2>Quiz Completed!</h2>
            <p>Thank you for participating in the quiz.</p>
            <div class="answers" v-if="userAnswers.length">
                <h3>Your Answers:</h3>
                <ul>
                    <li v-for="(answer, index) in userAnswers" :key="index">
                        <strong>Question {{ index + 1 }}:</strong> {{ answer || "No answer provided" }}
                    </li>
                </ul>
            </div>
            <button @click="closeOverlay">Restart Quiz</button>
        </div>
    </div>
        
</template>

<script>
export default {
  name: 'QuestionareMulti',
  props: {
    title: {
      type: String,
      default: 'Question', 
    },
    questionSlideColour: {
      type: String,
      default: 'black', 
    },
    buttonText: {
      type: String,
      default: 'Begin Quiz', 
    },
  },
  data () {
    return {
      currentSlideColour: this.questionSlideColour,
      currentTitle: this.title,
      currentButtonText: this.buttonText,
      slides: [
        { colour: 'black', title: 'Question One', button: 'Next Question' },
        { colour: 'pink', title: 'Question Two', button: 'Next Question' },
        { colour: 'teal', title: 'Question Three', button: 'Final Question' },
        { colour: 'purple', title: 'Question Four', button: 'End Quiz' },
        { colour: 'green', title: 'Well Done You Did It!!', button: 'Finish' },
      ], 
      currentIndex: 0, 
      showOverlay: false,
      userAnswers: [],
    };
  },
  methods: {
    changeSlideColour () {
      if (this.currentIndex === this.slides.length - 1) {
        this.showOverlay = true;
      } else {
        this.currentIndex = (this.currentIndex + 1) % this.slides.length;
        const currentSlide = this.slides[this.currentIndex];
        this.currentSlideColour = currentSlide.colour;
        this.currentTitle = currentSlide.title;
        this.currentButtonText = currentSlide.button;
      }
    },
    closeOverlay () {
      this.showOverlay = false;
      this.currentIndex = 0;
      const currentSlide = this.slides[this.currentIndex];
      this.currentSlideColour = currentSlide.colour;
      this.currentTitle = currentSlide.title;
      this.currentButtonText = currentSlide.button;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .question-box {
        display: flex;
        flex-direction: column;
        margin: 100px auto 50px auto;
        width: 100vh;
        padding: 100px;
    }
    .black {
        background: black;
        color: white;
        button {
            color: #fff;
            background: transparent;
            border: 2px solid #fff;
            transition: .3s ease;
            &:hover {
                background: #fff;
                color: black;
            }
        }
        input {
            color: #fff;
            background: transparent;
            border: 2px solid #fff;
        }
    }
    .pink {
        background: pink;
        color: black;
        button {
            color: #000;
            background: transparent;
            border: 2px solid #000;
            transition: .3s ease;
            &:hover {
                background: #000;
                color: pink;
            }
        }
        input {
            color: #000;
            background: transparent;
            border: 2px solid #000;
        }
    }
    .teal {
        background: teal;
        color: white;
        button {
            color: #fff;
            background: transparent;
            border: 2px solid #fff;
            transition: .3s ease;
            &:hover {
                background: #fff;
                color: teal;
            }
        }
        input {
            color: #fff;
            background: transparent;
            border: 2px solid #fff;
        }
    }
    .purple {
        background: purple;
        color: white;
        button {
            color: #fff;
            background: transparent;
            border: 2px solid #fff;
            transition: .3s ease;
            &:hover {
                background: #fff;
                color: purple;
            }
        }
        input {
            color: #fff;
            background: transparent;
            border: 2px solid #fff;
        }
    }
    .green {
        background: green;
        color: white;
        button {
            color: #fff;
            background: transparent;
            border: 2px solid #fff;
            transition: .3s ease;
            &:hover {
                background: #fff;
                color: green;
            }
        }
        input {
            color: #fff;
            background: transparent;
            border: 2px solid #fff;
        }
        
    }
    button {
        cursor: pointer;
        padding: 5px 20px;
        margin: 50px auto 0;
        font-size: 18px;
        max-width: max-content;
    }
    input {
        padding: 5px 20px;
        margin: 50px auto 0;
        font-size: 18px;
        max-width: 50%;
    }
    .overlay-content {
        position: fixed;
        width: 100%;
        height: 100vh;
        top: 8%;
        background: coral;
        padding: 300px 0 0;
        color: black;
        h2 {
            font-size: 32px;
        }
        button {
            cursor: pointer;
            padding: 5px 20px;
            margin-top: 50px;
            font-size: 18px;
            color: black;
            background: transparent;
            border: 2px solid black;
            transition: .3s ease;
            &:hover {
                background: black;
                color: coral;
            }
        }
    }
    .answers {
        margin-top: 20px;
        ul {
            padding: 0;
            li {
                list-style: none;
            }
        }
    }
</style>
