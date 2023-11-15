<template>
    <div id="accordion-" class="accordion">
      <div class="accordion-header" @click="toggleAccordion">
        <div class="accordion-icon" :class="{ 'open': isOpen }" :style="{ transform: rotateTransform }">
          <span class="plus">+</span>
        </div>
        <div class="accordion-title">{{ title }}</div>
      </div>
      <transition name="accordion-transition">
        <div class="accordion-content" v-show="isOpen">
          <div class="flex-container">
            <div></div>
            <div class="accordion-text flex-text" :class="{ 'fade-in': isOpen, 'fade-out': !isOpen }">
                <slot></slot>
            </div>
          </div>
          
          <br>
            <div style="font-size: 12px; font-style: italic;"><div class="source">Source: 
              
            </div>
        </div>
    </div>
      </transition>
    </div>
  </template>
  
  <script>

  export default {
    props: {
        title: {
            type: String,
            required: true
        }
    },
    data() {
      return {
        isOpen: false,
        switchState: false
      };
    },
    computed: {
      rotateTransform() {
        return this.isOpen ? 'rotate(45deg)' : 'rotate(0)';
      },
    },
    mounted() {

      console.log('accordion')
    },
    methods: {
      toggleAccordion() {
        this.isOpen = !this.isOpen;
      }
    }
  };
  </script>
  
  <style>
  .flex-container {
    display: flex;
    flex-wrap: wrap;
  }

  /* create flex class that does not grow */


  .flex-icon {
    flex: 0 1 100px;
  }

  .flex-text {
    flex: 1 1 70%;
  }

  .accordion {
    margin-top: 10px;
    margin-bottom: 30px;
    border-bottom: 0.5px solid #475026;
  }
  
  .accordion-header {
    display: flex;
    align-items: center;
    cursor: pointer;
  }
  
  .accordion-icon {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 24px;
    height: 24px;
    margin-right: 10px;
    transition: transform 0.6s;
  }
  
  .accordion-icon.open {
    transform: rotate(45deg);
  }
  
  .plus {
    font-size: 32px;
    font-weight: normal;
  }
  
  .accordion-title {
    font-weight: bold;
  }
  
  .accordion-content {
    margin-top: 10px;
    overflow: hidden;
  }
  
  .accordion-text {
    padding: 10px;
    border-bottom: 1px solid #475026;
    opacity: 0;
    transition: opacity 0.5s;
  }
  
  .fade-in {
    opacity: 1;
  }
  
  .fade-out {
    opacity: 0;
  }
  
  .accordion-transition-enter-active,
  .accordion-transition-leave-active {
    transition: height 0.5s, opacity 0.5s;
  }
  
  .accordion-transition-enter,
  .accordion-transition-leave-to {
    height: 0;
    overflow: hidden;
  }
  </style>
  