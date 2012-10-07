# 見えない

An experimental userscript to sync the hidden threads from the [4chan catalog](http://catalog.neet.tv) with the regular 4chan board pages. Look, I even thought up a weaboo name with my limited knowledge of Japanese! Am I cool yet?

# Approach

The userscript runs on the catalog as well as board.4chan.org. When a thread is hidden, events sync the `localStorage` representation of hidden threads across both domains, using hidden `iframe`s and `window.postMessage`, and hides the threads in active pages using the `storage` event.

Initially, I'm targeting only the [vanilla 4chan extension](https://github.com/4chan/4chan-JS)'s thread hiding mechanism. Eventually, I will target 4chan-X and html5chan as well.

