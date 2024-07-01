<script>
  async function handleFileSelect(event) {
    const file = event.target.files[0];
    if (!file) return;

    const formData = new FormData();
    formData.append("file", file);

    const response = await fetch("/api/upload", {
      method: "POST",
      headers: {
        Authorization:
          "Bearer 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",
      },
      body: formData,
    });
  }
</script>

<div
  class="bg-base-300 w-screen h-screen grid grid-cols-1 gap-4 content-center justify-items-center"
>
  <div class="card card-compact bg-base-100 w-1/2 h-full shadow-xl">
    <figure>
      <img
        src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.jpg"
        alt="Shoes"
      />
    </figure>
    <div class="card-body">
      <h2 class="card-title">Shoes!</h2>
      <p>If a dog chews shoes whose shoes does he choose?</p>
    </div>
  </div>
  <input
    type="file"
    class="file-input file-input-bordered file-input-primary w-full max-w-xs"
  />
</div>
