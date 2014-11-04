### Tweak your HiddenID to support Stake House

* Pull the latest [hidden-id](https://github.com/hidden-id/hidden-id).
* `git submodule update --init` (because there *was* a submodule update).

#### Per identity:

* Backup you id folder (better safe than sorry).
* Run `python2 hidden-id.py my_id_folder` to create the `sstore/templates/` and `sstore/static/` subfolders.
* You can kill it (you don't need to wait until it establishes the hidden service).
* Copy the 2 files from `templates/` to `my_id_folder/sstore/templates/`.
* Put some avatar at `my_id_folder/sstore/static/img/` (e.g. `my-avatar.png`).
* Edit `my_id_folder/sstore/profile.json` according to `example-profile.json`.

Notes:

* HiddenID serves `my_folder_id/sstore/static/` as `/static/` so we use that for the avatar.
* A "fresh" ID has `"avatar":"/static/img/default-avatar.png"` at `sstore/profile.json`,
  but for a "legacy id" you have to manually add an avatar URL to the profile
  if you want one (nothing bad happens if you don't).
