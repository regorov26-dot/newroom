 (cd "$(git rev-parse --show-toplevel)" && git apply --3way <<'EOF' 
diff --git a//dev/null b/login.md
index 0000000000000000000000000000000000000000..93c6d2e5bcb002b8c24631a850727285508577d8 100644
--- a//dev/null
+++ b/login.md
@@ -0,0 +1,20 @@
+---
+layout: default
+title: "Вход в редакцию Своё ТВ"
+---
+
+<h1>Вход в редакцию Своё ТВ</h1>
+
+<form action="/login" method="post">
+  <label>Email: <input type="email" name="email" required></label><br>
+  <label>Пароль: <input type="password" name="password" required></label><br>
+  <button type="submit">Войти</button>
+</form>
+
+<h2>Регистрация</h2>
+<form action="/register" method="post">
+  <label>Имя: <input type="text" name="name" required></label><br>
+  <label>Email: <input type="email" name="email" required></label><br>
+  <label>Пароль: <input type="password" name="password" required></label><br>
+  <button type="submit">Зарегистрироваться</button>
+</form>
 
EOF
)
