![banner](./assets/banner.png)

# @codex_bot notifier

This action sends a notification message to Telegram or Slack chat.

Powered by [@codex_bot/notify](https://github.com/codex-bot/notify) application.

## Inputs

### `webhook`

**Required.** Endpoint for sending message to chat.

### `message`

**Required.** Message text.

### `parse_mode`

Mode for parsing entities in the message text. Empty by default.  

`HTML` or `Markdown` (case insensitive) styles are supported.

### `disable_web_page_preview`

Disables link previews for links in this message. `false` by default.

## Outputs

### `response-body`

Response message

### `response-code`

Response status code

## Usage

```
...
- name: Send a chat notification via @codex_bot
  uses: codex-team/action-codexbot-notify@v1
  with:
    webhook: ${{ secrets.CODEX_BOT_CHAT }}
    message: '📦 [@editorjs/editorjs](https://npmjs.com/package/@editorjs/editorjs) 2.19.0 was published'
    parse_mode: 'markdown'
    disable_web_page_preview: true
...
```