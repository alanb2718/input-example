<script lang="ts">
  import { Input, Label, P } from 'flowbite-svelte';

  let textValue = $state('');
  let keystrokes = $state(0);

  function increment() {
    keystrokes++;
  };
</script>

<div>
  <Label>
    Enter some text:
    <Input type="text" bind:value={textValue} oninput={increment} />
  </Label>    
  
  <P>Keystrokes: {keystrokes.toString()}</P>
  <P>Text value: {textValue}</P>
</div>
