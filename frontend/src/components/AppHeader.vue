<template>
    <header class="main-header">
        <div class="header-left">
            <a href="" class="menu header-link">
                <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
                    width="52px" height="52px" viewBox="0 0 13.971 13.969" enable-background="new 0 0 13.971 13.969" xml:space="preserve">
                    <path fill="none" stroke="#FFFFFF" stroke-width="1.0909" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="
                        M2.945,0.545h8.07c1.319,0,2.38,1.06,2.38,2.38v8.121c0,1.31-1.061,2.379-2.38,2.379h-8.07c-1.311,0-2.37-1.069-2.37-2.379V2.925
                        C0.575,1.605,1.635,0.545,2.945,0.545z"/>
                    <line fill="none" stroke="#FFFFFF" stroke-width="0.5455" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" x1="3.155" y1="3.615" x2="10.844" y2="3.615"/>
                    <line fill="none" stroke="#FFFFFF" stroke-width="0.5455" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" x1="3.155" y1="6.715" x2="10.844" y2="6.715"/>
                    <line fill="none" stroke="#FFFFFF" stroke-width="0.5455" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" x1="3.155" y1="9.805" x2="10.844" y2="9.805"/>
                </svg>
                <span>Menu</span>
            </a>
        </div>
        <div class="header-middle">Points</div>
        <div class="header-right">
            <div class="search-expanded" v-on-clickaway="away">
                <input type="text" @keyup="showSearchResults" class="search-input" id="search-input" placeholder="Search"/>
                <div class="search-results" id="search-results">
                    <div class="results-header">
                        <a href="" class="results-filter">All</a>
                        <a href="" class="results-filter">Roster</a>
                        <a href="" class="results-filter">Student</a>
                        <a href="" class="results-filter">Reports</a>
                    </div>
                    <div class="results-body">
                        <a href="" class="search-result">
                            <span class="search-category">Student</span>
                            <span class="search-name">Jane Doe</span>
                        </a>
                        <a href="" class="search-result">
                            <span class="search-category">Student</span>
                            <span class="search-name">John Doe</span>
                        </a>
                        <a href="" class="search-result">
                            <span class="search-category">Roster</span>
                            <span class="search-name">3rd Grade</span>  
                        </a>
                        <a href="" class="search-result">
                            <span class="search-category">Roster</span>
                            <span class="search-name">Kindergarten</span> 
                        </a>
                        <a href="" class="search-result">
                            <span class="search-category">Report</span>
                            <span class="search-name">September Points</span>   
                        </a>
                        <a href="" class="search-result">
                            <span class="search-category">Report</span>
                            <span class="search-name">October Points</span>
                        </a>
                    </div>
                </div>
            </div>
            <a href="" class="search-icon header-link" @click.prevent="toggleSearch">
                <svg version="1.1" id="search-icon-svg" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="-255 347 100 100" style="enable-background:new -255 347 100 100;" xml:space="preserve">
                    <g>
                        <path class="st0" d="M-242.5,385.2c0-12.9,11.2-23.5,24.9-23.5c13.8,0,25,10.6,25,23.5c0,13-11.2,23.5-25,23.5
                            C-231.3,408.8-242.5,398.2-242.5,385.2z M-157.2,433.5l-29.7-27.9c4.3-5.8,6.8-12.8,6.8-20.4c0-19.5-16.8-35.3-37.5-35.3
                            c-20.7,0-37.5,15.8-37.5,35.3c0,19.5,16.8,35.3,37.5,35.3c8.1,0,15.6-2.4,21.7-6.5l29.6,27.9c2.7,2.6,7,2.8,9.5,0.4
                            C-154.2,440.1-154.5,436.1-157.2,433.5z"/>
                    </g>
                </svg>
            </a>
            <a href="" class="chat-icon header-link">
                <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
                    width="32px" height="32px" viewBox="0 0 15.82 15.82" enable-background="new 0 0 15.82 15.82" xml:space="preserve">
                    <g>
                        <path fill="#FFFFFF" d="M15.795,6.589c0.3-2.64-2.09-5.08-5.35-5.45c-1.99-0.23-3.84,0.38-5.05,1.48c0.27-0.02,0.54-0.04,0.81-0.04
                            c1.62,0,3.17,0.48,4.37,1.36c1.27,0.93,2.06,2.24,2.22,3.68c0.15,1.28-0.22,2.59-1.03,3.7c1.67,1.28,3.2,0.93,2.85,0.66
                            c-0.99-0.76-1.2-1.51-1.14-2.09C14.745,9.149,15.635,7.979,15.795,6.589z"/>
                        <path fill="#FFFFFF" d="M11.815,7.739c-0.28-2.41-2.71-4.15-5.61-4.15c-0.27,0-0.55,0.01-0.83,0.04c-3.26,0.37-5.65,2.81-5.35,5.45
                            c0.16,1.39,1.04,2.56,2.32,3.3c0.06,0.59-0.15,1.33-1.14,2.09c-0.16,0.12,0.06,0.26,0.49,0.26c0.68,0,1.9-0.33,3.07-1.56
                            c0.28,0.04,0.58,0.06,0.88,0.06c0.27,0,0.55-0.02,0.83-0.05C9.725,12.809,12.115,10.369,11.815,7.739z"/>
                    </g>
                </svg>
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
    export default { 
        name: "AppHeader",
        mixins: [ clickaway ],
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
            }
        }
    }
</script>
<style lang="scss">
    .main-header {
        height: 73px;
        background-color: #3B6FC8;
        position: relative;
    }
    .header-left,
    .header-right {
        position: absolute;
        top: 12px;
    }
    .header-left {
        left: 12px;
    }
    .header-middle {
        font-size: 24px;
        color: #fff;
        position: relative;
        top: 22px;
    }
    .header-right {
        right: 12px;
    }
    .menu {
        text-decoration: none;
        color: #fff;
        height: 52px;
        display: inline-block;
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
            /* height: 100px; */
            /* display: none; */
            -webkit-box-shadow: 0px 5px 5px 0px rgba(0,0,0,0.25);
            -moz-box-shadow: 0px 5px 5px 0px rgba(0,0,0,0.25);
            box-shadow: 0px 5px 5px 0px rgba(0,0,0,0.25); 
        }
        .search-results-active {
            height: auto;
            opacity: 1;
        }
    }
    .search-icon {
        width: 32px;
        height: 32px;
        display: inline-block;
        padding: 10px 10px;
    }
    .chat-icon {
        padding: 10px 20px 10px 10px;
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
        display: inline-block;
        z-index: 100;
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