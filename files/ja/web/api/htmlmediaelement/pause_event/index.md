---
title: 'HTMLMediaElement: pause イベント'
slug: Web/API/HTMLMediaElement/pause_event
page-type: web-api-event
tags:
  - Audio
  - Event
  - HTML
  - HTMLMediaElement
  - Media
  - Media Events
  - Pausing
  - Pausing Media
  - Pausing Speech
  - Speech Events
  - Video
  - Web Speech API
  - Web Speech Events
  - pause
  - speech
browser-compat: api.HTMLMediaElement.pause_event
translation_of: Web/API/HTMLMediaElement/pause_event
---
{{APIRef("HTMLMediaElement")}}

`pause` イベントは、動作の一時停止のリクエストが処理され、動作が一時状態に入ったときに送信されるものであり、メディアが要素の {{domxref("HTMLMediaElement.pause", "pause()")}} の呼び出しを通して一時停止した後が最も一般的です。

イベントは `pause()` メソッドから戻り、メディア要素の {{domxref("HTMLMediaElement.paused", "paused")}} プロパティが `true` に変化した後で一度送信されます。

## 基本情報

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">バブリング</th>
      <td>なし</td>
    </tr>
    <tr>
      <th scope="row">キャンセル</th>
      <td>不可</td>
    </tr>
    <tr>
      <th scope="row">インターフェイス</th>
      <td>{{DOMxRef("Event")}}</td>
    </tr>
    <tr>
      <th scope="row">対象</th>
      <td>Element</td>
    </tr>
    <tr>
      <th scope="row">既定のアクション</th>
      <td>なし</td>
    </tr>
    <tr>
      <th scope="row">イベントハンドラープロパティ</th>
      <td>{{domxref("GlobalEventHandlers.onpause")}}</td>
    </tr>
  </tbody>
</table>

## 例

これらの例は、 HTMLMediaElement の `pause` イベントにイベントリスナーを追加してから、イベントが発生したことでイベントハンドラーが動作したときにメッセージをポストします。

`addEventListener()` を使用した例:

```js
const video = document.querySelector('video');

video.addEventListener('pause', (event) => {
  console.log('The Boolean paused property is now true. Either the ' +
  'pause() method was called or the autoplay attribute was toggled.');
});
```

`onpause` イベントハンドラープロパティを使用した例:

```js
const video = document.querySelector('video');

video.onpause = (event) => {
  console.log('The Boolean paused property is now true. Either the ' +
  'pause() method was called or the autoplay attribute was toggled.');
};
```

## 仕様書

{{Specifications}}

## ブラウザーの互換性

{{Compat}}

## 関連イベント

- HTMLMediaElement {{domxref("HTMLMediaElement.playing_event", 'playing')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.waiting_event", 'waiting')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.seeking_event", 'seeking')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.seeked_event", 'seeked')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.ended_event", 'ended')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.loadedmetadata_event", 'loadedmetadata')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.loadeddata_event", 'loadeddata')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.canplay_event", 'canplay')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.canplaythrough_event", 'canplaythrough')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.durationchange_event", 'durationchange')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.timeupdate_event", 'timeupdate')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.play_event", 'play')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.pause_event", 'pause')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.ratechange_event", 'ratechange')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.volumechange_event", 'volumechange')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.suspend_event", 'suspend')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.emptied_event", 'emptied')}} イベント
- HTMLMediaElement {{domxref("HTMLMediaElement.stalled_event", 'stalled')}} イベント

## 関連情報

- {{domxref("HTMLAudioElement")}}
- {{domxref("HTMLVideoElement")}}
- {{HTMLElement("audio")}}
- {{HTMLElement("video")}}
- {{domxref("SpeechSynthesisUtterance")}}
