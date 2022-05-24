<template>
  <div class="card" :id="header.replace(/ /g, '_')" style="width: 18rem">
    <a :href="require(`@/assets/images/${imageUrl}`)" target="_blank">
      <img
        :src="require(`@/assets/images/${imageUrl}`)"
        class="card-img-top"
        :alt="header"
        :title="header"
      />
    </a>
    <div class="card-body">
      <h5 class="card-title">{{ header }}</h5>
      <p v-if="description" class="card-text">{{ description }}</p>
      <ul
        v-if="characteristics"
        class="p-0 mb-0"
        style="list-style-position: inside; list-style: none"
      >
        <li v-for="characteristic in characteristics" :key="characteristic.id">
          <span class="fw-bold">{{ characteristic.type }}:</span>
          <span>{{ characteristic.value }}</span>
        </li>
      </ul>
    </div>
    <div class="card-footer">
      <Badge
        v-for="tag in tags"
        :key="tag.id"
        :text="tag.type"
        color="primary"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    imageUrl: {
      type: String,
      required: true,
    },
    header: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: false,
    },
    characteristics: {
      type: Array,
      required: false,
    },
    tags: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {};
  },
};
</script>
