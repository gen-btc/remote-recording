# Remote Recording

The goal of this project is to create a set of web-based apps for remote recording of guests for podcasting. Currently this type of functionality is covered by apps/websites like Riverside.fm. 

The plan is to develop the project in Rust and React using the Janus media server to handle the heavy lifting of signal management.

MVP for the app will the ability to record in .wav format a conversation with a remote guest. The parties should be able to select their microphone and sound output. Audio should be recorded locally to each participant's computer and then uploaded to the host's computer when the recording is stopped. Any communication should occur over encrypted communications.

Nice to have would be the ability to have a round-table type discussion with up to say a dozen participants. A chat room for text conversation and the ability to "raise a virtual hand" would be needed to help keep the conversation flowing.


## Basic Architecture

The basic arcitecture would be an React (frontend server) with a Rust backend. The Janus Media Server will be middle-ware. Finally, stateful data will need to be stored in either SQLite or Postgres/MySQL.

