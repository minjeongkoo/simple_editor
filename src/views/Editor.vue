<template>
  <div class="editor">


    <!-- Text Area -->
    <div class="text-area">

      <!-- Section Controll -->
      <div class="top-section-control">
        <div>

          <span>Document's Align </span>
          <button v-on:click="documentAlignSet('left')"><img alt="text-align-left" src="../assets/ico/format_align_left_black_24dp.svg"/></button>
          <button v-on:click="documentAlignSet('center')"><img alt="text-align-center" src="../assets/ico/format_align_center_black_24dp.svg"/></button>
          <button v-on:click="documentAlignSet('right')"><img alt="text-align-right" src="../assets/ico/format_align_right_black_24dp.svg"/></button>
        </div>
      </div>

      <!-- Componant Box -->
      <div class="bottom-section-control">
        <div>
          <span>Componants </span>
          <button>HeadLine 1</button>
          <button>HeadLine 2</button>
          <button>HeadLine 3</button>
          <button>Caption</button>
          <button>Body</button>
        </div>
      </div>

      <article class="control-document-align" v-bind:class=" {'set-left' : set.documentAlign.left, 'set-center' : set.documentAlign.right, 'set-right': set.documentAlign.right} " >

        <div class="text-componant" onmouseover="">
          <button class="more-option"><img src="../assets/ico/more_vert_black_24dp.svg"/></button>
          <textarea rows="1">Headline</textarea>
        </div>

      </article>

    </div>

  </div>
</template>

<script>

export default {
  data () {
    return {
      set: {
        documentAlign: {
          left: true,
          center: false,
          right: false
        }
      }
    }
  },
  components: {

  },
  methods: {
    documentAlignSet (align) {
      this.set.documentAlign.left = false;
      this.set.documentAlign.center = false;
      this.set.documentAlign.right = false;

      switch (align) {
        case 'left':
          this.set.documentAlign.left = true;
          break;
        case 'center':
          this.set.documentAlign.center = true;
          break;
        case 'right':
          this.set.documentAlign.right = true;
          break;
      }
    }
  }

}


</script>

<style>

/* Setting Class */
.set-left { text-align: left }
.set-center { text-align: center }
.set-right { text-align: right }
.text-componant { position: relative }
/* Setting Class */

span {
  width: 10rem;
  color: rgba(69, 90, 100, 0.64);
}

textarea {
  display: block;
  width: 100%;
  padding: 0.5rem;
  border-radius: 0.6rem;
  font-family: 'Poppins', sans-serif;
  font-size: 1.6rem;
  background: none;
  border: none;
  resize: none;
}

textarea:focus {
  outline: none;
  background: rgba(69, 90, 100, 0.05);
}

.btn-left-icon {
  padding-left: 2.5rem;
  position: relative;
}

.btn-left-icon>span:nth-child(1) {
  position: absolute;
  top: 0.25rem;
  left: 0.75rem;
}

.editor {
  padding-left: 2rem;
  padding-right: 2rem;
}

button {
  text-align: center;
  padding: 0.1rem 0.2rem;
  margin: 0 0.2rem;
  border: 1px solid rgba(69, 90, 100, 0.5);
  border-radius: 4px;
  font-size: 1rem;
  color: #455a64;
  background: #fff;
}

button:hover {
  background: rgba(69, 90, 100, 0.16);
}

.top-section-control {
  text-align: left !important;
  width: 100%;
  display: block;
  position: absolute;
  left: 0;
  top: 0;
  padding: 0.5rem 0rem;
  border-bottom: 1px solid rgba(69, 90, 100, 0.5);
  border-radius: 2rem 2rem 0 0;
  background: #fff;
}

.top-section-control>div {
  display: flex;
  align-items: center;
  margin-left: 1rem;
  margin-right: 1rem;
}

.bottom-section-control {
  display: block;
  width: 100%;
  position: absolute;
  bottom: 0;
  left: 0;
}

.section-controll>span {
  margin-right: 1rem;
  margin-left: 1.5rem;
  color: #2c3e50;
  opacity: 0.64;
}

.control-name {
  width: 10rem;
  display: inline-block;
  line-height: 48px;
}

.text-area {
  position: relative;
  height: 700px;
  padding: 1rem;
  margin-top: 2rem;
  border: 1px solid rgba(69, 90, 100, 0.5);
  border-radius: 1rem;
}

article {
  padding-top: 2.6rem;
}

.control-document-align {

}

.more-option {
  position: absolute;
  top: 0.6rem;
  left: -1.5rem;
  padding: 0.2rem;
  border: none;
  background: #fff;
  box-shadow: 0px 0px 3px #00000050;
  line-height: 0;
  opacity: 0.5;
}

</style>