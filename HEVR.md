# HEVR dev logs

- Repository: https://github.com/omega-gg/HEVR
- Azure CI: https://dev.azure.com/bunjee/HEVR/_build?definitionId=12&_a=summary

## Renaming ALVR2 to HEVR - 5/28/2020
So I wrote the following email to polygraphene:

    Greetings polygraphene,

    Hopefully everything is fine for you during these troubled times!

    First, let me thank you for the great contribution you gave to the community with ALVR.

    Along with a few contributors we have decided to keep improving on the original code from your GitHub repository. I've also started a rewrite of the alvr_server with native C++ and Qt (to make it work on Linux, among other things).

    I thought about calling it ALVR2. We want to keep the ALVR name as an hommage to the original project and keep the community together.

    Would you be okay with us naming that new repository ALVR2 or ALVRX (as one contributor suggested) ?

Since I didn't get an answer I decided to rename the ALVR2 to HEVR -> High Efficiency Virtual Reality.

That name is a geeky pun based on the HEVC (H265) encoder and an emphasis on the streaming nature of the project.
So I'll resume working on the project with that new name.

Even though I'm departing from the ALVR name I'd like to maintain the compatibility with future [JackD83](https://github.com/JackD83) ALVR efforts, including a new GUI or a new client.

## ALVR2 project is up \o/ - 5/21/2020
I'm currently working on the new repository for ALVR2 (alvr_server v2).
I'm doing my best to keep the original project legacy and read about it.
My goal is to retain what makes it great while making it portable, easy to use, maintain and expand.

zarik5 has kindly shared wiki files with me regarding his project called ALVR-next that he started writing with Rust.
This should help me evaluate the best path to architecture the rewrite to handle future improvements.

Repository: https://github.com/omega-gg/ALVR2

The initial project is now up an running, displaying a beautiful "Welcome to ALVR2" from the console.
CI should be functionnal on Windows (gcc / msvc) / Linux / macOS.

My rewrite is going to use Qt because multiplatform without a good framework is hell.
An alternative would be Boost but I have more experience with Qt and I think I like it better.
It's also going to be based on my application kit called [Sky](http://omega.gg/Sky) that I designed for MotionBox.
License wise, I decided to go from GPLv3 to LGPLv3 to make it suitable for the ALVR2 developpement.
This should give me a headstart for various mundane tasks like handling configuration stuff.
Being a single developper on this, it's a good thing to avoid reinventing the wheel.
