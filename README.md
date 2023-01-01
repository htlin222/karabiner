# karabiner
my karabiner settings

* [tutorial](https://github.com/yqrashawn/GokuRakuJoudo/blob/master/tutorial.md#advance3)
* [GokuRakuJoudo/examples](https://github.com/yqrashawn/GokuRakuJoudo/blob/master/examples.org#profiles-wip)
* [Karabiner 助力，讓你的鍵盤操作快人一步_少數派 - MdEditor](https://www.gushiciku.cn/pl/a1zX/zh-tw)
* [key definations](https://github.com/yqrashawn/GokuRakuJoudo/blob/master/src/karabiner_configurator/keys_info.clj)
* [great example1](https://github.com/yqrashawn/yqdotfiles/blob/2699f833f9431ca197d50f6905c825712f7aee8d/.config/karabiner.edn#L41)
* [rgomezcasas/dotfiles](https://github.com/rgomezcasas/dotfiles/blob/main/os/mac/karabiner-goku/karabiner.edn)
* [Karabiner | Everything I know](https://wiki.nikiv.dev/macOS/apps/karabiner/)
* [edn-format/edn: Extensible Data Notation](https://github.com/edn-format/edn)

## install
```
brew install yqrashawn/goku/goku
```
## How to find app id
`osascript -e 'id of app "Finder"'`
:applications {:chrome ["^com\\.google\\.Chrome$"]}

## 簡化寫法：
```
    ;; !  | means mandatory -   modifier(s) alone when pressend change behavior
    ;; #  | means optional  -   modifiers are optional (but at least one necessary)

    ;; :!Ca is keycode :a and prefix a with !C

    ;; C  | left_command
    ;; T  | left_control
    ;; O  | left_option
    ;; S  | left_shift
    ;; F  | fn
    ;; Q  | right_command
    ;; W  | right_control
    ;; E  | right_option
    ;; R  | right_shift

    ;; ## | optional any
    ;; !! | command + control + optional + shift (hyper)
```

## Layer

```
;; layers are modifier keys 
;; TODO what are simlayers?
:simlayers {
    :layer-name-mode { :key :o }
} ;; layers

{:des "關於這個層的描述"
	:rules [:layer-name-mode
			[:l [:km "2Do: Capture URL to Read"] :Browsers]
			[:spacebar  [:2do "showToday"]]
			:2do-s-mode
			[:j [:!Cdown_arrow]]
			[:k [:!Cup_arrow]]
			[:v [:!C4]]]}
```

## Template
```
;; you can create templates for running shell commands. These follow clojure string template syntax.
:templates {
    :echo "echo \"%s\""
    :open "open \"%s\""
    :open-app "open -a \"%s\""
} ;; templates
```
