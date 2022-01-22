<template>
  <div>
    <!-- Section Controll -->
    <div class="section-controll">
      <span>Text Align</span>
      <button>Left</button>
      <button>Center</button>
      <button>Right</button>

      <span>Add</span>
      <button>HeadLine</button>
      <button>Caption</button>
      <button></button>
    </div>

  </div>
</template>

<script>

</script>

<style>

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

.section-controll {
  display: inline-block;
  padding: 0.5rem 1rem;
  border-radius: 1rem;
  background: #fff;
  box-shadow: 0px 4px 1rem rgba(69, 90, 100, 0.16);
}

.section-controll>span {
  margin-right: 1rem;
  margin-left: 1.5rem;
  color: #2c3e50;
  opacity: 0.64;
}

</style>