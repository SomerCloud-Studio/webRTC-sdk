# webRTC -sdk
## Overview
## Initialize Agora Engine
* This is the first step to use agora SDK. For more information, 
visit docs.agora.io
`
var client = AgoraRTC.createClient({mode: 'live', codec: "h264"});
client.init(<APPID>, function () {
  console.log("AgoraRTC client initialized");
}, function (err) {
  console.log("AgoraRTC client init failed", err);
});
`
## Set Local View
* Now set local view to make video call. Please accept the access request from 
the browser when prompted. 
`
localStream.init(function() {
  console.log("getUserMedia successfully");
  localStream.play('agora_local');
}, function (err) {
  console.log("getUserMedia failed", err);
});
`
