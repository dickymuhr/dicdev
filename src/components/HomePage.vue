<template>
  <div class="container">
    <div class="profile-picture">
      <img :src="profileImage" alt="Profile">
    </div>
    <div class="description-column">
      <!-- This is where your introduction and links will go -->
      <h2>Hello, I'm Dicky, An Aspiring Data Engineer</h2>
      <p>Wanna see my portfolio?</p>
      <!-- Social links -->
      <div class="links">
        <!-- Replace '#' with actual links -->
        <a href="#" class="social-link linkedin">LinkedIn</a>
        <a href="#" class="social-link github">GitHub</a>
        <a href="#" class="social-link medium">Medium</a>
        <!-- More links as needed -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data() {
    return {
      // This will include the image via webpack
      profileImage: require('@/assets/img/profile.png')
    };
  }
};
</script>

<style scoped>
.container {
  display: flex;
  align-items: center; /* This will vertically center the children */
  justify-content: center; /* This will horizontally center the children */
  min-height: 100vh; /* This ensures that the container is at least the height of the viewport */
  background-color: #04192C;
  color: #ffffff;
  padding: 0;
  margin: 0;
}

.profile-picture {
  flex: 0 0 33%; /* Gives the profile picture column a fixed width based on the container's width */
  text-align: right; /* Centers the image within the profile picture column */
}

.profile-picture img {
  width: auto; /* maintain the aspect ratio */
  height: auto; /* maintain the aspect ratio */
  max-width: 24em; 
}
.description-column {
  flex-grow: 1; /* Allows the description column to take up the remaining space */
  text-align: left; /* Aligns the text to the left */
  padding-left: 20px; /* Adds spacing between the columns */
  max-width: 66%; /* Sets the max width to enforce the 1:2 ratio */
}

h2 {
  margin: 0 0 20px; /* Adjust the margin as needed for your design */
  font-size: 2rem; /* Adjust the font size as needed */
}

p {
  margin: 0 0 20px; /* Adjust the margin as needed for your design */
}

.links a {
  display: inline-block;
  margin-right: 10px;
  text-decoration: none; /* Removes the underline from links */
  color: #ffffff; /* Sets the text color */
  /* Additional styles for your links */
}

/* Responsive styles and additional styling as needed */
</style>