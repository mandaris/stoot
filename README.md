![stoot logo](documentation/log.png)

# Stoot shortcode

This is a Hugo shortcode that will allow you to embed a mastodon toot into your blog. It's 100% based off of [this post](https://www.brycewray.com/posts/2022/06/static-mastodon-toots-hugo/) by [Bryce Wray](https://www.brycewray.com). I think that you can find updates from the original author by looking at the [git repository](https://github.com/brycewray/hugo-site) for his site. 

My goal is to pull the specific code out so that I can use it on Micro.blog as a plugin for myself and others.

## Usage

The shortcode format looks like the following.

```
{{< stoot instance="$InstanceTLD" id="$Id" >}}
```

You would take the URL for a post such as this `https://social.lol/@mandaris/112944060166510117` and it should look something like the following.

```go
{{< stoot instance="social.lol" id="112944060166510117" >}}
```

and the output will look something like this

![Statically rendered mastodon post](documentation/stoot-basic.png)

The output for a post with multiple images will look like this

![Statically rendered mastodon post with an image](documentation/stoot-multiple-images.png)

The output for a post with sensitive images will look like the following

![Statically rendered mastodon post with sensitive content](documentation/stoot-sensitive-images.png)

The output for post with a poll will look like the following
![Statically rendered mastodon post with a poll](documentation/stoot-poll.png)

## Notes about the plugin

All the code was copy and pasted. I just packaged it up. I didn't make any changes because I'm not familiar with the Go programming language and want to easily get updates from Bryce.

This plugin does not cover the case of text that is content sensitive. 

Also, I _DO_ know that I could use the iframe that mastodon provides to embed a post, but choose this as an option as it better integrates with the style of my blog.

## Version History
1.0.0
: Initial release

1.0.1
: Removed width so that the blockquote expands as needed

1.0.2
: Add new logo