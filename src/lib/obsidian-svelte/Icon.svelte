<script lang="ts">
	import { useIcon } from ".";

	let {
		name,
		size = "md",
		accent = false,
		tooltip = ""
	}: {
		/**
		 * Specifies the icon identifier. Visit https://lucide.dev for all valid
		 * identifiers.
		 */
		name: string;
		/**
		 * Specifies the icon size.
		 */
		size?: "xs" | "sm" | "md" | "lg";
		/**
		 * Specifies whether to invert the icon color on accent backgrounds.
		 */
		accent?: boolean;
		/**
		 * Specifies the tooltip text.
		 */
		tooltip?: string;
	} = $props();
</script>

<span
	class:accent
	class:icon-xs={size === "xs"}
	class:icon-sm={size === "sm"}
	class:icon-md={size === "md"}
	class:icon-lg={size === "lg"}
	aria-label={tooltip}
	use:useIcon={name}
></span>

<style>
	span {
		color: var(--icon-color);
		fill: var(--icon-color);
		opacity: var(--icon-opacity);
		display: flex;
		flex: 0 1 auto;
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

	.accent {
		color: var(--text-on-accent);
		fill: var(--text-on-accent);
	}
</style>
