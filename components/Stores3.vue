<template lang="">
        
      <main class="flex-1 ">
         




            <div class="md:p-5 md:px-10 h-full p-2 mt-8 bg-white rounded-3xl shadow">
                <!-- Flex Layout for Form and Manage Everything Section -->
                <div class="flex flex-col h-full gap-3 text-[#212121] py-6 md:gap-20 md:flex-row">
                    <!-- Form Section -->
                    <div class="flex-1 h-full">
                       <div class="w-1/1">
  <h2 class="pt-[10px] text-[26px] font-bold ">Let's catch your visitors' attention.</h2>
  <p class="text-[14px] text-[#656565] mt-[3px]">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed diam nonumy...</p>

  <form class="mt-10  ">
    <!-- Favicon -->
    <div>
      <label class="block font-semibold tracking-wider text-sm text-[#656565]">Fav-icon – Your tab favicon</label>
      <p class="text-[12px] text-[#7A7878]">Your favicon must be 16 × 16</p>
      
      <!-- Upload Area -->
      <div v-if="!faviconPreview" 
           @click="$refs.faviconInput.click()" 
           class="shadow-[0px_0px_6px_#0000001A] cursor-pointer mt-5 flex items-center rounded-2xl border border-[#3A0CA324] border-dashed bg-gray-50 px-4 py-3">
        <div class="w-[100%] text-center">
          <svg class="size-8 text-[#3A0CA3] mx-auto" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="currentColor" d="m12 15.577l-3.539-3.538l.708-.72L11.5 13.65V5h1v8.65l2.33-2.33l.709.719zM6.616 19q-.691 0-1.153-.462T5 17.384v-2.423h1v2.423q0 .231.192.424t.423.192h10.77q.23 0 .423-.192t.192-.424v-2.423h1v2.423q0 .691-.462 1.153T17.384 19z"/></svg>
          <p class="mt-[4px] text-[14px] leading-[18px] text-gray-400">Attach your favicon here<br />or<br /><span class="text-[#C0ADF4]">Browse your favicon</span></p>
        </div>
      </div>

      <!-- Preview Area -->
      <div v-else class="shadow-[0px_0px_6px_#0000001A] mt-5 rounded-2xl border border-[#3A0CA324] bg-gray-50 px-4 py-3">
        <div class="relative">
          <img :src="faviconPreview" alt="Logo Preview" class="max-h-[200px] w-auto mx-auto object-contain" />

          <button @click="removeFavicon" class="absolute -top-2 -right-2 bg-red-500 text-white rounded-full p-1 hover:bg-red-600">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
      </div>

      <input 
        type="file" 
        class="hidden" 
        ref="faviconInput"
        @change="handleFaviconUpload" 
        accept="image/*"
      />
      
      <div class="mt-[6px] flex text-[#A988F5] gap-[3px] items-center w-[100%] justify-end">
        <svg class="size-3.5" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="currentColor" fill-rule="evenodd" d="M5.25 9.303V8a6.75 6.75 0 0 1 13.5 0v1.303q.34.023.642.064c.9.12 1.658.38 2.26.981c.602.602.86 1.36.982 2.26c.116.867.116 1.97.116 3.337v.11c0 1.367 0 2.47-.116 3.337c-.122.9-.38 1.658-.982 2.26s-1.36.86-2.26.982c-.867.116-1.97.116-3.337.116h-8.11c-1.367 0-2.47 0-3.337-.116c-.9-.122-1.658-.38-2.26-.982s-.86-1.36-.981-2.26c-.117-.867-.117-1.97-.117-3.337v-.11c0-1.367 0-2.47.117-3.337c.12-.9.38-1.658.981-2.26c.602-.602 1.36-.86 2.26-.981q.301-.041.642-.064M6.75 8a5.25 5.25 0 0 1 10.5 0v1.253q-.56-.004-1.195-.003h-8.11q-.634 0-1.195.003zm-3.341 3.409c.277-.277.665-.457 1.4-.556c.754-.101 1.756-.103 3.191-.103h8c1.435 0 2.436.002 3.192.103c.734.099 1.122.28 1.399.556c.277.277.457.665.556 1.4c.101.755.103 1.756.103 3.191s-.002 2.436-.103 3.192c-.099.734-.28 1.122-.556 1.399c-.277.277-.665.457-1.4.556c-.755.101-1.756.103-3.191.103H8c-1.435 0-2.437-.002-3.192-.103c-.734-.099-1.122-.28-1.399-.556c-.277-.277-.457-.665-.556-1.4c-.101-.755-.103-1.756-.103-3.191s.002-2.437.103-3.192c.099-.734.28-1.122.556-1.399" clip-rule="evenodd"/></svg>
        <p class="mt-[2px] text-sm ">Secure</p>
      </div>
    </div>

    <!-- Logo -->
    <div>
      <label class="block font-semibold tracking-wider text-sm text-[#656565]">Logo — Your visual identity</label>
      <p class="text-[12px] text-[#7A7878]">Your favicon must be 16 × 16</p>
      
      <!-- Upload Area -->
      <div v-if="!logoPreview" 
           @click="$refs.logoInput.click()" 
           class="shadow-[0px_0px_6px_#0000001A] cursor-pointer mt-5 flex items-center rounded-2xl border border-[#3A0CA324] border-dashed bg-gray-50 px-4 py-3">
        <div class="w-[100%] text-center">
          <svg class="size-8 text-[#3A0CA3] mx-auto" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="currentColor" d="m12 15.577l-3.539-3.538l.708-.72L11.5 13.65V5h1v8.65l2.33-2.33l.709.719zM6.616 19q-.691 0-1.153-.462T5 17.384v-2.423h1v2.423q0 .231.192.424t.423.192h10.77q.23 0 .423-.192t.192-.424v-2.423h1v2.423q0 .691-.462 1.153T17.384 19z"/></svg>
          <p class="mt-[4px] text-[14px] leading-[18px] text-gray-400">Attach your Logo here<br />or<br /><span class="text-[#C0ADF4]">Browse Logo</span></p>
        </div>
      </div>

      <!-- Preview Area -->
      <div v-else class="shadow-[0px_0px_6px_#0000001A] mt-5 rounded-2xl border border-[#3A0CA324] bg-gray-50 px-4 py-3">
        <div class="relative">
          <img :src="logoPreview" alt="Logo Preview" class="max-h-[200px] w-auto mx-auto object-contain" />
          <button @click="removeLogo" class="absolute -top-2 -right-2 bg-red-500 text-white rounded-full p-1 hover:bg-red-600">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
      </div>

      <input 
        type="file" 
        class="hidden" 
        ref="logoInput"
        @change="handleLogoUpload" 
        accept="image/*"
      />
      
      <div class="mt-[6px] flex text-[#A988F5] gap-[3px] items-center w-[100%] justify-end">
        <svg class="size-3.5" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="currentColor" fill-rule="evenodd" d="M5.25 9.303V8a6.75 6.75 0 0 1 13.5 0v1.303q.34.023.642.064c.9.12 1.658.38 2.26.981c.602.602.86 1.36.982 2.26c.116.867.116 1.97.116 3.337v.11c0 1.367 0 2.47-.116 3.337c-.122.9-.38 1.658-.982 2.26s-1.36.86-2.26.982c-.867.116-1.97.116-3.337.116h-8.11c-1.367 0-2.47 0-3.337-.116c-.9-.122-1.658-.38-2.26-.982s-.86-1.36-.981-2.26c-.117-.867-.117-1.97-.117-3.337v-.11c0-1.367 0-2.47.117-3.337c.12-.9.38-1.658.981-2.26c.602-.602 1.36-.86 2.26-.981q.301-.041.642-.064M6.75 8a5.25 5.25 0 0 1 10.5 0v1.253q-.56-.004-1.195-.003h-8.11q-.634 0-1.195.003zm-3.341 3.409c.277-.277.665-.457 1.4-.556c.754-.101 1.756-.103 3.191-.103h8c1.435 0 2.436.002 3.192.103c.734.099 1.122.28 1.399.556c.277.277.457.665.556 1.4c.101.755.103 1.756.103 3.191s-.002 2.436-.103 3.192c-.099.734-.28 1.122-.556 1.399c-.277.277-.665.457-1.4.556c-.755.101-1.756.103-3.191.103H8c-1.435 0-2.437-.002-3.192-.103c-.734-.099-1.122-.28-1.399-.556c-.277-.277-.457-.665-.556-1.4c-.101-.755-.103-1.756-.103-3.191s.002-2.437.103-3.192c.099-.734.28-1.122.556-1.399" clip-rule="evenodd"/></svg>
        <p class="mt-[2px] text-sm ">Secure</p>
      </div>
    </div>

    <!-- Slogan -->
    <div>
      <label class="block font-semibold   tracking-wider text-sm text-[#656565]">Slogan – Choose your Motto!</label>
      <input type="text" class="mt-[10px] shadow-[0px_0px_6px_#0000001A] w-full rounded-2xl border bg-gray-100 px-4 py-6 focus:outline-none focus:ring focus:ring-indigo-300" placeholder="" />
      <p class="mt-[6px] text-[14px] font-medium text-[#7A7878]">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
    </div>
  </form>
  <div class="grid grid-cols-2 gap-2 sm:grid-cols-12 mt-5 sm:gap-4">
                          <button type="submit "
                            class="mt-6 bg-[#E3E3E3] sm:col-span-5 xl:col-span-4 hover:bg-gray-300 shadow-[0px_0px_6px_#0000001A] text-[#3A0CA3] px-6 py-3.5 rounded-full ">Previous</button>
                          <button type="submit "
                            class="mt-6 bg-[#3A0CA3] sm:col-span-7 xl:col-span-8 hover:bg-opacity-80 shadow-[0px_0px_6px_#0000001A] text-[#fff] px-6 py-3.5 rounded-full ">Next</button>
                        </div>
