<template>
    <div class="container mt-3">
        <div class="row">
            <div class="col">
                <p class="h3 text success fw-bold">View Contact</p>
                <p class="fs-italic">View the fields here</p>
            </div>
        </div>
    </div>>
    <div class="container align-items-center">
        <div class="row">
            <div class="col-md-4">
            <img src="https://image.shutterstock.com/image-vector/thin-line-user-icon-on-260nw-519039097.jpg" alt="" class="contact-img-big">
            </div>
            <div class="col-md-6">
              <ul class="list-group">
                <li class="list-group-item">Name:<span class="fw-bold">Name</span> </li>
                <li class="list-group-item">Email<span class="fw-bold">Email</span> </li>
                <li class="list-group-item">Mobile:<span class="fw-bold">Mobile</span> </li>
                <li class="list-group-item">PhotoUrl:<span class="fw-bold">PhotoUrl</span> </li>
                <li class="list-group-item">Role:<span class="fw-bold">Role</span> </li>
              </ul>
            </div>
        </div>
        <div class="row mt-3">
            <div class="col">
                <router-link to="/" class="btn btn-success">
                <i class="fa fa-arrow-alt-circle-left"></i>
                Back</router-link>
            </div>
        </div>
    </div>
</template>

<script>
export default {
   name :'ViewContact'
}
</script>

<style scoped>

</style>