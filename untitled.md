# Configuring Nano Text Editor with nanorc – Linux Hint

Nano is a very lightweight command line text editor. Many Linux system administrators use Nano to do basic editing of Linux configuration files as it is easier to work with than Vim. Vim has a little bit of a learning curve that Nano don’t have.In this article, I will show you how to configure the Nano text editor. So, let’s get started.

## Configuration File of Nano Text Editor:

You can configure Nano text editor system wide using the **/etc/nanorc** file.

You can also do user specific configuration of Nano text editor. In that case, you will have to create a **.nanorc** file in the HOME directory of the user you want to configure Nano for.

I will talk about many of the configuration options Nano has and how they work. You can use the **~/.nanorc** file or the system wide **/etc/nanorc** file. It will work for both of them.

### Using ~/.nanorc File for User Specific Configuration of Nano:

The **~/.nanorc** file does not exist in your login users HOME directory by default. But, you can create one very easily with the following command:

![](https://linuxhint.com/wp-content/uploads/2018/12/1-2.png)

Now, you can edit the **~/.nanorc** file as follows:

![](https://linuxhint.com/wp-content/uploads/2018/12/2-2.png)

**~/.nanorc** file should be opened with Nano text editor. Now, type in your required configuration options here.

![](https://linuxhint.com/wp-content/uploads/2018/12/3-2.png)

Once you’re done, you have to save the file. To save the file, press + **x**. Then, press **y**.

![](https://linuxhint.com/wp-content/uploads/2018/12/4-2.png)

Now, press. The changes to the **~/.nanorc** configuration file should be saved.

![](https://linuxhint.com/wp-content/uploads/2018/12/5-2.png)

#### Displaying Line Numbers in Nano:

Nano does not show line numbers by default. I will show you how to display line numbers using **~/.nanorc** file and **/etc/nanorc** file in this section. So you will figure out how it works. From the next sections, I will use the **~/.nanorc** file only for simplicity.

**Using the ~/.nanorc File:**

To show line numbers, type in **set linenumbers** in **~/.nanorc** and save it.

![](https://linuxhint.com/wp-content/uploads/2018/12/6-2.png)

As you can see, the line numbers are displayed.

![](https://linuxhint.com/wp-content/uploads/2018/12/7-2.png)

**Using /etc/nanorc File:**

To display line numbers on nano system wide, open **/etc/nanorc** with the following command:

![](https://linuxhint.com/wp-content/uploads/2018/12/8-2.png)

The **/etc/nanorc** file should be opened. It should look as follows. As you can see, all the nano options are already here. Most of them are disabled \(commented out using \# at the beginning\) and some of them are enabled.

![](https://linuxhint.com/wp-content/uploads/2018/12/9-2.png)

To display line numbers, find the line as marked in the screenshot below.

![](https://linuxhint.com/wp-content/uploads/2018/12/10-2.png)

Now, uncomment the **set linenumbers** line and save the file.

![](https://linuxhint.com/wp-content/uploads/2018/12/11-2.png)

As you can see, the line numbers are not displayed.

![](https://linuxhint.com/wp-content/uploads/2018/12/12-2.png)

#### Enabling Auto Indentation in Nano:

Auto indentation is not enable by default in Nano text editor. But, you can use the **set autoindent** option in **~/.nanorc** or **/etc/nanorc** file to enable auto indentation in Nano text editor.

#### Enabling Mouse Navigation in Nano:

If you’re using Nano text editor in a graphical desktop environment, then you can use your mouse to navigate. To enable this feature, use the **set mouse** option in **~/.nanorc** or **/etc/nanorc** file.

#### Enable Smooth Scrolling in Nano:

You can use the **set smooth** option in **~/.nanorc** or **/etc/nanorc** file to enable smooth scrolling.

#### Enable Word Wrapping in Nano:

Word wrapping is a very important feature of any text editor. Luckily, Nano has the ability to do word wrapping. It is not enabled by default. To enable word wrapping in Nano text editor, use the **set softwrap** option in **~/.nanorc** or **/etc/nanorc** file.

#### Setting Tab Size in Nano:

On Nano text editor, the default tab size is 8 characters wide. That’s too much for most people. I prefer a tab size of 4 characters wide. Anything more than that makes me very uncomfortable.

To define the tab size \(let’s say 4 characters wide\) in Nano text editor, use the following option in your **~/.nanorc** or **/etc/nanorc** file.

If you want to use a tab size of 2, then use the following option in your **~/.nanorc** or **/etc/nanorc** file.

#### Automatically Converting Tabs to Spaces in Nano:

Tabs width can vary system to system, editor to editor. So, if you use tabs in your program source code, it may look very ugly if you open it with a different text editor with different tab width. If you replace tabs with specific numbers of spaces, then you won’t have to face this problem again.

Luckily, Nano can automatically convert tabs to spaces. It is not enabled by default. But you can enable it with the **set tabstospaces** option in your **~/.nanorc** or **/etc/nanorc** file.

#### Changing Title Bar Color in Nano:

You can change the title bar color in Nano text editor using the following option in your **~/.nanorc** or **/etc/nanorc** file.

set titlecolor foregroundColorCode,backgroundColorCode

Here, the supported **foregroundColorCode** and the **backgroundColorCode** are:

white, black, blue, green, red, cyan, yellow, magenta

For example, let’s say, you want to set the background title bar color to **yellow** and the foreground/text color to **red**, the option to put in the **~/.nanorc** or **/etc/nanorc** file should be.

set titlecolor red,yellow

![](https://linuxhint.com/wp-content/uploads/2018/12/13-2.png)

#### Changing Other Colors in Nano:

You can change colors in other parts of your Nano text editor. Other than **titlecolor**, there are **statuscolor**, **keycolor**, **functioncolor**, **numbercolor** options in Nano. These options are used the same way as the **titlecolor** option shown in the earlier section of this article.

You can see what option changes colors of which part of Nano text editor below:

![](https://linuxhint.com/wp-content/uploads/2018/12/15-2.png)

#### Getting Help with nanorc Options:

There are many more options for configuring Nano text editor. It is out of the scope of this article to cover each and every one of them. I covered the basics. If you need something that is not available here, feel free to take a look at the manpage of nanorc.

You can read the manpage of nanorc with the following command:

![](https://linuxhint.com/wp-content/uploads/2018/12/16-2.png)

The manpage of nanorc.

![](https://linuxhint.com/wp-content/uploads/2018/12/17-2.png)

So, that’s how you configure Nano text editor with nanorc. Thanks for reading this article.

#### About the author

![Shahriar Shovon](https://linuxhint.com/wp-content/uploads/2018/01/photo2-150x150.png)

Freelancer & Linux System Administrator. Also loves Web API development with Node.js and JavaScript. I was born in Bangladesh. I am currently studying Electronics and Communication Engineering at Khulna University of Engineering & Technology \(KUET\), one of the demanding public engineering universities of Bangladesh.