</div>

                    </div>

                    <!-- Manage Everything Section -->
                    <div class="flex-1 flex-col flex justify-between">
                    <div class="w-[100%] h-full justify-center flex flex-col items-center mt-10 md:mt-[170px]">
                        <label for="file-upload" class="cursor-pointer group">
                            <div class="x border-gray-300 rounded-lg p-8 text-center hover:border-[#3A0CA3] transition-colors">
                                <svg class="size-14 text-gray-400 group-hover:text-[#3A0CA3] mx-auto mb-4" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="currentColor" d="M5 3h13a3 3 0 0 1 3 3v13a3 3 0 0 1-3 3H5a3 3 0 0 1-3-3V6a3 3 0 0 1 3-3m0 1a2 2 0 0 0-2 2v11.59l4.29-4.3l2.5 2.5l5-5L20 16V6a2 2 0 0 0-2-2zm4.79 13.21l-2.5-2.5L3 19a2 2 0 0 0 2 2h13a2 2 0 0 0 2-2v-1.59l-5.21-5.2zM7.5 6A2.5 2.5 0 0 1 10 8.5A2.5 2.5 0 0 1 7.5 11A2.5 2.5 0 0 1 5 8.5A2.5 2.5 0 0 1 7.5 6m0 1A1.5 1.5 0 0 0 6 8.5A1.5 1.5 0 0 0 7.5 10A1.5 1.5 0 0 0 9 8.5A1.5 1.5 0 0 0 7.5 7"/></svg>
                               
                            </div>
                            <input id="file-upload" type="file" class="hidden" @change="handleFileUpload" multiple accept="image/*">
                        </label>
                        
                        <!-- File Upload Preview -->
                        <div v-if="uploadedFiles.length" class="mt-4 w-full">
                            <div v-for="(file, index) in uploadedFiles" :key="index" 
                                 class="flex items-center justify-between p-3 bg-gray-50 rounded-lg mb-2">
                                <div class="flex items-center">
                                    <svg class="w-6 h-6 text-gray-400 mr-2" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z" />
                                    </svg>
                                    <span class="text-sm text-gray-700 cursor-pointer" @click="previewFile(file)">{{ file.name }}</span>
                                </div>
                                <button @click="confirmRemoveFile(index)" class="text-red-500 hover:text-red-700">
                                    <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                                        <path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd" />
                                    </svg>
                                </button>
                            </div>
                        </div>
                    </div>
                    <div class="md:mt-[130px] mt-5 md:ml-0  w-full p-5 border-[#DBDBDB] rounded-[20px] border-2 ">
                        <p class="font-semibold mb-3 text-[1.4rem]">Communicate with your audience</p>
                        <p class="text-[14px] text-[#656565]">Invidunt ut labore et dolore magna aliquyam era. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.</p>
                        
                    </div>
                </div>
                </div>
            </div>
        </main>

