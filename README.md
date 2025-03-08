```
extends Node

func _ready() -> void:
	# Clear any existing bindings for these actions and re-add them.
	for action in ["ui_up", "ui_down", "ui_left", "ui_right"]:
		if InputMap.has_action(action):
			InputMap.erase_action(action)
		InputMap.add_action(action)
	
	# Create and add a key event for "up" (W)
	var up_event := InputEventKey.new()
	up_event.keycode = KEY_W
	InputMap.action_add_event("ui_up", up_event)
	
	# Create and add a key event for "down" (S)
	var down_event := InputEventKey.new()
	down_event.keycode = KEY_S
	InputMap.action_add_event("ui_down", down_event)
	
	# Create and add a key event for "left" (A)
	var left_event := InputEventKey.new()
	left_event.keycode = KEY_A
	InputMap.action_add_event("ui_left", left_event)
	
	# Create and add a key event for "right" (D)
	var right_event := InputEventKey.new()
	right_event.keycode = KEY_D
	InputMap.action_add_event("ui_right", right_event)

```
