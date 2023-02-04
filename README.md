# Posthog Custom Events template for Google Tag Manager

This template will help you setup custom events for Posthog, allowing you to map event and user parameters for their respective events.

Current Version support:

1. posthog.capture events, including reset and virtual pageviews.
2. posthog.identify events, including $set and $setOnce user parameters.

## Instructions

1. Implement the Posthog Javascript SDK in Google Tag Manager using a Custom HTML tag with an All Pages trigger (or any trigger that respects your users consent wishes).
2. Implement the Posthog Custom Events template for the Google Tag Manager Template Gallery (search for `posthog`).
3. Create a new tag and select the Posthog Custom Events template.
4. Select which type of event you wish to add:
   - **Custom Event**: best used for custom events. Will track the `event` value from the dataLayer and any custom parameters defined in the tag.

