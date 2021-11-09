<script setup lang="ts">
import { ref } from "@vue/reactivity";
import FileInfo from "./components/FileInfo.vue";
import { File } from "./hooks/useFolders";

const file: File = {
  id: "1",
  name: "foo.jpg",
  mimeType: "image/jpeg",
  url: "",
  parentFolderId: "",
};

const selectedFiles = ref<Array<File>>([]);

const onFileSelect = (checked: boolean, file: File) => {
  console.log(checked)
  if (checked) {
    selectedFiles.value = [
      ...selectedFiles.value.filter((x) => x.id !== file.id), file
    ];
  } else {
    selectedFiles.value = [
      ...selectedFiles.value.filter((x) => x.id !== file.id)
    ];
  }
};

const isSelected = (file: File) =>
  selectedFiles.value.map((f) => f.id).includes(file.id);
</script>

<template>
  <FileInfo
    :file="file"
    @change="onFileSelect($event, file)"
    :isChecked="isSelected(file)"
  />

  <ul>
    <li :key="f.id" v-for="f in selectedFiles">{{ f.name }}</li>
  </ul>
</template>
