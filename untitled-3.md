# AWS CLI\(Command Line Interface\) Installation on Mac Using Homebrew

## AWS CLI\(Command Line Interface\) Installation on Mac Using Homebrew

[![Yogesh Darji](https://miro.medium.com/fit/c/96/96/1*Ai8008hpcOLFnsxmsm6oVQ.jpeg)](https://medium.com/@yogeshdarji99?source=post_page-----5bad783483a----------------------)

![](https://miro.medium.com/max/60/1*F9MCnexcULiewFXQpsftgA.png?q=20)

Below are the steps to install awscli using homebrew on your mac:

1. Install homebrew on your mac terminal if you don’t have one using this command

```text
$xcode-select --install$ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

2. Install awscli using brew

```text
$brew install awscli
```

3. Give permissions to pkgconfig

```text
$chmod 755 /usr/local/lib/pkgconfig
```

4. If you get below warning

```text
Warning: awscli 1.14.30 is already installed, it's just not linked.You can use `brew link awscli` to link this version.
```

5. Link your awscli

```text
$brew link awscli
```

6. Check if it is working

```text
$aws
usage: aws [options]   [ ...] [parameters]To see help text, you can run:aws helpaws  helpaws   help
```

Please comment below, I would be more than happy to help, if you would like to know more about AWS or have any specific questions.

