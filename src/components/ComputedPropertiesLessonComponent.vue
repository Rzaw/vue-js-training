<template>
  <h1>Computed Properties Lesson</h1>
  
  <h2>Using string template litterals</h2>
  <p>Full name - {{firstName}} {{lastName}}</p>
  <code>Full name - <span v-pre>{{firstName}} {{lastName}}</span></code>

  <h2>Using computed property</h2>
  <p>Full name - {{fullName}}</p>
  <code>Full name - <span v-pre>{{fullName}}</span></code><br>

    <table>
        <thead>
            <tr>
                <th v-for="(value, key) in cart[0]" :key="key">{{key}}</th>
            </tr>
        </thead>
        <tbody>
            <!-- Looping througt cart items -->
            <tr v-for="(item, index) in cart" :key="index">
                <!-- Loooping throught cart item propery -->
                <td v-for="(value) in item" :key="value.id">{{value}}</td>
            </tr>
        </tbody>
    </table>

  <p>Total - {{ cart.reduce((total, curr) => (total += curr.price), 0) }}</p>
  <p>Computed Total - {{ total }}</p>
    <button @click="addRandomButton">Add random item</button>
</template>

<script>
export default {
    name: 'ComputedPropertiesLessonComponent',
    data() {
        return {
            firstName: 'Matijs',
            lastName: 'Lode',
            cart: [
                {
                    id: 1,
                    title: 'TV',
                    price: 100
                },
                {
                    id: 2,
                    title: 'Phone',
                    price: 200
                },
                {
                    id: 3,
                    title: 'Laptop',
                    price: 300
                }
            ],
            items: [
                'Coffee Machine',
                'Laptop',
                'Monitor',
                'Speakers',
                'Wireless Headphones',
                'TV',
                'Phone',
                'Smart Watch'
            ]
        }
    },
    methods: {
        addRandomButton(){
            // Random selection from list
            var item = this.items[this.getRandomInt(0, this.items.length - 1)];

            // Random selection from price range (100 - 900)
            var price = this.getRandomInt(100, 900);

            // Getting the last item from cart and +1 id
            let lastCartItem = this.cart[this.cart.length - 1];

            this.cart.push({
                id: lastCartItem.id + 1,
                title: item,
                price
            })
        },
        getRandomInt(min, max)
        {
            min = Math.ceil(min);
            max = Math.floor(max);
            return Math.floor(Math.random() * (max - min) + min);
        }
    },
    computed: {
        fullName()
        {
            return `${this.firstName} ${this.lastName}`
        },
        total()
        {
            return this.cart.reduce((total, curr) => (total += curr.price), 0);
        }
    }
}
</script>

<style>

</style>