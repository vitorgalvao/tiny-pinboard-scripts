# Scripts to Interact with [Pinboard](https://pinboard.in/)

You can install these via the [the Homebrew tap](https://github.com/vitorgalvao/homebrew-tiny-scripts), or download and run them directly as they are self-contained.

### pinboard-backup

```
Backup all bookmarks from a pinboard account.

Usage:
  pinboard-backup [options]

'token' options are compatible between pinboard-backup, pinboard-delete-unread, pinboard-link-check, pinboard-url-update, pinboard-waybackmachine

Options:
  -x, --xml             Export as XML (default is JSON).
  -o, --output <file>   File to export to (defaults to saving in your home).
  -t, --token <token>   Your Pinboard API token.
  -a, --ask-for-token   Ask for your Pinboard API token on start.
  -s, --save-token      Save Pinboard API token to Keychain and exit. Use with '--token' or '--ask-for-token' (macOS-only).
  -h, --help            Show this message.
```

### pinboard-delete-unread

```
Delete Pinboard unread bookmarks older than X days. Give 'all' as an argument to delete all unread bookmarks.

Usage:
  pinboard-delete-unread [options] <days>

'token' options are compatible between pinboard-backup, pinboard-delete-unread, pinboard-link-check, pinboard-url-update, pinboard-waybackmachine

Options:
    -t, --token <token>              Your Pinboard API token.
    -a, --ask-for-token              Ask for your Pinboard API token on start.
    -s, --save-token                 Save Pinboard API token to Keychain and exit (macOS-only). Use with "--token" or "--ask-for-token".
```

### pinboard-link-check

```
Check the status code of links saved to a pinboard account.

By default, unread bookmarks and bookmarks with a 'pinboard-link-check-ignore' tag are ignored.

Usage:
  pinboard-link-check [options]

'token' options are compatible between pinboard-backup, pinboard-delete-unread, pinboard-link-check, pinboard-url-update, pinboard-waybackmachine

Options:
  -r, --redirect-log      If set, links with 301 (Moved permanently) will be on their own log. Pairs well with the 'pinboard-url-update' script.
  -l, --log-dir <dir>     Directory to save logs to. Defaults to the home directory.
  -i, --include-unread    Also check unread bookmarks.
  -g, --include-ignored   Do not ignore links with a 'pinboard-link-check-ignore' tag.
  -t, --token <token>     Your Pinboard API token.
  -a, --ask-for-token     Ask for your Pinboard API token on start.
  -s, --save-token        Save Pinboard API token to Keychain and exit. Use with '--token' or '--ask-for-token' (macOS-only).
  -h, --help              Show this message.
```

### pinboard-url-update

```
Substitute URLs of Pinboard bookmarks. Interacts with the files produced by 'pinboard-link-check': text file, each line following the pattern 'old_url → new_url'.

Usage:
  pinboard-url-update [options] <file>

'token' options are compatible between pinboard-backup, pinboard-delete-unread, pinboard-link-check, pinboard-url-update, pinboard-waybackmachine

Options:
    -t, --token <token>              Your Pinboard API token.
    -a, --ask-for-token              Ask for your Pinboard API token on start.
    -s, --save-token                 Save Pinboard API token to Keychain and exit (macOS-only). Use with "--token" or "--ask-for-token".
```

### pinboard-waybackmachine

```
Add to the Wayback Machine links saved to a pinboard account.

Usage:
  pinboard-waybackmachine [options] run

The argument 'run' is necessary to prevent running the script by mistake.

'token' options are compatible between pinboard-backup, pinboard-delete-unread, pinboard-link-check, pinboard-url-update, pinboard-waybackmachine

Options:
    -t, --token <token>              Your Pinboard API token.
    -a, --ask-for-token              Ask for your Pinboard API token on start.
    -s, --save-token                 Save Pinboard API token to Keychain and exit (macOS-only). Use with "--token" or "--ask-for-token".
```
