<template>
    <app-layout title="Dashboard">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Módulo de notas
            </h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="md:grid md:grid-cols-3 md:gap-6">
                    <div class="md:col-span-1">
                        <div class="px-4 sm:px0">
                            <h3 class="text-lg text-gray-900">Detalle una nota</h3>
                            <p class="text-sm text-gray-600">{{note.excerpt}}</p>
                        </div>
                    </div>
                    <div class="md:col-span-2 mt-5 md:mt-8">
                        <div class="shadow bg-white rounded-md p-4">
                            <p>{{note.content}}</p>
                            <hr class="my-6">
                            <Link :href="route('notes.index')">
                                Volver
                            </Link>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </app-layout>
</template>

<script>
    // import { defineComponent } from 'vue'
    import AppLayout from '@/Layouts/AppLayout.vue'
    import {Link} from '@inertiajs/inertia-vue3'

    export default {
        components: {
            AppLayout,
            Link
        },
        props:{
            note: Object,
        }
    }
</script>
