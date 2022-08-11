<template>
  <div className="tweet">
    <ProfileImage :profileImage="user.image"/>
    <div className="body">
      <div className="top">
        <span className="user">
         <User :user="user"/>
        </span>
        <Timestamp :timestamp="timestamp"/>
        
      </div>
      <Message :message="message"/>

      <div className="actions">
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

<script>
import ProfileImage from "./ProfileImage.vue";
import Message from "./Message.vue";
import Timestamp from "./Timestamp.vue";
import User from "./User.vue";

export default {
  name: "Tweet",
  components: {
    Message, ProfileImage, Timestamp, User
  },
  props: {
    user: Object,
    timestamp: String,
    message: String,
    profileImage: String,
  }
};


</script>

<style scoped>
a {
  color: #42b983;
}
</style>
