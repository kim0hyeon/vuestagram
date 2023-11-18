<template>
  <div class="post">
    <div class="post-header">
      <div class="profile" :style="{ backgroundImage: `url(${Posting.userImage})`}"></div>
      <span class="profile-name">{{ Posting.name }}</span>
    </div>
    <div class="post-body" :style="{backgroundImage: 'url('+Posting.postImage+')'}"></div>
    <div class="post-content">
      <p>{{ Posting.likes}} likes</p>
      <p><strong>{{ Posting.filter}}</strong>{{ Posting.content}}</p>
      <p class="date">{{ Posting.date }}</p>
    </div>
</div> 
</template>

<script>

export default {
    name : "PostBox",
    props:{
        Posting : Object,
    },
}
</script>

<style>
.post {
    width: 100%;
}
.profile {
    background-image: url();
    width: 30px;
    height: 30px;
    background-size: 100%;
    border-radius: 50%;
    float: left;
}
.profile-name {
    display: block;
    float: left;
    padding-left: 10px;
    padding-top: 7px;
    font-size: 14px;
}
.post-header {
    height: 30px;
    padding: 10px;
}
.post-body {
    background-image: url();
    height: 450px;
    background-position: center;
    background-size: cover;
}
.post-content {
    padding-left: 15px;
    padding-right: 15px;
    font-size: 14px;
}
.date {
    font-size: 11px;
    color: grey;
    margin-top: -8px;
} 
</style>