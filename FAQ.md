# Frequently Asked Questions

## Quick Links
- [I don't see my question here. How do I ask a question or contribute a FAQ?](#contribute-to-the-FAQ)
- [I can't access the project directory](#i-cant-access-the-project-directory)
- [I can't sign into Cedar](#i-cant-sign-into-cedar)
- [My connection to Fir timed out](#my-connection-to-fir-timed-out)
- [How do I copy specific subject folders, sub-folders, or specific files to my scratch directory?](#how-do-I-copy-specific-subject-folders-sub-folders-or-specific-files-to-my-scratch-directory)

---

## Questions & Answers

### Contribute to the FAQ

If you don't see your question here or if you'd like to contribute a FAQ, please create and submit it as a [new issue](https://github.com/INN-SFU/BRS_Training/issues/new/choose). We'll respond to your question and post it here as soon as we can. Thank you!

### I can't access the project directory

Make sure that the path you are trying to access begins with `/project/ctb-rmcintos`. You won't find the project directory from your home directory (`~`).

### I can't sign into Cedar

As of September 2025, Cedar has been decommissioned and replaced with [Fir](https://docs.alliancecan.ca/wiki/Fir). Please use `fir.alliancecan.ca` instead of `cedar.computecanada.ca` or `cedar.alliancecan.ca`.

### My connection to Fir timed out

Fir can experience network connectivity issues from time to time. You can check on the status of Fir [here](https://status.alliancecan.ca/system/Fir) and try again later.

### How do I copy specific subject folders, sub-folders, or specific files to my scratch directory?

If you want to copy specific **subject folders** and/or **sub-folders** (like `sub-BRS0001/ses-1/meg/`) from `/project/ctb-rmcintos/data-sets/BRS` to your own `scratch` directory, you can use an rsync script and a list of subjects that you're interested in. See the page on [copy_subs](tools/copy_subs.md). Please also see the [Training Session Notebook](Training_Session_Notebook.ipynb).
