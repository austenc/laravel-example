<template>
    <div class="container">
        <div class="row">
            <div class="col-md-8 col-md-offset-2">
                <div class="panel panel-default">
                    <div class="panel-heading">Example Component</div>

                    <div class="panel-body">
                        I'm an example component!
                        <br>
                        The version is {{ version }} -- this is from lumen
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                version: 0
            }
        },
        created() {
            axios.get('http://lumen-example.dev').then(function (response) {
                this.version = response.data;
            }.bind(this));
        }
    }
</script>
