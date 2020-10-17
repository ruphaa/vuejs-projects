<template>
  <div class="project">
    <img :src="project.image" alt />
    <div class="overlay"></div>
    <a :href="project.url" class="hide" target="_blank" rel="noreferrer">{{project.title}}</a>
  </div>
</template>

<script>
export default {
  props: ["project"]
};
</script>

<style>
.project {
  width: 290px;
  height: 260px;
  box-shadow: 0px 3px 10px 1px rgba(208, 208, 208, 0.16);
  border-radius: 10px;
  cursor: pointer;
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.project:hover {
  /* background: rgba(98, 105, 243, 0.46); */
  transition: all 0.3s ease;
}
.project img {
  transform: scale(1.15);
  transition: all 0.3s ease;
  width: 251px;
  height: 223px;
  border-radius: 4px;
}

.project a {
  display: none;
  position: absolute;
  margin: auto;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
}
.project .overlay {
  display: none;
}

.project:hover a {
  display: inline;
  width: 150px;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #444ac7;
  border-radius: 10px;
  color: #ffffff;
  font-weight: bold;
  font-size: 14px;
  line-height: 22px;
  text-decoration: none;
  letter-spacing: 1px;
  max-height: 50px;
}

.project:hover .overlay {
  position: absolute;
  display: block;
  transform: scale(1.15);
  transition: all 0.3s ease;
  width: 251px;
  height: 223px;
  border-radius: 4px;
  background: rgba(98, 105, 243, 0.46);
  opacity: 0.7;
}
</style>