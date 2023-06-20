# Extension File Structure

The file structure of an extension looks like this:

* A subfolder within `components/Extensions` containing the Extension's widget
* A small modification to `AgreementHome` to enable the widget on the community if the Extension is enabled (see [extension-setup.md](extension-setup.md "mention"))
* Optionally, a subfolder inside `pages/[slug]/e/` containing any additional Extension pages on the Meem web app
