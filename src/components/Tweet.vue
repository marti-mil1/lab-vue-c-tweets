<script setup>
import ProfileImage from './ProfileImage.vue';
import User from './User.vue';
import Timestamp from './Timestamp.vue';
import Message from './Message.vue';
import Actions from './Actions.vue';

const props = defineProps({
  tweet: {
    type: Object,
    required: true
  }
})
</script>


<template>
  <div class="tweet">

    <!-- PROFILE IMAGE -->
    <ProfileImage :image="tweet.user.image"></ProfileImage>

    <div class="body">
      <div class="top">
        <!-- USER -->
        <span class="user">
          <User :user="tweet.user"></User>
        </span>

        <!-- TIMESTAMP -->
         <Timestamp :timestamp="tweet.timestamp"></Timestamp>
      </div>

      <!-- MESSAGE -->
       <Message :message="tweet.message"></Message>

      <!--ACTIONS -->
      <Actions></Actions>

    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
