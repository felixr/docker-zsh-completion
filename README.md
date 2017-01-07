docker-zsh-completion
=====================

A [zsh](http://zsh.org) completion for [Docker](http://docker.io).

**Deprecation notice**: This repository is not kept up-to-date any more. Please,
switch to the [ZSH completion from Docker](https://github.com/docker/docker/blob/master/contrib/completion/zsh/_docker)
directly. To keep the same behavior as previously, you may want to add the following
code to your `~/.zshrc`:

```sh
zstyle ':completion:*:*:docker:*' option-stacking yes
zstyle ':completion:*:*:docker-*:*' option-stacking yes
```
 
How to Install
--------------

For [Oh My Zsh](http://ohmyz.sh/) users:
```sh
mkdir -p ~/.oh-my-zsh/plugins/docker/
curl -fLo ~/.oh-my-zsh/plugins/docker/_docker https://raw.github.com/felixr/docker-zsh-completion/master/_docker
```
And then in your `~/.zshrc` file, add `docker` to the plugins list. Then run `exec zsh` to restart zsh.

For [Prezto](https://github.com/sorin-ionescu/prezto) users:
```sh
curl -fLo ~/.zprezto/modules/completion/external/src/_docker \
  https://raw.github.com/felixr/docker-zsh-completion/master/_docker
exec zsh
```
This assumes you have the `completion` module enabled in your `~/.zpreztorc` file.

With [zplug](https://github.com/b4b4r07/zplug):
```sh
zplug "felixr/docker-zsh-completion"
```

For other Zsh users:
Drop the `_docker` file into your `~/.zsh/completion` directory, then reset zsh:

```sh
mkdir -p ~/.zsh/completion
curl -fLo ~/.zsh/completion/_docker https://raw.github.com/felixr/docker-zsh-completion/master/_docker
exec zsh
```
This assumes `~/.zsh/completion` is in Zsh's `$fpath` [parameter](http://zsh.sourceforge.net/Doc/Release/Parameters.html#index-fpath). Run `echo $fpath` to check.


Contributors
------------

* [felixr](http://github.com/felixr)
* [vincentbernat](http://github.com/vincentbernat)
* [sdurrheimer](https://github.com/sdurrheimer)

And many others as most commits now come directly from Docker. Patches
are applied this way:

    $ cd docker/contrib/completion/zsh
    $ git format-patch --stdout -1 d736a9d2c3758fcc4eac0b62e9c7b128388021c1 -- ./_docker | \
        (cd ~/.zsh/third-party/docker-zsh-completion ; git am -p4 )

License (BSD License)
------------------------------

    Copyright (c) 2013, Felix Riedel
    All rights reserved.
    
    Redistribution and use in source and binary forms, with or without
    modification, are permitted provided that the following conditions are met:
        * Redistributions of source code must retain the above copyright
          notice, this list of conditions and the following disclaimer.
        * Redistributions in binary form must reproduce the above copyright
          notice, this list of conditions and the following disclaimer in the
          documentation and/or other materials provided with the distribution.
        * Neither the name of the <organization> nor the
          names of its contributors may be used to endorse or promote products
          derived from this software without specific prior written permission.
    
    THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
    ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
    WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
    DISCLAIMED. IN NO EVENT SHALL <COPYRIGHT HOLDER> BE LIABLE FOR ANY
    DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
    (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
    LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
    ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
    (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
    SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

