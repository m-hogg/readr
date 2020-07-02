<template>
    <div class="flex flex-col justify-center p-5 h-64 bg-white rounded-md">
        <button
            @click="$emit('add')"
            class="focus:outline-none mx-4 mb-2 py-3 px-3 bg-green-400 rounded-md"
        >
            Add
        </button>
        <button
            @click="$emit('filter')"
            class="focus:outline-none mx-4 my-2 py-3 px-3 bg-orange-400 rounded-md"
        >
            Filter
        </button>
        <button
            @click="$emit('edit')"
            class="focus:outline-none mx-4 mt-2 py-3 px-3 bg-indigo-400 rounded-md"
        >
            Edit
        </button>
    </div>
</template>