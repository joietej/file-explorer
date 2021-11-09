<script setup lang="ts">
import { File } from "../hooks/useFolders";
import { Switch } from "@headlessui/vue";
import { PhotographIcon, DocumentIcon } from "@heroicons/vue/outline";
import { CheckCircleIcon } from "@heroicons/vue/solid";

defineProps<{
  file: File;
  isChecked: boolean;
}>();

defineEmits<{
  (e: "change", checked: boolean): void;
}>();
</script>

<template>
  <li
    :class="isChecked ? 'bg-blue-100' : 'bg-white'"
    class="
      flex
      rounded
      p-2
      gap-2
      mt-2
      justify-between
      align-middle
      hover:bg-blue-50
    "
  >
    <Switch
      data-testid="fileSwitchContainer"
      class="w-full"
      v-model="isChecked"
      @click="$emit('change', isChecked)"
    >
      <div class="w-full flex justify-between">
        <div class="flex align-middle">
          <PhotographIcon
            v-if="file?.mimeType?.includes('image')"
            data-testid="fileImageIcon"
            class="w-6 h-6"
          />
          <DocumentIcon v-else data-testid="fileDocIcon" class="w-6 h-6" />
          <span class="ml-4 text-sm font-light text-gray-600">{{
            file?.name
          }}</span>
        </div>
        <CheckCircleIcon
          v-show="isChecked"
          data-testid="fileCheckIcon"
          class="h-6 w-6 text-blue-600"
        />
      </div>
    </Switch>
  </li>
</template>
