# cpython-todo
Backlog of the things I want to do in CPython next, sorted by interestingness in descending order

- [ ] python/cpython#90910 Improve Python Language Reference based on [Köhl 2020]
- [ ] python/cpython#71902 call-matcher breaks if a method is mocked with spec=True
- [x] python/cpython#130827 singledispatchmethod.register fails with typing.Self annotation
- [x] python/cpython#132604 Non-runtime_checkable subclass of a runtime_checkable Protocol allows isinstance()
- [ ] python/cpython#74865 textwrap should treat Unicode em-dash like ASCII em-dash
- [ ] python/cpython#90883 Should shutil functions support bytes paths?
- [ ] python/cpython#132493 Avoid eagerly evaluating annotations

---

Add some syntax error specializations from https://github.com/astral-sh/ruff/tree/728609a06e590e8b458714b4e17d6b16828c21e7/crates/ruff_python_parser/resources/invalid/statements

- [x] this:
  ```py
  match subject:
      case *_:
          pass
  ```
- [x] this:
  ```py
  # Unary addition isn't allowed but we parse it for better error recovery.
  match subject:
      case +1:
          pass
  ```
- [x] this:
  ```py
  with item,: pass
  ```
