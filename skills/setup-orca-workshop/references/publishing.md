# Publish at the end of the workshop

Use when preparing or publishing the finished plugin, not during pre-work. Recheck the current [listing requirements](https://www.onorca.dev/plugins/add), [authoring guide](https://github.com/stablyai/orca/blob/main/docs/reference/plugin-authoring.md), and linked listing policy.

1. Test the actual plugin, including its main interaction, empty/error states where relevant, and light/dark appearance. For an HTML design, check frame sizing and bundled assets; for components, use Orca's plugin catalog and theme behavior.
2. Run `orca plugin validate .`. Resolve errors and review requested permissions. Use manifest format 2, a compatible minimum Orca version, an appropriate license, and original branding. Follow current publisher-field rules for that app version; documentation differs between releases.
3. Prepare a short README with purpose, installation/use instructions, and screenshots. Include only distributable assets and files; exclude secrets, local data, dependency folders, and unsupported binaries. Confirm the public repository is student-owned and is not a fork.
4. With publication authorized, commit and push the reviewed plugin. Match the manifest version to a new `vX.Y.Z` tag, push that tag, and add the `orca-plugin` repository topic using `gh`. Never overwrite an existing release tag.
5. Check `https://www.onorca.dev/plugins/<owner>/<repo>` for listing status. Fix reported problems and release a new version when needed. Don't equate a successful push with a confirmed listing or guarantee indexing time.

Public release is the workshop outcome; setup alone does not authorize publishing a starter. Preserve existing authorization when the student has already requested the finished release.
