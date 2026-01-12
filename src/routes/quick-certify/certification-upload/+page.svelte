<div class="py-12 px-4 sm:px-6 lg:px-8 max-w-4xl mx-auto">

<h1 class="mb-6 text-2xl font-semibold text-gray-900 dark:text-white text-center">
    Add New Design
  </h1>


  <p class="mb-12 text-xl text-center text-gray-600 max-w-2xl mx-auto">Add a new certificate or Badge Design by selecting name & Image</p>

  <form class="space-y-8">
  <br>
    <!-- Name Field -->
    <div class="max-w-lg mx-auto">
      <label for="add-name" class="block mb-3 text-sm font-semibold text-gray-900">Add Name</label>
      <input 
        id="add-name"
		data-testid = "certificate-name"
        type="text" 
        class="w-full px-4 py-3 border border-gray-300 rounded-lg shadow-sm text-gray-900 placeholder-gray-500 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-blue-500 text-sm" 
        placeholder="Enter certificate name"
        required 
      />
    </div>

    <!-- File Upload -->
<div class="max-w-lg mx-auto">
  <label for="dropzone-file" class="block mb-3 text-sm font-semibold text-gray-900">Upload Certificate Image</label>
  <div class="w-full h-60 border-2 border-dashed border-gray-300 rounded-lg bg-white hover:border-blue-400 hover:bg-gray-50 transition-all duration-200 cursor-pointer group p-8">
    <div class="flex flex-col items-center justify-center text-center h-full space-y-3">
      <svg class="w-12 h-12 text-gray-400 group-hover:text-blue-500 transition-all duration-200" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M15 13l-3-3m0 0l-3 3m3-3v12"/>
      </svg>
      <div>
        <p class="text-sm font-semibold text-gray-700 group-hover:text-blue-500">Click to upload or drag</p>
        <p class="text-xs text-gray-500 leading-relaxed max-w-xs">Upload A4 (1100 × 800) size image for certificate or 400×400 for Badge</p>
      </div>
    </div>
    <input 
      id="dropzone-file" 
      type="file" 
      class="hidden"
      accept="image/*"
      on:change={handleFileChange}
    />
  </div>
</div>


    <div class="flex flex-col sm:flex-row gap-4 justify-end max-w-lg mx-auto pt-8">
      <input type="submit" name="commit" value="Save Design" class="btn-primary" data-disable-with="Save Design">
      <input type="submit" name="commit" value="Replace Image" class="btn-primary" data-disable-with="Replace Image">
    </div>
  </form>
</div>

<style>
  @layer base {
    @import 'https://cdn.tailwindcss.com';
  }
</style>
