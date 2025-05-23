# Style Guide

- Put items in the appropriate section:
  - StackOverflow for posts on the stackexchange network
  - Main category for everything else
- Title should be in one of the following formats, based on the infamous thing in question:
  - Repository: `<title>`
  - Pull/Merge Request: `<repo title>#<MR number>`
  - Issue: `<repo title>#<issue number>`
  - Commit: `<repo title> <commit hash (7 chars)>`
  - StackOverflow post: `<Post title (question)>`
- Date should be in ISO 8601 format
  - e.g. September 19th, 2023 is `2023-09-19`
  - date *must* be in UTC
    -  On GitHub, you can get this date by inspecting the date element, then evaluating `$0.datetime.split("T")[0]` in the browser console
- All markdown files must be formatted before committing
  - On VSCode, use extensions `yzhang.markdown-all-in-one` and `TakumiI.markdowntable`
  - Eventually, we should add a pre-commit hook to automatically format everything
- Keep descriptions concise
  - Briefly describe the thing itself, and *why* it is infamous or otherwise notable
  - Format descriptions as sentences
  - 1 link providing more information is acceptable
    - Link title should accurately describe the content at the link

## Scripts to add new items:
- GitHub issue: `gh issue view -R OWNER/REPO NUMBER --json 'createdAt,number,title,url'`
  - This should get you the information you need to fill in the item metadata
  - Of course you should read the comments and description to figure out why
    this issue is infamous!
