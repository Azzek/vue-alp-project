<template>
    <form>
        <div class="mb-3">
            <label for="exampleInputEmail1" class="form-label">your name, pls dont lie owo</label>
            <input type="text" class="form-control" v-model="pageName">
            <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
        </div>
        <div class="mb-3">
            <label for="exampleInputPassword1" class="form-label">type some text for me pls UwU</label>
            <input type="password" class="form-control" id="exampleInputPassword1" v-model="content">
        </div>
        <div class="mb-3 form-check">
            <input type="checkbox" class="form-check-input" id="exampleCheck1">
            <label class="form-check-label" for="exampleCheck1">Check me out</label>
        </div>
        <button class="btn btn-primary"
        @click.prevent="pageCreated({pageName, content})"
        >Submit</button>
    </form>
</template>
<script>
export default {
    props:['pageCreated'],
    data()  {
        return {
            pageName: '',
            content:  ''
        }
    }
}
</script>