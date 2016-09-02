# ansible-the-unarchiver

Install The Unarchiver via the Mac App Store or Homebrew. Does nothing on non-macOS platforms.

## Role Variables

* `prefer_mas_over_homebrew`: Defaults to `false`.

## Dependencies

* [icopp.mas-cli](https://github.com/icopp/ansible-mas-cli) (included as repository dependency), but only if `prefer_mas_over_homebrew` is `true`.
* [icopp.homebrew-cask](https://github.com/icopp/ansible-homebrew-cask) (included as repository dependency), but only if `prefer_mas_over_homebrew` is `false`.

## Example Playbook

```
  - hosts: all
    roles:
      - role: icopp.the-unarchiver
```

```
  - hosts: all
    roles:
      - role: icopp.the-unarchiver
        prefer_mas_over_homebrew: true
```

## License

MIT
