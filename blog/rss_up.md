# RSS: An alternative way to subscribe uploaders

There is always such a situation: one simply wants to check whether their faviorite uploaders(YouTubers) have updated on socail media, but spends hours watching videos recommended by the smart algorithm.

RSS(Really Simple Syndication) helps to avoid this disturbance and allows people to only focus on the infomation they care about.

Only two things is needed
1. RSS feed (sometimes hard to find)
2. RSS reader

Here I use a the tool [RSSHub](https://docs.rsshub.app) to build my own RSS feed on my server.

![RSSHub](https://raw.githubusercontent.com/wq-peng/repo_image/master/rss_up/icon.png)

---

## Deploy
With `Docker` , one can quickly deploy `RSSHub` service on their servers.

![Deploy](https://raw.githubusercontent.com/wq-peng/repo_image/master/rss_up/deploy.png)

## Route
Here takes [Bilibili](https://www.bilibili.com) for exanple. 
To find route to a Bilibili RSS feeds, one should firstly change the UID of the user accordingly, then change `https://rsshub.app` to `"server IP":1200` to use their own service.

![route](https://raw.githubusercontent.com/wq-peng/repo_image/master/rss_up/route.png)

---

My own RSSHub service was established at `139.196.136.182:1200` , feel free to use, but maintenance is not guaranteed.

Thanks to the [contributors](https://github.com/DIYgod/RSSHub/graphs/contributors) of RSSHub.