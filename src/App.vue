<template>
  <div id="app">
    <md-card>
        <md-card-header>
        <div class="md-title">
        Vue.js Practice App 01

        </div>
        <div class="md-subhead">
        by: Austin Rutledge

        </div>
        
        </md-card-header>
        
        <md-card-content>
        <md-button class="md-raised md-primary" v-on:click="fillTable()">
        Fill Table
          
        </md-button>

        <md-button class="md-raised md-primary" v-on:click="clearTable()">
        Clear Table
          
        </md-button>

        </md-card-content>
        <md-table>
        <md-table-header>

        	<md-table-row>
        		<md-table-head>First Name</md-table-head>
        		<md-table-head>Last Name</md-table-head>
        		<md-table-head>Email</md-table-head>
        		

       		</md-table-row>

        </md-table-header>
        <md-table-body>
        <md-table-row v-for="contact in contacts">
        

        <md-table-cell>{{contact.firstname}}</md-table-cell>
        <md-table-cell>{{contact.lastname}}</md-table-cell>
        <md-table-cell>{{contact.email}}</md-table-cell>
        </md-table-row>
        </md-table-body>

        </md-table>
    </md-card>
  </div>
</template>
<script>
	import Hello from './components/Hello'

	export default {
		name:'app',
		data: function(){
			return{
				contacts: []
			}
		},
		methods: {
			fillTable: function(){
				this.contacts.push({firstname: 'Austin', lastname: 'Rutledge', email: 'vark47@aol.com'});

				this.contacts.push({firstname: 'Austin', lastname: 'Rutledge', email: 'vark47@aol.com'});

				this.contacts.push({firstname: 'Austin', lastname: 'Rutledge', email: 'vark47@aol.com'});
			},
			clearTable: function(){
				this.contacts.splice(0,this.contacts.length);
			}
		}
	}

</script>


<style>
#app {
 
  margin-top: 60px;
  margin-left: 30px;
  margin-right: 30px;

  }
</style>
