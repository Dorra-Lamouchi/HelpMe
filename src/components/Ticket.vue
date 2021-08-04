<template>
<div class="inner-block2">
    <div class="vue-tempalte">
        <form>
            <center>
            <h3>Vous n'avez pas trouvé ce que vous voulez? Créer un ticket maintenant!</h3>
            <br>
            <h5> Nous sommes très réactifs dans notre service. Vous recevrez une réponse dans les 72 heures. </h5>
            </center>

            <br><br>
            <div class="form-group">
                <label>Subject</label>
                <input type="email" class="form-control form-control-lg" />
            </div>

            <div class="form-group">
                <label> Type </label>
                <b-dropdown
                    text="Block Level Dropdown Menu"
                    block
                    variant="primary"
                    class="m-2"
                    menu-class="w-100"
                >
                    <b-dropdown-item href="#">Action1</b-dropdown-item>
                    <b-dropdown-item href="#">Action2</b-dropdown-item>
                    <b-dropdown-item href="#">Action3</b-dropdown-item>
                </b-dropdown>
            </div>

            <div class="form-group">
                <label>Description</label>
                <input type="password" class="form-control form-control-lg" />
            </div>

            <div class="form-group">
                <label>File
                <input type="file" id="file" ref="file" v-on:change="handleFileUpload()"/>
                </label>
            </div>

            <button type="submit" class="btn btn-dark btn-lg btn-block">Send</button>
            
        </form>
    </div>
</div>
</template>

<script>
    export default {
        data() {
            return {
                file: ''
            }
        },
        methods: {
            handleFileUpload(){
                this.file = this.$refs.file.files[0];
            }
        }
    }
</script>