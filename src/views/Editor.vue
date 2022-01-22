<template>
  <div class="editor">


    <!-- Text Area -->
    <div class="text-area">

      <!-- Section Controll -->
      <div class="top-section-control">
        <div>
          <span>Text Align </span>
        </div>
        <button>Left</button>
        <button>Center</button>
        <button>Right</button>
      </div>

      <!-- Componant Box -->
      <div class="bottom-section-control">
        <div>
          <div>
            <span>Componants </span>
          </div>
          <button><menu-icon/> HeadLine 1</button>
          <button>HeadLine 2</button>
          <button>HeadLine 3</button>
          <button>Caption</button>
          <button>Body</button>
        </div>
      </div>

    </div>

  </div>
</template>

<script>
import MenuIcon from 'vue-material-design-icons/Menu.vue';

components: {
  MenuIcon;
}


</script>

<style>

.editor {
  padding-left: 2rem;
  padding-right: 2rem;
}

button {
  text-align: center;
  padding: 0.5rem 1rem;
  margin: 0.2rem;
  border: 1px solid rgba(69, 90, 100, 0.5);
  border-radius: 4px;
  font-size: 1rem;
  color: #455a64;
  background: rgba(69, 90, 100, 0.05);
}

button:hover {
  background: rgba(69, 90, 100, 0.16);
}

.top-section-control, .bottom-section-control>div {
  display: inline-block;
  padding: 0.5rem 1rem;
  border-radius: 1rem;
  background: #fff;
  box-shadow: 0px 4px 1rem rgba(69, 90, 100, 0.16);
}

.top-section-control {
  display: block;
  padding: 0.5rem 0rem;
  width: 100%;
  vertical-align: middle;
  position: absolute;
  left: 0;
  top: 0;
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

.text-area {
  position: relative;
  height: 700px;
  padding: 1rem;
  margin-top: 2rem;
  border: 1px solid rgba(69, 90, 100, 0.5);
  border-radius: 1rem;
}

</style>