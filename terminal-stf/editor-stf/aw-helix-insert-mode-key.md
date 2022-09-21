I did a upgrade form source yesterday

and I cannot use arrow key in `insert mode` since

```
+        "left" => move_char_left,
+        "C-b" => move_char_left,
+        "down" => move_line_down,
+        "up" => move_line_up,
+        "right" => move_char_right,
+        "C-f" => move_char_right,
+        "A-b" => move_prev_word_end,
+        "C-left" => move_prev_word_end,
+        "A-f" => move_next_word_start,
+        "C-right" => move_next_word_start,
+        "A-<" => goto_file_start,
+        "A->" => goto_file_end,
+        "pageup" => page_up,
+        "pagedown" => page_down,
+        "home" => goto_line_start,
+        "C-a" => goto_line_start,
+        "end" => goto_line_end_newline,
+        "C-e" => goto_line_end_newline,
```

Sun Sep 18 20:54:16 CST 2022

---

