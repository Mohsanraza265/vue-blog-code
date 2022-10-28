<template>
    <div>
    
        <header>
            <slot name="Header"></slot>
        </header>
        <content>
            <slot name="Content"></slot>
        </content>
        <footer>
            <slot name="Footer"><button>Click me</button></slot>
        </footer>

    </div>
</template>

<script>
    export default {
        name: "SlotChild",
       
    }
</script>