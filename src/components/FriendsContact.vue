<template>
<section>
    <li>
        <h2>{{ friend.name }}</h2>
        <button @click="showdetails">Show Details</button>
        <ul v-if="detailsAreAvailable">
            <li><strong>Phone</strong>{{ friend.phone }}</li>
            <li><strong>Email</strong>{{ friend.email }}</li>
        </ul>
    </li>
</section>
</template>

<script>
export default {
    data() {
        return {
            detailsAreAvailable: false,
            friend: {
                id: "dffgkghs",
                name: "Muli2",
                phone: "45454545",
                email: "email",
            },
        };
    },
    methods: {
        showdetails() {
            this.detailsAreAvailable = !this.detailsAreAvailable;
        },
    },
};
</script>
