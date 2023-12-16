<template>
  <div class="container">
    <div class="profile-picture">
      <img :src="profileImage" alt="Profile">
    </div>
    <div class="description-column">
      <!-- Introduction -->
      <h2>Hello, I'm Dicky! An Aspiring Data Engineer</h2>
      <p>Wanna see my portfolio?</p>
      <!-- Social links with icons -->
      <div class="links">
        <a href="https://www.linkedin.com/in/dickymuhr/" target="_blank" rel="noopener noreferrer" class="social-link">
          <img :src="linkedinIcon" alt="LinkedIn">
        </a>
        <a href="https://github.com/dickymuhr" target="_blank" rel="noopener noreferrer" class="social-link">
          <img :src="githubIcon" alt="GitHub">
        </a>
        <a href="https://medium.com/@dickymuhrizal" target="_blank" rel="noopener noreferrer" class="social-link">
          <img :src="mediumIcon" alt="Medium">
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data() {
    return {
      profileImage: require('@/assets/img/profile.png'),
      linkedinIcon: require('@/assets/img/LinkedIn.png'),
      githubIcon: require('@/assets/img/GitHub.png'),
      mediumIcon: require('@/assets/img/Medium.png'),
    };
  }
};
</script>

<style scoped>
.container {
  display: flex;
  align-items: center; /* This will vertically center the children */
  justify-content: center; /* This will horizontally center the children */
  height: 100%; /* This ensures that the container is at least the height of the viewport */
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
  max-width: 54%; /* Sets the max width to enforce the 1:2 ratio */
}

h2 {
  margin: 0 0 20px; /* Adjust the margin as needed for your design */
  font-size: 2rem; /* Adjust the font size as needed */
}

p {
  margin: 0 0 20px; /* Adjust the margin as needed for your design */
  font-size: 1.4rem;
}

.links {
  display: flex; /* Use flexbox for the links container */
  justify-content: flex-start; /* Align links to the start */
  align-items: center; /* Center links vertically */
  gap: 10px; /* Creates a gap between each link */
}

.links a.social-link {
  display: flex; /* Use flexbox for individual link alignment */
  justify-content: center; /* Center the content horizontally */
  align-items: center; /* Center the content vertically */
  width: 54px; /* Fixed width for the link background */
  height: 54px; /* Fixed height for the link background */
  background-color: #ffffff; /* White background */
  border-radius: 4px; /* Rounded corners */
  overflow: hidden; /* Ensures no overflow from the content */
}

.links a.social-link img {
  width: 80%; /* Scaled down size, adjust as needed */
  height: auto; /* Maintain aspect ratio */
  object-fit: contain; /* Ensures the image fits within the element's box */
}

.links a.social-link:hover {
  background-color: #e1e1e1; /* Light grey background on hover */
}


/* Responsive styles and additional styling as needed */
</style>