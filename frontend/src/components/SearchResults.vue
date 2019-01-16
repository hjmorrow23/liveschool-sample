<template>
    <div class="search-results" id="search-results">
        <div class="results-header">
            <a href="" class="results-filter" @click.prevent="resetSearch">All</a>
            <a href="" class="results-filter" @click.prevent="filterCategory">Roster</a>
            <a href="" class="results-filter" @click.prevent="filterCategory">Student</a>
            <a href="" class="results-filter" @click.prevent="filterCategory">Reports</a>
        </div>
        <div class="results-body">
            <a href="" class="search-result" v-for="item in searchItems">
                <span class="search-category">{{item.category}}</span>
                <span class="search-name">{{item.name}}</span>
            </a>
        </div>
    </div>
</template>

<script>
    export default {
        name: "SearchResults",
        data() {
            return {
                startSearchItems: [
                    {
                        name: "Jane Doe",
                        category: "Student"
                    },
                    {
                        name: "John Doe",
                        category: "Student"
                    },
                    {
                        name: "3rd Grade",
                        category: "Roster"
                    },
                    {
                        name: "Kindergarten",
                        category: "Roster"
                    },
                    {
                        name: "September Points",
                        category: "Reports"
                    },
                    {
                        name: "October Points",
                        category: "Reports"
                    }
                ],
                searchItems: []
            }
        },
        methods: {
            filterCategory(e) {
                let clickedCat = e.target.textContent;
                
                this.searchItems = this.startSearchItems.filter(item => item.category === clickedCat);
            },
            resetSearch(e) {
                this.searchItems = this.startSearchItems;
            }
        },
        created() {
            this.resetSearch();
        }
    }
</script>

<style scoped>

</style>