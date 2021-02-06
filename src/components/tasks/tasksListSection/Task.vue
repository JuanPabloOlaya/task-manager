<template>
  <div class="tasks-list-section__task">
    <div class="card">
      <img
        class="card__image"
        src="https://www.talkwalker.com/images/2020/blog-headers/image-analysis.png"
        alt=""
      />
      <span class="card__title">Card title</span>
      <div class="card__description">
        Lorem ipsum dolor sit, ametaaaaaaaaaaaaa aaaddaaffa Lorem ipsum dolor sit, ametaaaaaaaaaaaaa
        aaaddaaffaLorem ipsum dolor sit, ametaaaaaaaaaaaaa aaaddaaffaLorem ipsum dolor sit,
        ametaaaaaaaaaaaaa aaaddaaffaLorem ipsum dolor sit, ametaaaaaaaaaaaaa aaaddaaffaLorem ipsum
        dolor sit, ametaaaaaaaaaaaaa aaaddaaffa
      </div>
      <div class="card__actions">
        <div class="card__action card__action--delete">
          <i class="mdi mdi-delete"></i>
        </div>
        <div class="card__action card__action--update">
          <i class="mdi mdi-update"></i>
        </div>
        <div class="card__action card__action--detail">
          <i class="mdi mdi-eye-outline"></i>
        </div>
        <div class="card__action">
          <i class="mdi mdi-plus"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Task',
};
</script>
