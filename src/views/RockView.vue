<template>
  <div class="rock-screen">
    <div v-if="showForm" class="form-container">
      <h1>Cats Rock!</h1>
      <p>
        Lorem Ipsum is simply dummy text of the printing and typesetting
        industry. Lorem Ipsum has been the industry's standard dummy text ever
        since the 1500s, when an unknown printer took a galley of type and
        scrambled it to make a type specimen book. It has survived not only five
        centuries, but also the leap into electronic typesetting, remaining
        essentially unchanged.
      </p>
      <div class="button-group">
        <button class="agree-btn">I agree</button>
        <button class="disagree-btn" @click="disagree">I do not</button>
      </div>
    </div>
    <div v-else class="form-container">
      <h1>Cats Rock!</h1>
      <p>You said you don’t agree.</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showForm: true,
    };
  },
  methods: {
    disagree() {
      this.showForm = false;
    },
  },
};
</script>

<style>
body {
  background-image: url("@/assets/back.jpeg");
  background-repeat: no-repeat;
  background-size: 100% 100%;
  height: 100vh;
  margin: 0;
  color: white;
  transition: background-size 1s ease, filter 1s ease;
}

.form-container {
  position: absolute;
  top: calc((100% - 532px) / 2);
  left: calc((100% - 532px) / 3);
  width: 378px;
  height: 532px;
  background: #342828;
  padding: 30px 53px;
  border-radius: 12px;
  box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.6);
  text-align: left;
  color: white;
  box-sizing: border-box;
}

.button-group {
  display: flex;
  flex-direction: column;
  margin-top: 50px;
  gap: 15px;
}

.button-group button {
  padding: 20px 20px;
  border: none;
  border-radius: 12px;
  font-size: 16px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
  color: #fff;
  text-align: center;
  cursor: pointer;
}

.button-group > .agree-btn {
  background: #8784ff;
}

.button-group > .disagree-btn {
  background: #f66b6b;
}

@media (max-width: 540px) {
  body {
    background-position: center;
    background-size: cover;
  }
  .form-container {
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    filter: brightness(90%);
  }
}

@media (max-width: 379px) {
  .form-container {
    width: 100%;
    transform: translate(-50%, -23%);
  }
}
</style>
