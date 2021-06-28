# Rustshell - A VERY basic reverse shell in rust

I'm currently working on learning the basics of Rust, and wanted to do something relatively useful with it, so I wrote a small program to use as a reverse shell. It can be compiled on Windows or Linux and requires no dependencies. It is at the moment incredibly basic, but I do plan on refining it over time. Currently, it just makes a TCP connection to the specified server, and runs anything it receives as a command (either through 'sh' on linux, or 'cmd' on windows).

Things I'd like to add eventually:

* An actual shell with prompts and everything!
* Writing stderr to the shell
* Refactor some of the code into different functions instead of having everything process through main()
* Encryption between the command server and the client
* Many many other things tbd

## Usage

* Build with `cargo build`
* Set up a listener, such as with `nc -lnvp <port>`
* Run with `rustshell <host> <port>`

## Disclaimer

This was made for educational purposes only. It is not advisable to use this in production environments, especially in its current state.
