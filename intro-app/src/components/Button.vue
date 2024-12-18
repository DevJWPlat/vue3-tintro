<template>
    <a
        :class="['base-button', colorClass, sizeClass, widthClass, borderRadiusClass]"
        :href="href"
        :target="target"
    >
        <slot>{{ label }}</slot>
        <i v-if="icon" :class="['base-button--icon', icon]"></i>
    </a>
  </template>
  
  <script>
  export default {
    name: "BaseButton",
    props: {
        color: {
            type: String,
            default: "blue",
        },
        size: {
            type: String,
            default: "small", 
        },
        label: {
            type: String,
            default: "",
        },
        width: {
            type: String,
            default: "full", 
        },
        borderRadius: {
            type: String,
            default: "normal", 
        },
        href: {
            type: String,
            default: "#",
        },
        target: {
            type: String,
            default: "_self", 
        },
        icon: {
            type: String,
            default: "", 
        },
    },
    computed: {
      colorClass() {
        return `base-button--${this.color}`;
      },
      sizeClass() {
        return `base-button--${this.size}`;
      },
      widthClass() {
        return `base-button--${this.width}`;
      },
      widthClass() {
        return `base-button--${this.borderRadius}`;
      },
    },
  };
  </script>
  
  <style lang="scss">
  .base-button {
    border: none;
    border-radius: 4px;
    padding: 16px;
    font-size: 16px;
    cursor: pointer;
    text-decoration: none;
    display: inline-block;
  
    &--blue {
        background: blue;
        color: white;
        transition: ease .3s;
        &:hover {
            background: darkblue;
        }
    }
    &--red {
        background: red;
        color: white;
        transition: ease .3s;
        &:hover {
            background: darkred;
        }
    }
    &--green {
        background: green;
        color: white;
        transition: ease .3s;
        &:hover {
            background: darkgreen;
        }
    }
    &--white {
        background: white;
        color: black;
        transition: ease .3s;
        border: 1px solid black;
        i {
            color: aqua;
        }
        &:hover {
            background: black;
            color: white;
        }
    }
    &--black {
        background: black;
        color: white;
        transition: ease .3s;
        border: 1px solid transparent;
        &:hover {
            background: white;
            color: black;
            border: 1px solid black;
        }
    }
    &--small {
        padding: 8px 16px;
        font-size: 14px;
    }
    &--medium {
        padding: 12px 24px;
        font-size: 16px;
    }
    &--large {
        padding: 16px 32px;
        font-size: 18px;
    }
    &--extralarge {
        padding: 20px 40px;
        font-size: 20px;
    }
    &--full {
        width: 100%;
    }
    &--max-content {
        width: max-content;
    }
    &--min-content {
        width: min-content;
    }
    &--normal {
        border-radius: 12px;
    }
    &--pill {
        border-radius: 9999px;
    }
    &--small {
        border-radius: 4px;
    }
    &--large {
        border-radius: 16px;
    }
    &--icon {
        margin-left: 12px; /* Space between icon and text */
        font-size: 14px;
      }
  }
  </style>
  