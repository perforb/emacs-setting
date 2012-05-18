# Emacs settings on Mac

This is the setting of Cocoa Emacs.

## Version

`GNU Emacs 23.2.92.1 (x86_64-apple-darwin10.6.0, NS apple-appkit-1038.35)`

# Submodule

## yasnippet
See <https://github.com/capitaomorte/yasnippet>

    $ mkdir ~/.emacs.d/plugins
    $ git submodule add git://github.com/capitaomorte/yasnippet.git plugins/yasnippet

# Add-On

## auto-install

    $ mkdir ~/.emacs.d/elisp
    $ cd ~/.emacs.d/elisp
    $ wget  http://www.emacswiki.org/emacs/download/auto-install.el

    M-x byte-compile-file auto-install.el

## ELPA

    $ mkdir ~/.emacs.d/elpa

    (install-elisp "http://bit.ly/pkg-el23")

## auto-async-byte-compile

    (install-elisp-from-emacswiki "auto-async-byte-compile.el")

## anything

    (auto-install-batch "anything")

## anything-c-moccur

    (install-elisp-from-emacswiki "color-moccur.el")
    (install-elisp "http://svn.coderepos.org/share/lang/elisp/anything-c-moccur/trunk/anything-c-moccur.el")

## anything-for-tags

    (install-elisp-from-emacswiki "anything-gtags.el")
    (install-elisp-from-emacswiki "anything-exuberant-ctags.el")

## redo+

    (install-elisp-from-emacswiki "redo+.el")

## auto-save-buffers

    (install-elisp "http://homepage3.nifty.com/oatu/emacs/archives/auto-save-buffers.el")

## text-adjust-buffer

    (install-elisp "http://taiyaki.org/elisp/mell/src/mell.el")
    (install-elisp "http://taiyaki.org/elisp/text-adjust/src/text-adjust.el")

### Note
     This domain is not currently being answered.

## igrep

    (install-elisp-from-emacswiki "igrep.el")
    (install-elisp-from-emacswiki "grep-edit.el")

## smartchr

    (install-elisp "https://raw.github.com/imakado/emacs-smartchr/master/smartchr.el")

## sequential-command

    (auto-install-batch "sequential-command")

## auto-complete

    ;; company
    (package-install 'company)

    ;; ac-company
    (install-elisp "https://raw.github.com/buzztaiki/auto-complete/master/ac-company.el")

    ;; auto-complete
    (package-install 'auto-complete)

## Other ELPA Packages

    (package-install 'ctags)
    (package-install 'js2-mode)
    (package-install 'haml-mode)
    (package-install 'php-mode)
    (package-install 'python-mode)
    (package-install 'yaml-mode)

## perl-completion

    (install-elisp "http://www.emacswiki.org/emacs/download/perl-completion.el")

## CakePHP

    (install-elisp "https://raw.github.com/k1LoW/emacs-historyf/master/historyf.el")
    (install-elisp "https://raw.github.com/k1LoW/emacs-cake/master/cake-inflector.el")
    (install-elisp "https://raw.github.com/k1LoW/emacs-cake/master/cake.el")
    (install-elisp "https://raw.github.com/k1LoW/emacs-cake/master/ac-cake.el")
    (install-elisp "https://raw.github.com/k1LoW/emacs-cake2/master/cake2.el")
    (install-elisp "https://raw.github.com/k1LoW/emacs-cake2/master/ac-cake2.el")

## Ruby

    (install-elisp "https://raw.github.com/ruby/ruby/trunk/misc/ruby-electric.el")
    (install-elisp-from-emacswiki "ruby-block.el")
    (install-elisp "https://raw.github.com/ruby/ruby/trunk/misc/inf-ruby.el")

## Markdown

    (install-elisp "http://jblevins.org/projects/markdown-mode/markdown-mode.el")

## Markdown

    $ cd ~/.emacs.d/
    $ mkdir lib
    $ cd lib/
    $ wget http://daringfireball.net/projects/downloads/Markdown_1.0.1.zip
    $ unzip Markdown_1.0.1.zip
    $ mv Markdown_1.0.1/Markdown.pl ./
    $ rm -rf Markdown_*

### append elisp to init.el

    (setq markdown-command "perl /home/.emacs.d/lib/Markdown.pl")
