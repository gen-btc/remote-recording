# Remote Recording

The goal of this project is to create a set of web-based apps for remote recording of guests for podcasting. Currently this type of functionality is covered by apps/websites like Riverside.fm. 

The plan is to develop the project in Rust. Actix-web will be used for the front-end development.

MVP for the app will the ability to record in .wav format a conversation with a remote guest. The parties should be able to select their input and output. Audio should be recorded locally to each participant's computer and then uploaded to the host's computer when the recording is stopped. Any communication should occur over encrypted communications.

Nice to have would be the ability to have a round table type discussion with up to say a dozen participants. A chat room for text conversation and the ability to "raise a virtual hand" would be needed to help keep the conversation flowing.


## Basic Architecture

  [User]
    |
    | HTTPS Request
    |
[NGINX Reverse Proxy]
    |
    +-----> Actix-web (frontend server)
    |
    +-----> Rust backend (API, processing, etc.)
