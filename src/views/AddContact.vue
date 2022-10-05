<template>
    <div class="container mt-3">
        <div class="row">
            <div class="col">
                <p class="h3 text success fw-bold">Add Contact</p>
                <p class="fs-italic">Add the fields here</p>
            </div>
        </div>
    </div>>
    <div class="container mt-3">
        <div class="row">
            <div class="col-md-4">
             <form>
                 <div class="mb-2">
                     <input type="text" class="form-control" placeholder="Name">
                 </div>
                  <div class="mb-2">
                     <input type="text" class="form-control" placeholder="PhotoUrl">
                 </div>
                  <div class="mb-2">
                     <input type="email" class="form-control" placeholder="Email">
                 </div>
                  <div class="mb-2">
                     <input type="number" class="form-control" placeholder="MobileNo">
                 </div>
                  <div class="mb-2">
                     <input type="text" class="form-control" placeholder="Role">
                 </div>
                  <div class="mb-2">
                     <input type="submit" class="btn btn-success" value="Create">
                 </div>
             </form>
            </div>
            <div class="col-md-4">
                <img src="https://image.shutterstock.com/image-vector/thin-line-user-icon-on-260nw-519039097.jpg" alt="" class="contact-img">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name : "AddContact"
}
</script>

<style scoped>

</style>