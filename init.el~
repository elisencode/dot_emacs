(require 'package)
(setq package-enable-at-startup nil)
(add-to-list 'package-archives
	     '("melpa" . "https://melpa.org/packages/"))
(package-initialize)

(unless (package-installed-p 'use-package)
  (package-refresh-contents)
  (package-install 'use-package))

(unless (package-installed-p 'spacemacs-theme)
  (package-refresh-contents)
  (package-install 'spacemacs-theme))


;;; ---------- Debugging "Package cl is deprecated" ----------

(setq byte-compile-warnings '(cl-functions))

;;; ----------


;;; ---------- Actual Config File ----------

;;; This is the actual config file. It is omitted if it doesn't exist so emacs won't refuse to launch.
;;; To restarting server, executing Lisp code: type `C-x C-e` at the end of `"~/.emacs.d/config.org")))`
(when (file-readable-p "~/.emacs.d/dot_emacs/config.org")
  (org-babel-load-file (expand-file-name "~/.emacs.d/dot_emacs/config.org")))

;;; ----------


;;; ---------- Installing Emacs and SLIME ----------

;;; https://lisp-lang.org/learn/getting-started/
;;; https://common-lisp.net/project/slime/doc/html/Installation.html

(load (expand-file-name "~/.quicklisp/slime-helper.el"))
;; Replace "sbcl" with the path to your implementation
(setq inferior-lisp-program "sbcl")

;;; ----------


;;; ---------- Custom Setting ----------

(custom-set-variables
 ;; custom-set-variables was added by Custom.
 ;; If you edit it by hand, you could mess it up, so be careful.
 ;; Your init file should contain only one such instance.
 ;; If there is more than one, they won't work right.
 '(ansi-color-faces-vector
   [default default default italic underline success warning error])
 '(custom-enabled-themes '(spacemacs-dark))
 '(custom-safe-themes
   '("bffa9739ce0752a37d9b1eee78fc00ba159748f50dc328af4be661484848e476" default))
 '(package-selected-packages
   '(try magit org-roam yasnippet-snippets yasnippet company-shell slime-company slime company-irony company-c-headers flycheck-clang-analyzer company-jedi pretty-mode expand-region mark-multiple swiper emms popup-kill-ring exwm symon dmenu diminish spaceline company rainbow-delimiters sudo-edit hungry-delete switch-window rainbow-mode avy smex ido-vertical-mode ido-verticle-mode org-bullets beacon spacemacs-theme which-key use-package)))
(custom-set-faces
 ;; custom-set-faces was added by Custom.
 ;; If you edit it by hand, you could mess it up, so be careful.
 ;; Your init file should contain only one such instance.
 ;; If there is more than one, they won't work right.
 '(default ((t (:inherit nil :extend nil :stipple nil :inverse-video nil :box nil :strike-through nil :overline nil :underline nil :slant normal :weight normal :height 143 :width normal :foundry "DAMA" :family "Ubuntu Mono")))))
