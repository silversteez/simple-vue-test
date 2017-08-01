<template>
    <div class="body">
        <div>
            <button v-on:click="toggleUsers">Toggle Users</button>
        </div>
        <user-list-item v-if="showUsers"
                        v-on:sayName="sayName(user)"
                        v-for="(user, index) in users" class="user-item"
                        :key="index"
                        :user="user"
                        :index="index"
                        :selectedUserIndex="selectedUserIndex">
        </user-list-item>
        <div>
            <button v-on:click="incrementIndex">Select Next User</button>
        </div>
    </div>
</template>

<script>
    import userListItem from './user-list-item.vue';

    export default {
        components: {
            userListItem
        },
        data() {
            return {
                users: [
                    {name: 'john'},
                    {name: 'mary'},
                    {name: 'steve'}
                ],
                selectedUserIndex: 0,
                showUsers: true
            };
        },
        methods: {
            incrementIndex() {
                if (this.selectedUserIndex >= this.users.length-1) {
                    this.selectedUserIndex = 0;
                    return;
                }
                this.selectedUserIndex++;
            },
            toggleUsers() {
                this.showUsers = !this.showUsers;
            },
            sayName(user) {
                console.log(user);
                alert(user.name);
            }
        }
    }
</script>

<style>
    .user-item {
        color: green;
    }
</style>
