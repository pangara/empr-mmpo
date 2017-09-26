Download and install:

- Git Bash 2.14.1
- NodeJS v6.1.1.3
- Ruby 2.4.1-2

Installing Ruby:

When installing MSYS2 just hit enter.
Do not put a number in at all.

After all programs are installed go to the desired directory for the source code.

This step will hopefully be replaced with Dreamweaver.
In the directory, right-click and click on Git Bash Here.

Type in:

```

git clone https://github.com/bcgov-c/EAO-Internal-Guidance.git

```

You will be prompted for your git username and password.
This user must be allowed to pull from this repository.

Now type in:

```

cd EAO-Internal-Guidance

```

You are now in the project directory.

Type in:

```
gem install bundler

bundler install

./go serve

```

The server should be running.
In an internet browser go to the url:

http://127.0.0.1:4000/