<div v-if="showNotification" 
   class="fixed bottom-5 right-5 bg-white shadow-lg rounded-lg p-4 flex items-center space-x-3 transition-all duration-300"
   :class="uploadStatus === 'progress' ? 'border-blue-500' : 'border-green-500'"
   style="border-left: 4px solid">
<div v-if="uploadStatus === 'progress'" class="flex items-center">
  <svg class="animate-spin h-5 w-5 text-blue-500 mr-2" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
    <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
    <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
  </svg>
  <span>Uploading file... {{ uploadProgress }}%</span>
</div>
<div v-else class="flex items-center">
  <svg class="h-5 w-5 text-green-500 mr-2" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
    <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
  </svg>
  <span>File uploaded successfully!</span>
</div>
<button @click="showNotification = false" class="text-gray-400 hover:text-gray-600">
  <svg class="h-4 w-4" fill="currentColor" viewBox="0 0 20 20">
    <path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd" />
  </svg>
</button>
</div>

<!-- File Preview Modal -->
<div v-if="showFilePreview" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center">
<div class="bg-white p-5 rounded-lg shadow-lg max-w-lg w-full">
  <button @click="showFilePreview = false" class="text-gray-400 hover:text-gray-600 float-right">
    <svg class="h-4 w-4" fill="currentColor" viewBox="0 0 20 20">
      <path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd" />
    </svg>
  </button>
  <div v-if="previewFileType === 'image'">
    <img :src="previewFileContent" alt="File Preview" class="w-full h-auto" />
  </div>
  <div v-else>
    <p class="text-gray-700">Preview not available for this file type.</p>
  </div>
