<script>
    export default {
        data(){
            return {
                domain       : document.location.host,
                cookieName   : 'my_cookie_consent',
                expiration   : (365 * 20),
                hasConcented : false,
                showDialog   : true,
            }
        },

        beforeMount(){
            if (this.cookieExists()) {
                this.showDialog = false
            }
        },

        methods:{
            consentWithCookies() {
                this.setCookie(this.cookieName, 1, this.expiration)
                this.showDialog = false
            },

            cookieExists() {
                return (document.cookie.split('; ').indexOf(this.cookieName + '=' + 1) !== -1)
            },

            setCookie() {
                const date = new Date();
                date.setTime(date.getTime() + (this.expiration * 24 * 60 * 60 * 1000));
                document.cookie = this.cookieName + '=1'
                    + ';expires=' + date.toUTCString()
                    + ';domain=' + this.domain
                    + ';path=/;secure'
                    + 'lax';
            },
        },
    }
</script>

<template>
    <div v-if="showDialog" class="fixed bottom-0 left-0 right-0 inset-x-0 pb-2 z-50">
        <div class="w-full max-w-7xl mx-auto px-6">
            <div class="p-2 rounded-lg bg-black border border-white">
                <div class="grid grid-flow-col place-items-center justify-between flex-wrap">
                    <div class="w-full flex-1 items-center hidden md:block">
                        <p class="ml-3 text-white cookie-consent__message">
                            This app uses cookies to track and enhance your experience on this site.
                        </p>
                    </div>
                    <div class="mt-2 flex-shrink-0 w-full sm:mt-0 sm:w-auto">
                        <button
                            @click="consentWithCookies"
                            class="cursor-pointer flex items-center justify-center px-4 py-2 rounded-md text-sm font-medium text-black bg-white">
                            Allow cookies
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
