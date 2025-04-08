<script setup>
// import ProfileImage from './ProfileImage.vue';
// import User from './User.vue';
// import TimeStamp from './Timestamp.vue';
// import Message from './Message.vue';
// import Actions from './Actions.vue';

const props = defineProps({
  tweet: {
    type: Object,
    required: true
  }
})
     
</script>


<template>
  <div class="tweet">
    <img
      :src="tweet.user.image"
      class="profile"
      alt="profile"
    />

    <div class="body">
      <div class="top">
        <span class="user">
          <span class="name">{{ tweet.user.name }}</span>
          <span class="handle">{{ tweet.user.handle }}</span>
        </span>

        <span class="timestamp">{{ tweet.timestamp }}</span>
      </div>

      <p class="message">{{ tweet.message }}
      </p>

      <div class="actions">
        <!-- Font Awesome icons -->
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
