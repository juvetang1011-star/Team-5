# Student interface language

The student page has an **EN / 中文** control in its header. English remains the default. The selected language is stored on the current device under `dream-journey-language` and restored on reload.

`public/student-i18n.js` owns the interface dictionary and language preference. It translates labels, headings, placeholders, accessible names, navigation, upload controls and cloud/validation messages. Static bindings are recorded before any student content is loaded. They never translate input values, team data, filenames or journal content.

Dynamic UI messages use localized templates rather than translated data fields. Switching language redraws the interface without sending a new submission or changing the project document. The database format and API field names remain unchanged.

Voice recognition follows the selected interface language (`en-US` or `zh-CN`). Switching language stops an active microphone session; finalized transcript text stays in the input. Browser support and permissions still determine whether speech recognition is available.

Browser checks covered both languages across all four stages, file-list and input preservation, selected journal-day labels, and restoring the Chinese preference after a reload. Real microphone transcription was not exercised.
