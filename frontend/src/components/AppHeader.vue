<template>
    <header class="main-header">
        <div class="header-left">
            <a href="" class="menu header-link">
                <MenuSVG></MenuSVG>
                <span>Menu</span>
            </a>
        </div>
        <div class="header-middle">Points</div>
        <div class="header-right">
            <div id="search-expanded" class="search-expanded" v-on-clickaway="away">
                <input type="text" @keyup="showSearchResults" class="search-input" id="search-input" placeholder="Search"/>
                <SearchResults></SearchResults>
            </div>
            <a href="" class="search-icon header-link" @click.prevent="toggleSearch">
                <SearchSVG></SearchSVG>
            </a>
            <a href="" class="chat-icon header-link">
                <ChatSVG></ChatSVG>
            </a>
            <a href="" class="user-icon header-link">
                <span class="user-circle">
                    <span class="user-initials">HM</span>
                </span>
            </a>
        </div>
    </header>
</template>
<script>
    import { mixin as clickaway } from 'vue-clickaway'
    import MenuSVG from '@/components/svg/MenuSVG'
    import SearchSVG from '@/components/svg/SearchSVG'
    import ChatSVG from '@/components/svg/ChatSVG'
    import SearchResults from '@/components/SearchResults'

    export default { 
        name: "AppHeader",
        mixins: [ clickaway ],
        components: {
            MenuSVG,
            SearchSVG,
            ChatSVG,
            SearchResults
        },
        methods: {
            toggleSearch(e) {
                let searchInput = document.getElementById("search-input");
                searchInput.classList.toggle("search-input-active");
            },
            showSearchResults(e) {
                let searchResults = document.getElementById("search-results");
                if(!searchResults.classList.contains('search-results-active')) {
                    searchResults.classList.add("search-results-active");
                }
            },
            away() {
                let searchExpanded = document.getElementById("search-expanded");
                let searchResults = document.getElementById("search-results");
                if(searchResults.classList.contains('search-results-active')) {
                   searchResults.classList.remove("search-results-active"); 
                }       
            }
        }
    }
</script>
<style lang="scss">
    .main-header {
        height: 73px;
        background-color: #3B6FC8;
        position: relative;
        padding: 0 12px;
        text-align: center;
    }
    .header-left,
    .header-right {
        position: absolute;
        top: 12px;
    }
    .header-left {
        /* left: 12px; */
    }
    .header-middle {
        font-size: 24px;
        color: #fff;
        position: relative;
        top: 22px;

        @media only screen and (max-width: 1150px) {
            display: none;
        }
    }
    .header-right {
        right: 12px;
    }
    .menu {
        text-decoration: none;
        color: #fff;
        height: 52px;
        display: inline-block;
        opacity: 1;
        transition: opcaity .35s;

            &:hover {
                opacity: .8;
            }

        span {
            font-size: 24px; 
            vertical-align: top;
            position: relative;
            top: 10px;
        }
    }
    .search-expanded {
        display: inline-block;
        position: relative;
        bottom: 10px;
        .search-input {
            border: none;
            /* border-bottom: 1px solid black; */
            height: 27px;
            font-size: 18px;
            width: 0;
            opacity: 0;
            transition: width .35s, opacity .35s;
            /* border-radius: 13px; */
            padding: 5px 10px;
            /* display: none; */
            &:active,
            &:focus {
                outline: none;
            }
            
        }
        .search-input-active {
            width: 300px ;
            opacity: 1;
        }
        .search-results {
            width: 310px;
            border-top: 1px solid rgba(0,0,0,0.05);
            background: #fff;
            position: absolute;
            padding: 5px;
            top: 36px;
            height: 0;
            opacity: 0;
            pointer-events: none;
            /* height: 100px; */
            /* display: none; */
            -webkit-box-shadow: 0px 5px 5px 0px rgba(0,0,0,0.25);
            -moz-box-shadow: 0px 5px 5px 0px rgba(0,0,0,0.25);
            box-shadow: 0px 5px 5px 0px rgba(0,0,0,0.25); 
        }
        .search-results-active {
            height: auto;
            opacity: 1;
            pointer-events: auto;
        }
    }
    .search-icon {
        width: 32px;
        height: 32px;
        display: inline-block;
        padding: 10px 10px;

        opacity: 1;
        transition: opcaity .35s;

        &:hover {
            opacity: .8;
        }

        @media (max-width: 650px) {
            display: none ;
        }
    }
    .chat-icon {
        padding: 10px 20px 10px 10px;
        opacity: 1;
            transition: opcaity .35s;

            &:hover {
                opacity: .8;
            }
    }
    .user-icon {
        width: 48px;
        height: 48px;
        border: 1px solid #fff;
        display: inline-block;
        position: relative;
        bottom: 15px;
        text-decoration: none;
        background-color: #28548A;
        opacity: 1;
            transition: opcaity .35s;

            &:hover {
                opacity: .8;
            }
        
        .user-circle {
            color: #fff;
            background-color: #3B6FC8;
            display: inline-block;
            width: 100%;
            height: 100%;
            border-radius: 50%;
            .user-initials {
                font-size: 28px;
                position: relative;
                top: 5px;
            }
        }
    }
    #search-icon-svg {
       pointer-events: none;
       position: relative;
       z-index: 10;
    }
    .results-header {
        display: flex;
        
        .results-filter {
            flex: auto;
            text-decoration: none;
            padding: 10px 0; 
        }
    }
    .results-body {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-gap: 5px;
        .search-result {
            text-decoration: none;
            border: 1px solid rgba(0,0,0,0.25);
            align-self: center;
            text-align: left;
            padding: 20px 10px;
        }
        .search-category,
        .search-name {
            display: block;
        }
        .search-category {
            color: #133862;
            font-size: 12px;
            opacity: .6;
        }
    }
    .header-link {
        position: relative;
        z-index: 100;
    }

    .chat-icon,
    .user-icon {
        display: inline-block;
    }

    .header-link:after {
       content: ""; 
        position: absolute; 
        top: 0; 
        left: 0; 
        width: 100%;
        height: 100%;
    }
    .st0{fill:#FFFFFF;}
</style>