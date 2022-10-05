<template>
    <div class="container mt-3"> 
        <div class="row">
            <div class="col">
                <p class="h3 text-success fw-bold">Contact Managaer
                    <router-link to="/contacts/add" class="btn btn-success btn-sm">
                    <i class="fa fa-plus-circle"> New
                    </i>
                    </router-link>
                </p>
                <p class="fst-italic">welcome to contactmanager have wonderful evening session</p>
                <form >
                    <div class="row">
                        <div class="col-md-5">
                            <div class="row">
                                <div class="col">
                                    <input type="text" class="form-control" placeholder="search name">

                                </div>
                                <div class="col">
                                  <input type="submit" class="btn btn-dark">
                                </div>
                            </div>

                        </div>
                    </div>
                </form>
            </div>
        </div>
    </div>
    <div class="container mt-3" v-if="contacts.length > 0">
        <div class="row">
            <div class="col-md-6" v-for="contact of contacts" :key="contact">
                <div class="card my-2 list-group-item-success shadow-lg"  >
                    <div class="card-body" >
                        <div class="row align-items-center">
                            <div class="col-sm-4">
                                <img v-bind:src="contact.photourl" class="contact-img">
                            </div>
                            <div class="col-sm-7">
                                <ul class="list-group">
                                    <li class="list-group-item">Name:<span class="fw-bold">{{contact.name}}</span> </li>
                                    <li class="list-group-item">Email:<span class="fw-bold">{{contact.Email}}</span> </li>
                                    <li class="list-group-item">Mobile:<span class="fw-bold">{{contact.mobile}}</span> </li>
                                </ul>
                            </div>
                            <div class="col-sm-1 d-flex flex-column justify-content-center align-items-center">
                                <router-link to = '/contacts/view/:contactId' class="btn btn-warning my-1">
                                <i class="fa fa-eye"></i>
                                </router-link>
                                <router-link to = '/contacts/edit/:contactId' class="btn btn-primary my-1">
                                <i class="fa fa-pen"></i>
                                </router-link>
                                <button class="btn btn-danger my-1">
                                    <i class="fa fa-trash"></i>
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import ContactService from '../services/ContactService'

export default {
    name : 'ContactManager',

    data: function(){
        return{
            contacts : [],
            errormessage : null
        }

    },
    created :  async function(){
        try {
            let response = await ContactService.getAllContacts()
            this.contacts = response.data
            console.log(this.contacts)
            
        } catch (error) {
            this.errormessage=error
        }

    },
    methods :{
    
    }
}
</script>

<style >

</style>