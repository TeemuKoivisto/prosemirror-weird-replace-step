# [prosemirror-weird-replace-step](https://teemukoivisto.github.io/prosemirror-weird-replace-step/)

When I replace `'<i>p</i>o'` text with a character, say `'m'`, it produces a quite convoluted ReplaceStep which, for some reason, defaults all marks's attributes to their default values.

## To reproduce

1. Go to https://teemukoivisto.github.io/prosemirror-weird-replace-step OR locally you can run `node serve.js` and go to http://localhost:4040/
2. Follow the steps


### Previous at https://github.com/TeemuKoivisto/prosemirror-weird-replace-step/tree/13c125a37430efcafce4dd6e8a304aa85df6a9c1

1. Go to https://teemukoivisto.github.io/prosemirror-weird-replace-step
2. Click 'Restore example'
3. Select <code><i>p</i>o</code>, press <code>m</code>
4. The below JSON should be shown

```json
{
  "stepType": "replace",
  "from": 5,
  "to": 38,
  "slice": {
    "content": [
      {
        "type": "text",
        "text": "m"
      },
      {
        "type": "text",
        "marks": [
          {
            "type": "italic",
            "attrs": {
              "color": null
            }
          }
        ],
        "text": "l"
      },
      {
        "type": "text",
        "text": "oo"
      },
      {
        "type": "text",
        "marks": [
          {
            "type": "bold",
            "attrs": {
              "color": null
            }
          }
        ],
        "text": "o"
      },
      {
        "type": "text",
        "text": "oooo"
      },
      {
        "type": "text",
        "marks": [
          {
            "type": "bold",
            "attrs": {
              "color": null
            }
          }
        ],
        "text": "o"
      },
      {
        "type": "text",
        "marks": [
          {
            "type": "italic",
            "attrs": {
              "color": null
            }
          }
        ],
        "text": "mm"
      },
      {
        "type": "text",
        "text": "oooo"
      },
      {
        "type": "text",
        "marks": [
          {
            "type": "bold",
            "attrs": {
              "color": null
            }
          }
        ],
        "text": "ooo"
      },
      {
        "type": "text",
        "text": " ooo"
      },
      {
        "type": "text",
        "marks": [
          {
            "type": "bold",
            "attrs": {
              "color": null
            }
          }
        ],
        "text": "o"
      },
      {
        "type": "text",
        "marks": [
          {
            "type": "italic",
            "attrs": {
              "color": null
            }
          }
        ],
        "text": "cb"
      },
      {
        "type": "text",
        "text": "ooo"
      },
      {
        "type": "text",
        "marks": [
          {
            "type": "italic",
            "attrs": {
              "color": null
            }
          }
        ],
        "text": "ocb"
      }
    ]
  }
}
```

## How to install

0. `git submodule update --init --recursive`
1. `yarn`
2. `yarn pm`
3. `yarn start`
