# ormolu.el

Format Haskell source code using the [ormolu](https://github.com/tweag/ormolu).

# Usage

With [use-package](https://github.com/jwiegley/use-package/) + [quelpa](https://framagit.org/steckerhalter/quelpa):

```elisp
(use-package ormolu
 :quelpa
 (ormolu
  :fetcher github
  :repo "vyorkin/ormolu.el")
 :hook (haskell-mode . ormolu-mode)
 :custom
 (ormolu-reformat-buffer-on-save t)
 :config
 (nmap 'haskell-mode-map
   "C-c r" 'ormolu-format-buffer))
```

## spacemacs

In `spacemacs/additional-packages`:

```elisp
   (ormolu :location (recipe :fetcher github :repo "grmble/ormolu.el"))
```

