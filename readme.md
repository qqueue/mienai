# 見えない

`mienai` synchronizes your hidden threads from the [4chan
catalog](http://catalog.neet.tv) with the regular 4chan board pages. If you use
the catalog extensively, but can't resist the classic F5 experience on page 0,
this userscript will keep your threads hidden in either view.

It even works in real-time! Try it out with two windows or tabs. Cool? Yes.
Near useless? Yes.

**Right now, only the [built-in 4chan
extension](https://github.com/4chan/4chan-JS)'s "Thread Hiding" feature is
supported. Stand by for a 4chan-X version.**

# Installation

[Download the latest version here.](https://github.com/qqueue/mienai/downloads)

If you're on Firefox >=14 with Greasemonkey >=1.3, it should just werk. If you're
on Chrome >=22, save the file to your computer, open up the Extensions page,
and drag `mienai.user.js` to install.

If you're on Opera >=12.10, `mienai` will likely work, but I don't care enough
to test it. Submit a bug report if it breaks.

# Approach

The userscript runs on the catalog as well as board.4chan.org. When a thread is
hidden, events sync the `localStorage` representation of hidden threads across
both domains using hidden `iframe`s and `window.postMessage` and hide the
threads in active pages using the `storage` event. It's all pretty wonderful,
you should check out the source.

