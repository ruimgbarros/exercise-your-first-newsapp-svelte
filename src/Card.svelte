<script>
    export let name;
    export let company;
    export let jobTitle;
</script>

<div class="rounded overflow-hidden shadow-lg">
  <img class="w-full" src="person_placeholder.png" alt="{name}">
  <div class="px-6 py-4">
    <div class="font-bold text-xl">{name}</div>
    <p class="text-gray-700 text-xs opacity-50 mb-4">
      {company}
    </p>
    <p class="text-gray-700 text-base">
        {jobTitle}
    </p>
  </div>
</div>