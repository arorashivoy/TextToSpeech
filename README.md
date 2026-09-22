# Speech-to-Text conversation analyser

**Archived.** A Python console client for the [Symbl.ai](https://symbl.ai) speech API,
written June–November 2022 as an IIIT-Delhi assignment with Nishi Ninawat and
Suhani Mathur.

**The repository name is backwards** — this is speech to text, not text to speech. It
takes an `.mp3` of a conversation, submits it to Symbl.ai's async API, polls for the
job, and then pulls back the transcript along with the topics, questions and action
items Symbl extracts from it. A sample `test.mp3` is included.

## Running it

It needs Symbl.ai credentials, which are not committed. Copy the template and fill in
your own:

```
cp Keys.example.json Keys.json
python3 main.py
```

`GetToken.py` exchanges `appId` and `appSecret` for an access token and writes it back
into `Keys.json`; `conversationId` and `jobId` are filled in as the program runs, so
they start empty. `Keys.json` is gitignored — do not commit it.

Without this file the program exits on a missing-file error at startup, which is what
earlier visitors to this repository would have hit.
