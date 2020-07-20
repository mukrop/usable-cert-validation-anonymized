# docs-changes-tracker
This repository keeps track of given files on the internet and its workflow run fails if there's a change in them since the last run. You can specify URLs to those files in `docs-urls.txt`.
This tool is configured to run on GitHub using GitHub actions and workflow. It fails if there was a change and leaves `diff` output in the log of the run.

## Usage
Manually, you can run `python3 libscheck.py`. This automatically reads saved urls in `docs-urls.txt`.

## `docs-urls.txt` structure
One url on each line, blank lines are ignored.
Also you can use comments. Comment lines are those that start with `#` (watch out you can't use comment in the middle of a line, e.g. after an url).

This won't work!
```text
https://valcikeric.github.io/  # some comment
```

### Example `docs-urls.txt`:
```text
# test text file

https://valcikeric.github.io/

# actual docs

https://raw.githubusercontent.com/openssl/openssl/master/doc/man3/X509_STORE_CTX_get_error.pod
https://raw.githubusercontent.com/openssl/openssl/master/doc/man1/openssl-verify.pod.in
```
