# packtFree

Cli tool for scraping [Packt Publishing Free Learning](https://www.packtpub.com/packt/offers/free-learning) and notifying users about resulting offer.

You can notify users about offer via email (with mailgun) or just printing it to standard output (terminal).

If notifying via email, some configurations are required - mailgun client credentials and name/email for sender and recipients (see examples in cmd/config/).

Lastly, since each day Pack Publishing offers different e-book, I suggest setting up a Cron job that automatically executes command each day.

# How to install

Move in `cmd` folder and `go build -o packtFree` or `go install -o packtFree`.

If intended for Cron job, I suggest using `install` command since binary is then moved to `$GOPATH/bin` and thus accessible from everywhere (assuming `$GOPATH/bin` is in your `PATH`)

# How to use

```
packtFree -notifier=email
```
If flag is omitted, it defaults to printing the offer to the terminal.
