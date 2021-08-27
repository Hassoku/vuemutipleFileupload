<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">FILE UPLOAD</div>

                    <div class="card-body">
                      <vue-dropzone ref="myVueDropzone" id="dropzone" :options="dropzoneOptions" v-model="files"></vue-dropzone>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {

        dropzoneOptions:[],


     data: function () {
    return {
         files : [],
      dropzoneOptions: {
          url: 'https://httpbin.org/post',
          thumbnailWidth: 150,
          maxFilesize: 0.5,
           headers: { "My-Awesome-Header": "header value" }
      }
    }
  }
    }
</script>
