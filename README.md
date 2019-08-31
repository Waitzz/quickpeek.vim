![Screenshot](http://i.andrewradev.com/88051d292a4314f88151f0887c845838.jpg)

## Usage

Turn on/off preview popup (commands only defined in quickfix window):

``` vim
:Quickpeek
:QuickpeekStop
:QuickpeekToggle
```

It's recommended to create a mapping for `QuickpeekToggle`, for instance, in `~/.vim/ftplugin/qf.vim`, you can do this:

``` vim
nnoremap <buffer> <c-p> :QuickpeekToggle<cr>
```

To turn preview popup on automatically, put this in your `.vimrc`:

``` vim
let g:quickpeek_auto = v:true
```

Note that auto mode is currently experimental and results in some weird issues for me sometimes. If you end up with popups hanging around, you can close all of them with `:call popup_close()`.

You can customize the popup that shows up using the `g:quickpeek_popup_options` variable. See the help docs for more details.

## Requirements

The plugin needs Vim with popup window support (v8.1 with a large patch number), otherwise it'll silently do nothing. If you'd like to check if you have popups, try:

``` vim
:echo exists('*popup_create')
```

If you get the value of "1", that means you have popup support.

## Related Work

The [quickr-preview](https://github.com/ronakg/quickr-preview.vim) plugin provides previews of quickfix items in customizable buffers.

## Contributing

Pull requests are welcome, but take a look at [CONTRIBUTING.md](https://github.com/AndrewRadev/quickpeek.vim/blob/master/CONTRIBUTING.md) first for some guidelines. Be sure to abide by the [CODE_OF_CONDUCT.md](https://github.com/AndrewRadev/quickpeek.vim/blob/master/CODE_OF_CONDUCT.md) as well.
