# gh-catsup

A `gh` extension to generate summaries of GitHub repository events around issues and PRs.

## Quickstart

1. `gh extension install andyfeller/gh-catsup`
1. `gh catsup <owner>/<repo> ...`
1. Profit! :moneybag: :money_with_wings: :money_mouth_face: :money_with_wings: :moneybag:

## Usage

```shell
$ gh catsup --help


Generate report of recent repository issue and pull request events.

USAGE
  gh catsup [flags] <organization or repo> ...

FLAGS
  -c, --cache-dir=</path/to/dir>      Path to directory to cache data used by extension; default creates temporary directory
  -d, --date-format=<format>          Format of datetimes; default `%b %d %Y`
  -D, --debug                         Enable debugging
  -e, --exclude-event=<events>        Event to exclude from output, can be used multiple times
  -f, --format=<format>               Output render format; default `markdown-list`
                                        - `markdown-list`: simple list of issue links in GFM
                                        - `markdown-table`: extensive table of information in GFM
                                        - `terminal`: extensive table of information for shell usage
  -h, --help                          Display help usage
  -H, --hostname=<hostname>           Hostname of the GitHub instance to authenticate with
  -i, --include-event=<events>        Event to include with output, can be used multiple times
  -o, --output-path=</path/to/file>   Path to file to capture output; default to standard out
  -p, --preserve                      Preserve temporary cache directory containing data
  -s, --since=<days>                  Number of days since updated; default `7`

EVENTS
  added_to_project
  added_to_project_v2
  assigned
  base_ref_changed
  base_ref_deleted
  base_ref_force_pushed
  comment_deleted
  convert_to_draft
  converted_from_draft
  converted_note_to_issue
  converted_to_discussion
  demilestoned
  head_ref_deleted
  head_ref_force_pushed
  head_ref_restored
  issue_closed
  issue_closed_not_planned
  issue_reopened
  labeled
  locked
  marked_as_duplicate
  merged
  milestoned
  moved_columns_in_project
  pinned
  pr_closed
  pr_reopened
  project_v2_item_status_changed
  ready_for_review
  removed_from_project
  removed_from_project_v2
  renamed
  review_request_removed
  review_requested
  signoff
  signoff_canceled
  transferred
  unassigned
  unlabeled
  unlocked
  unmarked_as_duplicate
  unpinned
```

## Setup

Like any other `gh` CLI extension, `gh-catsup` is trivial to install or upgrade and works on most operating systems:

- **Installation**

  ```shell
  gh extension install andyfeller/gh-catsup
  ```
  
  _For more information: [`gh extension install`](https://cli.github.com/manual/gh_extension_install)_

- **Upgrade**

  ```shell
  gh extension upgrade gh-catsup
  ```

  _For more information: [`gh extension upgrade`](https://cli.github.com/manual/gh_extension_upgrade)_
