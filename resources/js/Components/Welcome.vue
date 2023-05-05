<script setup>
import ApplicationLogo from '@/Components/ApplicationLogo.vue';
</script>

<template>
    <div>
        <div class="p-6 lg:p-8 bg-white border-b border-gray-200">

            <div v-if="$page.props.user.permissions.includes('read articles')">
                <button type="button" 
                    class="inline-flex items-center rounded-md border border-transparent 
                        bg-indigo-600 px-4 
                        py-2 text-sm font-medium text-white shadow-sm 
                        hover:bg-indigo-700 
                        focus:outline-none 
                        focus-ring-2 
                        focus:ring-indigo-500 
                        focus:ring-offset-2"
                >Read article</button>
            </div>

            <div class="mt-4" v-if="$page.props.user.permissions.includes('write articles')">
                <button type="button" 
                    class="inline-flex items-center rounded-md border border-transparent 
                        bg-indigo-100 
                        px-4 py-2 text-sm font-medium text-indigo-700 shadow-sm 
                        hover:bg-indigo-200 
                        focus:outline-none 
                        focus-ring-2 
                        focus:ring-indigo-500 
                        focus:ring-offset-2"
                >Write article</button>
            </div>

            <div class="mt-4" v-if="$page.props.user.permissions.includes('edit articles')">
                <button type="button" 
                    class="inline-flex items-center rounded-md border 
                        border-gray-300 
                        bg-white px-4 
                        py-2 text-sm font-medium text-gray-700 shadow-sm 
                        hover:bg-gray-50 
                        focus:outline-none 
                        focus-ring-2 
                        focus:ring-indigo-500 
                        focus:ring-offset-2"
                >Edit article</button>
            </div>
            <div class="mt-4" v-if="$page.props.user.permissions.includes('delete articles')">
                <button type="button" 
                    class="inline-flex items-center rounded-md border border-transparent 
                        bg-red-600 px-4 
                        py-2 text-sm font-medium text-red-50 shadow-sm 
                        hover:bg-red-700 
                        focus:outline-none 
                        focus-ring-2 
                        focus:ring-red-500 
                        focus:ring-offset-2"
                >Delete article</button>
            </div>
            
            <!--<div class="mt-4">
                {{ $page.props.user.permissions.includes('delete articles') }}
                {{ $page.props }}
            </div>-->

        </div>
    </div>
</template>
