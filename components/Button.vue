<template>
  <button :class="cssClasses()"><slot></slot></button>
</template>

<script>
export default {
	name: 'MyButton',
	props: {
		big: {
			type: Boolean,
			default: false
		}
	},
	methods: {
		cssClasses() {
			return {
				[`big-button`]: this.big
			};
		}
	}
};
</script>


<style lang="scss">
@import '../design-tokens/colors.scss';

button {
	font-size: inherit;
	padding: 0.3em 0.6em;
	border: none;
	background-color: $main-color;
}

.big-button {
	font-size: 24px;
	padding: 1em 2em;
}
</style>


<styleguide-doc>
### MyButton is used for demo purposes
</styleguide-doc>


<styleguide-states>
[{
    name: "Default",
    content: "I am a button"
},
{
    name: "Big",
    content: "I am a big button",
    data: {
        props: {
            big: true
        }
    }
}]
</styleguide-states>