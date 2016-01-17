# crm-custom.el --- Alternate `completing-read-multiple` that uses `completing-read`

## Short version

Enable `crm-custom-mode` and `ido-ubiquitous-mode` to get ido
completion for `completing-read-multiple`!

## Longer explanation

If you use a custom completion mechanism such as
`ido-ubiquitous-mode`, you might notice that functions like
`describe-face` don't use it. This is because they use a function
called `completing-read-multiple` to read multiple values at once, and
this function doesn't use the standard completion mechanisms. This
package allows you to use the standard completion mechanisms to
replace `completing-read-multiple`, allowing your custom completion
system to work for functions that use it.

When you turn on `crm-custom-mode`, any command that uses
`completing-read-multiple` will now prompt you again each time you
enter an item. This is because it is reading a list of multiple
items. To end the completion and finish the list of items, simply
enter an empty string.

## Wanted features

This is basically a toy project and I don't have time to work on it,
but it could use the following features to be more user-friendly.

- Ability to go back to previously completed entries by backspacing at
  an empty input (Currently the only recourse if you want to change a
  previously completed entry is to abort and restart the completion)
- Map the separator character to select the curent entry and move on
  to the next one.
