``` 
; capslock + J キー ⇒ ← キー
; capslock + L キー ⇒ → キー
; capslock + I キー ⇒ ↑ キー
; capslock + K キー ⇒ ↓ キー

F13 & j::Send, {Blind}{Left}
F13 & l::Send, {Blind}{Right}
F13 & i::Send, {Blind}{Up}
F13 & k::Send, {Blind}{Down}

; capslock + y キー ⇒ Home キー
; capslock + p キー ⇒ End キー
F13 &  y::Send, {Blind}{Home}
F13 &  p::Send, {Blind}{End}



; capslock + Q キー ⇒ deleat キー
; capslock + B キー ⇒ backspace キー
; capslock + E キー ⇒ esc キー
F13 & q::Send, {Blind}{delete}
F13 & b::Send, {Blind}{backspace}
F13 & e::Send, {Blind}{esc}


; F13 + 数字・記号のキー ⇒ Shiftを押しながらと同等の操作
F13 & 1::Send, +1						; Shift + 1 ("!"を入力)
F13 & 2::Send, +2
F13 & 3::Send, +3
F13 & 4::Send, +4
F13 & 5::Send, +5
F13 & 6::Send, +6
F13 & 7::Send, +7
F13 & 8::Send, +8
F13 & 9::Send, +9
 
F13 & -::Send, +-
F13 & ^::Send,{Blind}{~}
F13 & \::Send, +\
 
F13 & @::Send, +@
F13 & [::Send, +[
 
F13 & `;::Send, +`;						;`(バッククォート)はエスケープシーケンス。";"は特殊な意味を持つ記号なので、"`;"と表記する
F13 & vkBA::Send,{Blind}{NumpadMult}	;":"(コロン) ⇒ "*"(アスタリスク) に。一部特殊な記号は特別な表記をする必要がある
F13 & ]::Send, +]
 
F13 & ,::Send, +,
F13 & .::Send, +.
F13 & /::Send, +/
F13 & vkE2::Send,{Blind}{_}				;"\"(バックスラッシュ) ⇒ "_"(アンダーバー) に

F13 & C::Send, ^c				; O ⇒ Ctrl + c (コピー)
F13 & X::Send, ^x				; U ⇒ Ctrl + x (切り取り)
F13 & V::Send, ^v				; O ⇒ Ctrl + v (貼り付け)
F13 & N::Send, ^z				; O ⇒ Ctrl + z (元に戻す)
F13 & M::Send, ^y				; O ⇒ Ctrl + y (前に進む) 

F13 & u::Send, ^+{Left}				; U ⇒ Ctrl + ←
F13 & o::Send, ^+{Right}				; O ⇒ Ctrl + →


;Windows+Space（言語切り替え）無効化
#Space::Return

;Shift+マウスホイール回転で水平スクロール
  +WheelDown::WheelRight ;マウスホイール下回転で、右側に移動
  +WheelUp::WheelLeft ;マウスホイール上回転で、左側に移動
Return




; F, D, S を Shift, Ctrl, Alt に。他キーとの同時押しを有効にするため、特殊な書き方をする必要がある。
F13 & F::
	SetKeyDelay -1
	Send {Blind}{Shift Down}
	return
F13 & F up::
	SetKeyDelay -1
	Send {Blind}{Shift up}
	return
 
F13 & D::
	SetKeyDelay -1
	Send {Blind}{Ctrl Down}
	return
F13 & D up::
	SetKeyDelay -1
	Send {Blind}{Ctrl up}
	return
 
F13 & S::
	SetKeyDelay -1
	Send {Blind}{Alt Down}
	return
F13 & S up::
	SetKeyDelay -1
	Send {Blind}{Alt up}
	return
 
Return



```
