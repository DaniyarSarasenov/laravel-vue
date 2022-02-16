<template>
    <div class="container">
        <div class="row page-content">
            <div class="col-md-12" style="padding: 0px 20px">
                <form class="product-form">
                    <div class="edit-image-wrapper mt-10">
                        <div class="edit-image-preview" v-if="preview">
                            <img :src="preview" class="preview-image">
                        </div>

                        <div class="edit-image-selector">
                            <div class="file-button">
                                <label for="select-file"><i class="fa fa-camera"></i></label>
                                <input type="file" accept="image/*" id="select-file" @change="previewImage"/>
                            </div>
                        </div>
                    </div>

                    <div class="edit-textarea mt-10">
                        <textarea ></textarea>
                    </div>

                    <div class="edit-location mt-10">
                        
                    </div>

                    <div class="edit-time mt-10">

                    </div>

                    <div class="col-md-12 mt-10 mb-10">
                        <button class="btn btn-black" @click="this.$router.push('/myproduct')">Update</button>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "EditProduct",
    data() {
        return {
            preview: null,
            image: null,
        }
    },
    created() {
    },
    methods: {
        previewImage: function(event) {
            var input = event.target;
            if (input.files) {
                var reader = new FileReader();
                console.log(reader);
                reader.onload = (e) => {
                    console.log("preview--", e);
                    this.preview = e.target.result;
                }
                this.image = input.files[0];

                console.log(this.image);
            }
        }
    }
}
</script>
