<template>
  <div class="card reveal">
        <div class="content">
          <div v-html="skill.svg"/>
          <div class="text-content">
            <h2 class="text-white">{{skill.skillname}}</h2>
            <p class="text-white m-0">{{skill.description}}</p>
            <ul>
              <li v-for="item in skill.items" class="text-white">
                {{item.itemname}}
              </li>
            </ul>
          </div>
        </div>
      </div>
</template>

<script>
export default {
    props: ['skill']
}
</script>

<style>

</style>