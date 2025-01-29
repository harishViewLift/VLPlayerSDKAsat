1- For Asat Videos, we need to pass new params `asatVideo = true`

```java
vlPlayer?.setSource(
            "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.....", // Auth Token
            "",
            "tag SamplePlayer",
            videoResponse = videoResponse,
            asatVideo = true // 
        )
```

** Case 1

If we provide `asatVideo = true`, and `Custom Video Response` with Custom URL, then Video SDK will make entitlement api call. If we get monetisation error, then it will throw back error. 
If we get success, then we play asat Video

** Case 2

if we provide `asatVideo = true`, and Video ID = "some Video ID", then it will not play the video. Because we are expecting Custom Video Response for asat.

** Case 3

if we provide `asatVideo = false`, and `Custom Response = null`, then SDK will make api call with videoId provided.

** Note:

We need `asatVideo = true` in order to make beacon event work for ASAT. 

