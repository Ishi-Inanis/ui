<script>
  import { Meta, Story, Template } from '@storybook/addon-svelte-csf';
  import Button from '../lib/Button.svelte';
</script>

<Meta title="Components/Button" component={Button} argTypes={{
  color: {
    control: { type: 'select' },
    options: ['red', 'amber', 'black', 'white']
  }
}}/>

<Template let:args>
  <Button {...args}>Text</Button>
</Template>

<Story name="just button"/>

<Story name="red rounded" args={{rounded: true}}/>
<Story name="red blurry" args={{blurry: true, translucent: true}}/>
<Story name="red large" args={{large: true}}/>
<Story name="red translucent" args={{translucent: true}}/>

<Story name="amber rounded" args={{color: 'amber', rounded: true}}/>
<Story name="amber blurry" args={{color: 'amber', blurry: true, translucent: true}}/>
<Story name="amber large" args={{color: 'amber', large: true}}/>
<Story name="amber translucent" args={{color: 'amber', translucent: true}}/>

<Story name="black rounded" args={{color: 'black', rounded: true}}/>
<Story name="black blurry" args={{color: 'black', blurry: true, translucent: true}}/>
<Story name="black large" args={{color: 'black', large: true}}/>
<Story name="black translucent" args={{color: 'black', translucent: true}}/>

<Story name="white rounded" args={{color: 'white', rounded: true}}/>
<Story name="white blurry" args={{color: 'white', blurry: true, translucent: true}}/>
<Story name="white large" args={{color: 'white', large: true}}/>
<Story name="white translucent" args={{color: 'white', translucent: true}}/>