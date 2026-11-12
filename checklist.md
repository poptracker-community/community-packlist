# PopTracker Pack List Checklist

When changing or adding a pack to a packlist (e.g. [`community-packs.json`](./community-packs.json)),
make sure to verify the following:

* The new key in the top level object matches the `package_uid` in the `manifest.json` of packs that should be upgraded:
  Usually that means it is the same as all `package_uid`s of all `manifest.json`s of all downloads listed in the
  linked versions json (`versions_url`). This may not be true if the `package_uid` changed at some point.
* `versions_url` of changed/added objects starts with `https://` and points to a valid versions file.
* `homepage` of changed/added objects starts with `https://` and points to a valid website.
* `icon_url` of changed/added objects starts with `https://` and points to a valid PNG (preferred) or JPEG, not WEBP.
* `name`, `author` and `platform` of changed/added objects match the properties of the `manifest.json` in the latest
  download (highest version number) in the linked versions json (`versions_url`).
* The proposed changes result in a valid JSON file (no extra or missing `,`).
* You are the author of the pack or have permission to add the pack.

* Due to an ACE security issue (arbitrary code execution) found in Git on November 10, 2026, tracked as CVE-2026-111760, all
  submitted pack releases cannot contain a `.git` folder. Click [here](https://github.com/git/git/security/advisories/GHSA-vp2w-7xxj-jvxr)
  to learn more about this issue and why this rule was added.
  
  If a later release is found/reported to have a `.git` folder, your pack will be removed from the list until you are compliant
  with our rule. If this rule is continuously ignored, you may be blacklisted from the community packlist entirely, including
  any future packs you may make.
