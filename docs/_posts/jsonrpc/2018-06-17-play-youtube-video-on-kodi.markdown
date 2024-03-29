---
layout: post
category: jsonrpc
title: How to use Python to play a Youtube video on Kodi?
permalink: /jsonrpc/kodi-youtube
---
<div class="wide-logos" markdown="1">
![kodi](/assets/kodi.png)
![json](/assets/json.png)
</div>

Play a Youtube video on Kodi, by sending a JSON-RPC request with Python.

```sh
pip install requests jsonrpcclient
```

```python
import requests
from jsonrpcclient import request
params = {"file": "plugin://plugin.video.youtube/?action=play_video&videoid=QwSazmPRfaI"}
requests.post("http://kodi:8080/jsonrpc", json=request("Player.Open", params=params))
```

Change the `videoid` to your video.
