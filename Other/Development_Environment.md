# Development Environment

The following tool is required to be installed to work on this course. It contains the Git version control system that you will use to submit your work to the instructor. The Git installation package also includes a virtual terminal Mintty, the command interpreter Bash, and an SSH client to connect and work with the course server.

* [Git SCM](https://git-scm.com)

On macOS, it is recommended to install the official command-line developer tools from Apple by opening the `Terminal.app` and running the following command.

```bash
xcode-select --install
```

The following code editor is optional. It is not required, but it can be helpful if you will not feel comfortable working with the command-line interface for long periods. You have to install the 'Remote - SSH' extension from the editor to use it with our remote server.

* [Microsoft Visual Studio Code](https://code.visualstudio.com)

This virtualization software and the OS images will allow you to set up your development environment on your computer to not depend on the course server. It is optional to set it up. You are on your own here as we will not help you figure out what to do to get your environment up and running. Internet is full of information about the process, though. The Vagrantfile in this directory could be helpful.

* [Vagrant](https://developer.hashicorp.com/vagrant)
* [Oracle VM VirtualBox](https://www.virtualbox.org)
* [VMware Fusion](https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion)

---

To setup, a development environment, open the terminal (for example, through `git-bash` on Windows) and run the Secure Copy (`scp`) program to download credentials to your machine to login to the course server. Your credentials will include public and private RSA cryptographic keys with a configuration file to point to our server with your login information. To download the keys, you will have to agree with any prompts by typing `yes` and pressing enter. You will also have to type the password when prompted. The password will be given to you during the class. The passwords will be disabled two weeks after the start of the course. Ensure to get your keys before that. You will not be able to see your password when you type it. It is normal not to leak it to your command-line history file or show it to people nearby. Continue typing the password. If the system does not accept your password multiple times, type it into a text editor, cut and paste it into the terminal window. Remember that `CTRL+C` and `CTRL+V` key combinations do not work in most Unix terminals. You will have to use other key combinations that are different for different terminals. Mintty on Windows uses `CTRL+INSERT` and `SHIFT+INSERT` by default. macOS terminal users are luckier as they can use the standard `COMMAND+C` and `COMMAND+V` key combinations.

```bash
# WARNING: If you have existing .ssh keys or configuration files, make a backup of them first.
scp -r <AUCA/GHEA login>@auca.space:~/.ssh ~/
```

Do not forget to replace `<AUCA/GHEA login>`, including the `<` and `>` character, with your actual AUCA/GHEA login. For example, `toksaitov_d` would be the text the instructor of this course would write to download the keys to access the server. GHEA students MUST replace `.`, and `-` characters in logins with `_`. For example, `toksaitov.dmitrii` should be entered as `toksaitov_dmitrii`.

From now on, you can access the server with all the necessary tools installed by issuing the following command in your terminal.

```bash
ssh auca
```

To terminate the connection from the remote server, you can issue the `exit` command.
