# Tailwind CSS @apply Directive Variable Resolution Bug

This repository demonstrates a bug where Tailwind CSS's `@apply` directive fails to correctly resolve CSS custom properties (variables) when used within the directive.

## Bug Description

When using `@apply` with a custom directive that references a CSS variable, the variable may not be resolved, leading to unexpected styling or no styling at all.  This can be particularly problematic when working with dynamic styles or themes.

## Steps to Reproduce

1. Clone this repository.
2. Open `bug.css`.
3. Observe the `.my-class` selector.  Notice it attempts to use a variable via `@apply`.
4. The expected behavior is a blue background. However, the actual behavior is the absence of the background, or an unexpected background color.

## Solution

The solution involves using the variable directly within the class definition. Avoid using `@apply` in cases with CSS variables.