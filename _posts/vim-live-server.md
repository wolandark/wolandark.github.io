<h1>Vim Live Server</h1>
 A dead-simple live server implementation using [browser-sync](https://www.npmjs.com/package/browser-sync).
 
 Preview your code in your browser as you change it with ease.

<h2>Dependency</h2>
- nodejs 
- npm

Install the `browser-sync` package globally using npm:
```
   sudo npm install -g browser-sync
```

<h1>Installation</h1>
Use your favorite Vim plugin manager to install [vim-live-server](https://github.com/wolandark/vim-live-server).

<h4>Using Vim [packages](https://vimhelp.org/repeat.txt.html#packages)	(**needs Vim 8+**)</h4>
```
git clone https://github.com/wolandark/vim-live-server.git ~/.vim/pack/plugins/start/vim-live-server/
```
<h4>Using [vim-plug](https://github.com/junegunn/vim-plug)</h4>

Add the following line to your plugin configuration in your .vimrc file:
```
Plug 'https://github.com/wolandark/vim-live-server.git'
```
With vimplug you can use this alternative command that uses a post-installation hook to download the browser-sync package from npm automatically:

```
Plug 'https://github.com/wolandark/vim-live-server.git', { 'do': 'sudo npm install -g browser-sync' }
```

<h4>Using [Vundle](https://github.com/VundleVim/Vundle.vim)</h4>

```
Plugin 'https://github.com/wolandark/vim-live-server.git'
```

<h4>Using [Pathogen](https://github.com/tpope/vim-pathogen)</h4>

Clone the vim-live-server repository into your Vim bundle directory:
```
cd ~/.vim/bundle
git clone https://github.com/wolandark/vim-live-server.git
```

<h1>Usage</h1>
Open your index.html file in vim and issue the following in ex-mode. The server will start and bind itself to `localhost:3000`

```
StartBrowserSync
```

To start serving on a specific port, use:
```
StartBrowserSyncOnPort N
StartBrowserSyncOnPort 3009
```

To kill the server on the default port 3000 use this:
```
KillBrowserSync
```
Use this command to kill the server on a certain port:
```
KillBrowserSyncOnPort N
KillBrowserSyncOnPort 3006
```
_Note:
vim-live-server will kill all running instances of browser-sync on [VimLeave](https://vimhelp.org/autocmd.txt.html#VimLeave)._

<h1>Optional keybindings</h1>
```
nmap <F2> :StartBrowserSync <CR>
nmap <F3> :KillBrowserSync <CR>
```

<h1 align="center">Thats it! Enjoy!</h1>

<h1>Demo</h1>
<img src="https://github.com/wolandark/browser-sync/assets/107309764/218cb8a0-459a-43cd-a987-1b43d1fb2b92">

