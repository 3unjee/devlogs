# ALVR2 dev logs

- Repository: https://github.com/omega-gg/ALVR2
- Azure CI: https://dev.azure.com/bunjee/ALVR2/_build?definitionId=12&_a=summary

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
