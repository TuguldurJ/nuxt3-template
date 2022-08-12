<script setup lang="ts">
const color = useColorMode()
</script>

<template>
    <div class="text-gray-400 flex gap-4 relative z-50 w-full flex-none text-sm font-semibold leading-6">
        <nav class="mx-auto max-w-container w-full">
            <div v-if="color.value === 'system'">
                <div class="p-4 mx-auto max-w-7xl lg:px-8 w-full">
                    <div class="animate-pulse flex space-x-4">
                        <div class="rounded-full bg-slate-200 h-10 w-10"></div>
                        <div class="flex-1 py-1 space-x-4 space-y-1">
                            <div class="h-2 bg-slate-200 rounded"></div>
                            <div class="space-y-1">
                                <div class="grid grid-cols-3 gap-4">
                                    <div class="h-2 bg-slate-200 rounded col-span-2"></div>
                                    <div class="h-2 bg-slate-200 rounded col-span-1"></div>
                                </div>
                                <div class="h-2 bg-slate-200 rounded"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <HeaderLight v-else-if="color.value === 'light'"></HeaderLight>
            <HeaderDark v-else></HeaderDark>
        </nav>
    </div>
</template>
