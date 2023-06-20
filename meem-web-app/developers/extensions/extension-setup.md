# Extension Setup

**Create extension files**

We've created an easy way to set up the necessary files to build an extension.&#x20;

From the project root directory, run `yarn createExtension` and follow the instructions. Files will be auto-generated with matching class names and example code for you to get hacking.&#x20;



**Add extension icons**

Add light and dark mode icons (ideally 64x64px png or larger) to represent the extension (follow the pattern `integration-[extension-slug].png`, appending `-white` at the end for dark mode)

e.g. `integration-discord.png` and `integration-discord-white.png`)



**Enable the extension on your community**

Ensure that the extension shows up in your community's extension settings page, which requires having the Meem team adding the extension to our database. (See [getting-started.md](getting-started.md "mention") to find out how).

Then click to enable it. After a moment, you should now be able to navigate to the extension's settings page (if a Link extension) or both its homepage and settings page (if a Standard extension)



**Enable widget support**

You'll need to modify the extensions switch case found in the `AgreementHome.ts` component file:\


```typescript
<div key={extension.id}>
	{extension.Extension?.slug ===
	'symphony' && (
		<>
			<SymphonyWidget />
		</>
	)}
	{extension.Extension?.slug ===
	'discussions' && (
		<DiscussionWidget
			key="discussion-widget"
			agreement={agreement}
		/>
	)}

	{extension.Extension?.slug ===
	'guild' && (
		<GuildWidget key="guild-widget" />
	)}
</div>
```

See inline code documentation on how to modify the components for your own extension's UI  needs.
