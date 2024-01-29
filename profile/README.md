# Project Herta
Project Herta aims to be a simple and easy to use Honkai Star Rail assistant, with features like:
* Battle/damage prediction (Not a complex battle simulation, just something you could have on the side and help optimize a battle, which take in variables like light cones, relics, and the level of traces, as much as the fandom provides)
* Character information (Level up cost from lvl x to y, with stats that will hopefully be accurate to the game)
* Downloadable character portraits and splash art

> *To be honest, it's a very ambitious project and I don't know how to implement all of this,
> the whole thing is a massive [HSR Fandom](https://honkai-star-rail.fandom.com/wiki/Honkai:_Star_Rail_Wiki)
> scraper with the aim of being something you can run alongside HSR*

At the moment, I am only focusing on the small things, like maturing the frontend and backend, and eventually
UI decisions

This project is developed by me, Kiwifruit, with hopes of
eventually [porting this to android](https://source.android.com/docs/setup/build/rust/building-rust-modules/overview).
If you find this project interesting and you'd be willing to help with the project's development, please contact me.
Because of this, development will be very slow, only occuring when I am spurred to do so, please do not expect this
project to finish any time soon.

## Project Structure
The project is divided into two crates, the [backend library](https://github.com/Project-Herta/herta-lib)
and its [interface](https://github.com/Project-Herta/herta-bin). The whole reason for this, mentioned earlier,
is to eventually port the entire thing to android, so there would eventually be a `herta-android` repository
(*very* very) somewhat far into the future. This division is also made for FFI, for when someone wants to
implement a better UI for Project Herta.

The backend is does the scraping and calculation, while the frontend interface handles the HTTP requests,
the backend isn't designed to request the webpages, because yes 🙂

Enough yapping, hopefully by the time you are reading this, at least `herta-bin` will be useful
