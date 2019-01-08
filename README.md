# polymer-wct-demo [![Build status][travis-img]][travis]

Testing Polymer 2 using Web Component Tester (WCT).

## Initialization

You don't need to initialize this demo, this is already done. You can continue
to the next section. If you're interested about how to do it, the command is:

    $ polymer init polymer-2-element

Just click ENTER to go next when the interactive commands are displayed.

## Installation

Install Polymer CLI 1.6.0 and Bower 1.8.4:

    $ npm install -g polymer-cli@1.6.0
    $ npm install -g bower@1.8.4

Ensure the versions installed are correct:

    $ node --version
    v6.11.3
    $ npm -version
    5.6.0
    $ polymer --version
    1.6.0
    $ bower --version
    1.8.4

Build the app:

    $ bower install
    $ polymer build

Run the tests:

```
polymer-wct-demo $ polymer test
Installing and starting Selenium server for local browsers
Selenium server running on port 53858
safari 12.0.1            Beginning tests via http://localhost:8081/components/polymer-wct-demo/generated-index.html?cli_browser_id=2
chrome 71                Beginning tests via http://localhost:8081/components/polymer-wct-demo/generated-index.html?cli_browser_id=0
chrome failed to maximize
safari 12.0.1            Tests passed
chrome 71                Tests passed
[BABEL] Note: The code generator has deoptimised the styling of "unknown" as it exceeds the max of "500KB".
firefox 58               Beginning tests via http://localhost:8081/components/polymer-wct-demo/generated-index.html?cli_browser_id=1
firefox 58               Tests passed
Test run ended with great success

chrome 71 (2/0/0)                       firefox 58 (2/0/0)                      safari 12.0.1 (2/0/0)
```

## Troubleshooting

**GeckoDriver** is installed by WCT, if you have another one available in your
PATH variable, it won't be used.

**Firefox** version has an impact on the tests. We're using GeckoDriver 0.19.0
here, it is only compatible with Firefox 55-62. If the version is not
compatible, the tests will fail. See [mapping between
geckodriver releases, supported versions of Firefox, and required Selenium
version](https://firefox-source-docs.mozilla.org/testing/geckodriver/geckodriver/Support.html).

[travis]: https://travis-ci.org/mincong-h/polymer-wct-demo
[travis-img]: https://travis-ci.org/mincong-h/polymer-wct-demo.svg?branch=master