</div>
</div>

<!-- Delete Confirmation Modal -->
<div v-if="showDeleteConfirm" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50">
<div class="bg-white rounded-lg p-6 w-[400px] shadow-xl">
  <div v-if="deleteStatus === 'confirm'">
    <div class="text-center mb-4">
      <svg class="w-16 h-16 text-red-500 mx-auto" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v1.59l3.293 3.293c.359.358.587.847.587 1.414z" />
      </svg>
    </div>
    <h3 class="text-xl font-bold text-center mb-4">Delete File</h3>
    <p class="text-gray-600 text-center mb-6">Are you sure you want to delete this file? This action cannot be undone.</p>
    <div class="flex justify-center space-x-4">
      <button @click="cancelDelete" class="px-4 py-2 bg-gray-200 text-gray-800 rounded-lg hover:bg-gray-300 transition-colors">
        Cancel
      </button>
      <button @click="confirmDelete" class="px-4 py-2 bg-red-500 text-white rounded-lg hover:bg-red-600 transition-colors">
        Delete
      </button>
    </div>
  </div>

  <div v-if="deleteStatus === 'progress'" class="text-center">
    <div class="mb-4">
      <svg class="animate-spin h-12 w-12 text-red-500 mx-auto" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
        <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
        <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
      </svg>
    </div>
    <p class="text-gray-600">Deleting file...</p>
  </div>

  <div v-if="deleteStatus === 'success'" class="text-center">
    <div class="mb-4">
      <svg class="h-12 w-12 text-green-500 mx-auto" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
      </svg>
    </div>
    <p class="text-gray-600">File deleted successfully!</p>
  </div>
</div>
</div>
</template>
<script>
export default {
data() {
    return {
        uploadedFiles: [],
        showNotification: false,
        uploadStatus: 'progress', // 'progress' or 'success'
        uploadProgress: 0,
        showFilePreview: false,
        previewFileContent: '',
        previewFileType: '',
        showDeleteConfirm: false,
        deleteStatus: 'confirm', // 'confirm', 'progress', 'success'
        fileToDeleteIndex: null,
        faviconPreview: null,
        logoPreview: null,
    }
},
methods: {
    async handleFileUpload(event) {
        const files = Array.from(event.target.files);
        this.showNotification = true;
        this.uploadStatus = 'progress';
        
        // Simulate upload progress
        for (let i = 0; i <= 100; i += 10) {
            this.uploadProgress = i;
            await new Promise(resolve => setTimeout(resolve, 200));
        }
        
        this.uploadedFiles.push(...files);
        this.uploadStatus = 'success';
        
        // Hide notification after 3 seconds
        setTimeout(() => {
            this.showNotification = false;
            this.uploadProgress = 0;
        }, 3000);
    },
    confirmRemoveFile(index) {
        this.showDeleteConfirm = true;
        this.deleteStatus = 'confirm';
        this.fileToDeleteIndex = index;
    },
    async confirmDelete() {
        this.deleteStatus = 'progress';
        
        // Simulate delete progress
        await new Promise(resolve => setTimeout(resolve, 1500));
        
        this.removeFile(this.fileToDeleteIndex);
        this.deleteStatus = 'success';
        
        // Close modal after showing success
        setTimeout(() => {
            this.showDeleteConfirm = false;
            this.deleteStatus = 'confirm';
            this.fileToDeleteIndex = null;
        }, 1500);
    },
    cancelDelete() {
        this.showDeleteConfirm = false;
        this.deleteStatus = 'confirm';
        this.fileToDeleteIndex = null;
    },
    removeFile(index) {
        this.uploadedFiles.splice(index, 1);
    },
    previewFile(file) {
        const reader = new FileReader();
        reader.onload = (e) => {
            this.previewFileContent = e.target.result;
            this.previewFileType = file.type.startsWith('image') ? 'image' : 'other';
            this.showFilePreview = true;
        };
        reader.readAsDataURL(file);
    },
    handleFaviconUpload(event) {
        const file = event.target.files[0];
        if (file) {
            const reader = new FileReader();
            reader.onload = (e) => {
                this.faviconPreview = e.target.result;
            };
            reader.readAsDataURL(file);
        }
    },

    removeFavicon() {
        this.faviconPreview = null;
        this.$refs.faviconInput.value = ''; // Reset the file input
    },
    handleLogoUpload(event) {
        const file = event.target.files[0];
        if (file) {
            const reader = new FileReader();
            reader.onload = (e) => {
                this.logoPreview = e.target.result;
            };
            reader.readAsDataURL(file);
        }
    },

    removeLogo() {
        this.logoPreview = null;
        this.$refs.logoInput.value = ''; // Reset the file input
    }
}
}
</script>
<style lang="">
    
</style>