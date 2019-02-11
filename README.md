# [The original file can be found here](https://github.com/mileusna/viber/blob/master/README.md).

# MiXaiLL76 update
 
  * [Remove Webhook](#webhook)
  * [File messages](#file_message)

## Webhook <a id="webhook"></a>

For removing webhook:
[Viber documentation "Removing your webhook"](https://developers.viber.com/docs/api/rest-bot-api/#removing-your-webhook).
```go
v.RemoveWebhook()
```

## Auto File messages <a id="file_message"></a>
Added automatic detection of file type and sending images and video.
Also implemented to send regular files.

```go
// The first parameter is optional. He will go only with the image.
// The second parameter is a link to the file.
// Third, its preview.
m := v.NewFileMessage("test_message", "http://www.images.com/file.doc", "")
//m := v.NewFileMessage("test_message", "http://www.images.com/video.mp4", "http://www.images.com/thumb.jpg")
//m := v.NewFileMessage("test_message", "http://www.images.com/img.jpg", "http://www.images.com/thumb.jpg")
v.SendMessage("test_user_id", m)
```

# P.S.
All work was carried out for personal purposes to integrate Viber and Telegram bots into a single API.