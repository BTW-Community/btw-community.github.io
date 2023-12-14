---
# the default layout is 'page'
icon: fa-solid fa-download
order: 2
---

{% include lang.html %}

<h2>Which file should I download?</h2>

<p>Please check out our <a href="">installation page</a>.</p>

<template id="release-template">
  <article class="card card-wrapper" style="border: 1px solid gray">
    <div class="card-body">
      <h2 slot="name" class="card-title" style="margin-top: 0">NAME</h2>
      <p slot="description" class="card-text content" style="white-space: pre-line; max-height: 6em; overflow-y: scroll"></p>
      <a slot="url" class="btn btn-primary">Download</a>
    </div>
  </article>
</template>

<section id="post-list"></section>

<script type="module">

  const getSlot = (el, name) => el.querySelector(`[slot="${name}"]`);

  const addRelease = async (repo, id) => {
    const response = await fetch(`https://api.github.com/repos/BTW-Community/${repo}/releases/${id}`);
    const release = await response.json();

    const template = document.getElementById("release-template");
    const element = template.content.cloneNode(true);

    getSlot(element, "name").textContent = release.name;
    getSlot(element, "description").textContent = release.body;
    getSlot(element, "url").href = release.assets[0].browser_download_url;

    return element;
  }

  const elements = await Promise.all([
    ["cursed-fabric-loader", "latest"],
    ["BTW-Public", "latest"]
  ].map(args => addRelease(...args)));

  const section = document.getElementById("post-list");
  section.append(...elements);

</script>
