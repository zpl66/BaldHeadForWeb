<template>
  <ContentBase>
    <div class="about">
      <h1>About Us</h1>

      <div class="part">
        <h2>Who Are We?</h2>
        <img src="@/assets/about/we.jpg" alt="who are we">
        <p>We are a team of five dedicated students from Class 5, <br>
          Software Engineering at Hainan University,<br>
          brought together by a shared passion for web development and innovative problem-solving.<br>
          <br>
          As part of our academic journey, <br>
          we have embarked on a collaborative project aimed at creating an website<br>
          that showcases both our technical expertise and creative vision.
        </p>
        <br>
        <table class="table table-success table-striped">
          <thead>
            <tr>
              <th>Role</th>
              <th>Name</th>
            </tr>
          </thead>

          <tbody>
            <tr>
              <td>Leader</td>
              <td>Dumpling</td>
            </tr>

            <tr>
              <td>Member</td>
              <td>Casssie</td>
            </tr>

            <tr>
              <td>Member</td>
              <td>Young</td>
            </tr>

            <tr>
              <td>Member</td>
              <td>Alma</td>
            </tr>

            <tr>
              <td>Member</td>
              <td>Issac</td>
            </tr>
          </tbody>
        </table>
      </div>

      <div class="part">
        <h2>Our Vision</h2>
        <img src="@/assets/about/vision.jpg" alt="our vision">
        <p>
          The aim of Whisper-Space is to create a serene and welcoming environment, <br>
          where individuals can freely express their innermost thoughts and feelings. <br>
          <br>
          We envision this platform as a modern-day confessional, <br>
          a safe space <br>
          where users can unburden themselves, <br>
          knowing their voices will be heard without judgment. <br>
          <br>
          Whether someone wishes to speak under the veil of anonymity <br>
          or with the comfort of their identity,<br>
          Whisper-Space is designed to foster a sense of connection, empathy, and relief. <br>
          <br>
          Our goal is to build a community <br>
          that encourages open dialogue, offering people a sanctuary <br>
          to share their stories, worries, or simple reflections. <br>
          <br>
          By blending thoughtful design with intuitive features, <br>
          we strive to make Whisper-Space a place of solace, <br>
          where users can retreat from the noise of everyday life <br>
          and find comfort in the act of speaking from the heart.
        </p>
      </div>

      <div class="part">
        <h2>A Journey of Growth</h2>
        <img src="@/assets/about/learn.jpg" alt="learn">
        <p>This project is more than just a coursework requirement<br>
          —it is an opportunity for us to refine our skills, embrace creativity, <br>
          and work as a cohesive unit.<br>
          <br>
          We hope that through our efforts, <br>
          this website will stand as a testament to our dedication <br>
          and the knowledge we have gained throughout our studies.
        </p>
      </div>
    </div>
  </ContentBase>
</template>

<script>
import ContentBase from '@/components/ContentBase.vue';

export default {
  name: "AboutView",
  components: {
    ContentBase,
  }
}
</script>

<style scoped>
/* 使用 @font-face 定义 SigmarOne 字体 */
@font-face {
  font-family: 'Dosis';
  src: url('@/assets/fonts/Dosis.ttf') format('truetype');
  font-weight: normal;
  font-style: normal;
}

/* 使用 Comforter 字体 */
.about {
  font-family: 'Dosis', sans-serif;
  margin: 0;
  padding: 0;
  text-align: center;
}

.part {
  margin: 20px;
}

h1 {
  color: orange;
  font-weight: bold;
}

h2 {
  color: yellow;
  font-weight: bold;
}

p {
  font-size: 1.17em;
  line-height: 1.6;
  font-weight: bold;
}

img {
  width: atuo;
  height: 200px;
  opacity: 0.9;
  border-radius: 10px;
  margin: 10px;
}

table {
  width: 50%;
  opacity: 0.9;
  margin: auto;
}

table th:first-child {
  border-top-left-radius: 10px;
}

table th:last-child {
  border-top-right-radius: 10px;
}

table tr:last-child td:first-child {
  border-bottom-left-radius: 10px;
}

table tr:last-child td:last-child {
  border-bottom-right-radius: 10px;
}
</style>