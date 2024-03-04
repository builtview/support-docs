---
title: Structured Share Links
description: An explanation of the structured URL for linking to gallery pages and media items
---

BuiltView makes it easy to share and collaborate with your colleagues, and generate reports for documentation purposes.

One of the ways to do this is generating a structured URL which takes you directly to a particular view; for example:

`https://app.builtview.com/gallery/demo?st=DateNewestFirst&m=Video&ds=2020-09-06T14%3A00%3A00.000Z&de=2020-09-10T14%3A00%3A00.000Z&l=0`

or

`https://app.builtview.com/gallery/view/84c7c934-331b-495e-b4da-cf34890bc8d3/VME3f1p?&time=2.33&hfov=150.000`

## Gallery

The URL at app.builtview.com will update as you browse your gallery, so at any time you can copy it and save it somewhere or send to your team members to see the same things you're currently seeing.  

!!! note
    When navigating to a structured link, the user must have access to the Team being viewed.  This also means if you share a link to Private or All Photos & Videos, they may see different content to you.

## Media Items

For individual photos and videos, you can easily create a share link to any item, including a specific point in a video or 360 item, by clicking the Share icon (pictured below) and then "Copy Link".

![Share Media](../assets/functions/image.png)

The link will be structured like this:

`app.builtview.com/gallery/view/{media_id}/{sharecode}?{query}`

The {sharecode} is a short text string unique to that media item which provides perpetual access to any visitor, without needing to sign in or be added to the team.  If a visitor accesses this link,  they will see a restricted form of the media item interface, where they cannot edit, delete or comment on the media, but they can still view the content, see the comments and browse the voiceover (if there is one).

You can also remove the sharecode from the link to create a private link to a single-page view of that media item, accessible only to registered users with access to that media item. 

Query parameters:

* `time` - for videos, the time in seconds to start the video at
* `hfov` - for 360 items, the horizontal field of view in degrees
* `pitch` - For 360 content, this specifies your vertical angle.
* `yaw` - For 360 content, this specifies your horizontal angle.

## Gallery  Views

If you want to share a link to a specific set of items in the gallery, for example after filtering by specific tags, you can use the structured gallery link.

As mentioned above, your URL will update while browsing the gallery, so you can manually set your view and then copy the link so that anyone with access to that team can see it; however, you can also construct the URL manually using the following format:

`https://app.builtview.com/gallery/{team_shorthand}?{query}`

 or

`https://app.builtview.com/iframe/{team_shorthand}?{query}`

Query parameters:

|Parameter|Parameter Name|Description|
|---|---|---|
|`st`|Sort|Sort order for media items; can be one of; DateNewestFirst, DateOldestFirst, UploaderAZ or UploaderZA|
|`t`|Tags|Comma-separated list of tags to filter by|
|`m`|Media Type|Filter by media type, can be `Photo` or `Video`|
|`sr`|Search|String to search by; results will be detected in tags, description, notes and voiceover|
|`u`|Uploaders|Comma-separated list of user IDs, such that only content uploaded by those users is shown|
|`ds`|Date range start|Show no content earlier than this date. Can be specified in a number of formats;  ISO 8601 is preferred, but even "yyyy-mm-dd" works|
|`de`|Date range end|Show no content later than this date. Can be specified in a number of formats;  ISO 8601 is preferred, but even "yyyy-mm-dd" works|

Note that all parameter values should be URL encoded, (for example, "&" becomes %26)