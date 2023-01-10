<template>
    <div class="form-group">
        <label :for="id" class="form-label">{{title}}</label>
            <slot></slot>
        <small :id="idHelp" class="form-text text-muted">{{textHelp}}</small>
    </div>
</template>

<script>
    export default {
        props: ['id', 'title', 'idHelp', 'textHelp']
    }

</script>
