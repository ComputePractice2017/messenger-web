<template>
<div class="container">
    <div class="row">
        <div class="panel panel-default">
          <div class="panel-heading">Chat</div>
          <div class="panel-body">
            <div class="container">
                <div class="row message-bubble">
                <p class="text-muted">zhe_fro:</p>
                    <span>Hello, it's me!</span>
                </div>
                <div class="row message-bubble">
                    <p class="text-muted">gaavrr:</p>
                    <span>How are you?</span>
                    </div>
                    <div class="row message-bubble">
                    <p class="text-muted">zhe_fro:</p>
                    <span>I'm fine, thank you</span>
                    </div>
                    <div class="row message-bubble">
                    <p class="text-muted">gaavrr:</p>
                    <span>What do you think about this app?</span>
                  
                </div>
            <div class="panel-footer">
                 <div class="input-group">
                  <input v-model="newmessage.mas" type="text" class="form-control">
                  <span class="input-group-btn">
                    <button  v-on:click="addnewmessage" class="btn btn-default" type="button">Send</button>
                  </span>
                </div>
            </div>
          </div>
        </div>
    </div>
    </div>
</div>
</template>
<script>
export default {
  name: 'hello',
  data () {
    return {
      messager:
      {
        'mas': '11'
      },
      newmessage:
      {
        'mas': ''
      }
    }
  },
  methods: {
    addnewmessage: function () {
      var obj = {
        'mas': ''
      }
      obj.mas = this.newmessage.mas
      this.messager.push(obj)
    }
  }
}
</script>
<style>
.message-bubble 
{
    padding: 10px 0px 10px 0px;
}

.message-bubble:nth-child(even) { background-color: #F5F5F5; }

.message-bubble > *
{
    padding-left: 10px;    
}

.panel-body { padding: 0px; }

.panel-heading { background-color: #51cfd6 !important; color: white !important; }
</style>
