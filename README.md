# Posthog Custom Events template for Google Tag Manager
This template will help you setup custom events for Posthog, allowing you to map event and user parameters for their respective events.

> **⚠️** This template **will only work when Posthog’s snippet is implemented** either hardcoded or through a Custom HTML tag as described in [Posthog's Google Tag Manager documentation](https://posthog.com/docs/integrate/third-party/google-tag-manager). This is a limitation of the Posthog Javascript SDK.

> ✅ The benefit of hardcoded or Custom HTML tag approach is that it **will allow you to fully configure your Posthog Javascript snippet**. Learn more about [available configuration options](https://posthog.com/docs/integrate/client/js#config).

## Template supports the following featuers:
1. **posthog.capture events**, including:
   - custom event tracking (using dataLayer `event` parameter as event name or any custom value), and the adding of event parameters, and $set and $set_once user parameters.
   - reset function to reset ids on a logout event
   - virtual pageviews for single page application
1. **posthog.identify events**, including:
   - user_id
   - $set user parameters
   - $setOnce user parameters
1. **posthog.opt_out.tracking** and **posthog.opt_in_tracking** functions that can be used in conjunction with cookie consent triggers
2. **autoTracking** since the Posthog snippet needs to be implemented either hardcoded or through a Custom HTML tag. This option can be disable in the Posthog snippet.

## Instructions
1. Implement the [Posthog Javascript SDK in Google Tag Manager using a Custom HTML tag](https://posthog.com/docs/integrate/third-party/google-tag-manager) with an All Pages trigger (or any trigger that respects your users consent wishes).
2. Implement the Posthog Custom Events template for the Google Tag Manager Template Gallery (search for `posthog`).
3. Create a new tag and select the Posthog Custom Events template.
4. Select which type of event you wish to add:
   - **Custom Event**: Choose the source for the even name value, add custom parameters and if applicable set both $set and/or $set_once user parameters defined in the tag.
   - **Identify**: Can only be used when a distinct user ID is available in the dataLayer. Can be expanded with user properties using both $set and $set_once methods.
   - **Reset**: Resets the user’s Posthog cookies and ids. Should be using in conjunction with a log out event.
   - **User Opt In / Out**: Start or stop tracking based on a user’s cookie consent.
1. Add all necessary parameters and corresponding dataLayer values.
2. Add the trigger and save.

## Feature Backlog:
- Super Properties
- Feature Flags
- Alias
- Group Analytics

## Resources
- [Posthog Javascript SDK](https://posthog.com/docs/integrate/client/js)

