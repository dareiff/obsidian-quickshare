<script lang="ts">
	import { useIcon } from ".";

	let {
		icon,
		size = "md",
		active = false,
		tooltip = "",
		nopadding = false,
		disabled = false,
		onclick,
		onkeypress
	}: {
		/**
		 * Specifies the icon identifier. Visit https://lucide.dev for all valid
		 * identifiers.
		 */
		icon: string;
		/**
		 * Specifies the width and height of the icon in pixels. Defaults to 16px.
		 */
		size?: "xs" | "sm" | "md" | "lg";
		/**
		 * Specifies whether icon is active.
		 */
		active?: boolean;
		/**
		 * Specifies the tooltip.
		 */
		tooltip?: string;
		/**
		 * Specifies whether to remove the default padding.
		 */
		nopadding?: boolean;
		disabled?: boolean;
		onclick?: (event: MouseEvent) => void;
		onkeypress?: (event: KeyboardEvent) => void;
	} = $props();
</script>

<div
	class="clickable-icon"
	class:nopadding
	class:is-active={active}
	class:icon-xs={size === "xs"}
	class:icon-sm={size === "sm"}
	class:icon-md={size === "md"}
	class:icon-lg={size === "lg"}
	aria-label={tooltip}
	role="button"
	tabindex="0"
	use:useIcon={icon}
	{onclick}
	{onkeypress}
	{disabled}
></div>

<style>
	.nopadding {
		padding: 0;
	}
	.icon-xs {
		--icon-size: var(--icon-xs);
		--icon-stroke: var(--icon-xs-stroke-width);
	}
	.icon-sm {
		--icon-size: var(--icon-s);
		--icon-stroke: var(--icon-s-stroke-width);
	}
	.icon-md {
		--icon-size: var(--icon-m);
		--icon-stroke: var(--icon-m-stroke-width);
	}
	.icon-lg {
		--icon-size: var(--icon-l);
		--icon-stroke: var(--icon-l-stroke-width);
	}
</style>
