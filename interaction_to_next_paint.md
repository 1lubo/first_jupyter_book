
# Interaction to Next Paint (INP)

INP aims to represent a page's overall responsiveness by measuring all click, tap, and keyboard interactions made with a page. The longest of those observed interactions—with some exceptions noted below—is chosen as the page's INP value when the user is done with the page.
An interaction is a group of event handlers that fire during the same logical user gesture. For example, "tap" interactions on a touchscreen device include multiple events, such as pointerup, pointerdown, and click. An interaction can be driven by JavaScript, CSS, built-in browser controls (such as form elements), or a combination thereof.

An interaction's latency consists of the single longest duration of a group of event handlers that drives the interaction, from the time the user begins the interaction to the moment the next frame is presented with visual feedback.

![figure](experimental_interaction_to_next_paint.png)