# today.vim

today-focused todo list in vim.

## Install

Install the plugin [optionally with async.vim] in the usual way (depending on what plugin manager you use).

DEPENDENCY NOTE: `today.vim` depends on a go binary `today`. For now you need `go` on your system to install it (I'll precompile binaries in future)

For example, using vim-plug:

```viml
Plug 'prabirshrestha/async.vim'
Plug 'laher/today.vim', { 'do': ':TodayUpdate' }
```

## Usage

Use one of the following commands to open the 'today' markdown file and add a TODO entry (a 'checkbox' like `[ ]`/`[x]`)

```
:Today                  """ <- just open the file
:TodaySplit             """ <- split-open the file
:TodayPrompt            """ <- add an entry from a prompt 
```

These will add an entry in `g:today_dir` . '/today.md'.


### Usage with FZF/FZM

`today.vim` is compatible with `fzm.vim` (a fuzzy menu system). 
Use via fzm is recommended, for learnability. 
Otherwise, I recommend just mapping some key combinations.

For installing today.vim alongside fzf/fzm:

```viml
Plug 'junegunn/fzf', { 'do': { -> fzf#install() } }
Plug 'junegunn/fzf.vim'
Plug 'laher/fzm.vim'
Plug 'prabirshrestha/async.vim'
Plug 'laher/today.vim', { 'do': ':TodayUpdate' }
```

## Usage 

... _todo_

## Features

Globally available features

| Feature         | Done     | Function       | Notes                 |
|-----------------|----------|----------------|-----------------------|
| Install/Update  | [x]      | :TodayInstall  | |
| Init            | [x]      | :TodayInit     | `today init`. TODO: Automatic?? |
| Open today.md   | [x]      | :TodayOpen     | |
| File Choose     | [x]      | :TodayFz       | |
| New File        | [x]      | :TodayNewFile  | |
| Prompt/split    | [x]      | :TodayPrompt   | |
| Rollover        | [x]      | :TodayRollover | `today rollover`. Only supports 'daily' right now    |
| fzm integration | [x]      |                | |
| docs            | [ ]      |                | README _and_ vim help |
| Scrape `TODO`s  | [ ]      | :TodayScrapeTodos | find TODOs in other files. Add them as items in today.md | 

### Features available within a todo list

Features available on .md files

| Feature         | Done     | Function       | Notes                 |
|-----------------|----------|----------------|-----------------------|
| Refile          | [x]      | :TodayRefile   | |
| Cycle Status    | [ ]      | :TodayCheck    | |
| Insert date etc | [ ]      |                | |
| Move to heading | [ ]      | :TodayMove     | |
