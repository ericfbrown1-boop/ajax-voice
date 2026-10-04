# ajax-voice

A single static page: interruptible voice chat with the OpenAI Realtime API from
a phone browser, over WebRTC.

It holds **no API key, no credential and no private data**. You paste a
short-lived session token (`ek_...`, ~10 minutes) at use time; it lives in one
tab and is cleared from the DOM once the call connects. Audio goes from the
browser straight to OpenAI and never transits the machine that minted the token.

This surface has no data access - no databases, no files, no memory, no search -
and the session is instructed to refuse figures rather than invent them. A hard
session cap and an idle timeout are enforced in the page, because a realtime
socket bills per minute and an idle one bills too.

Public because GitHub Pages requires it. There is nothing here worth taking.
