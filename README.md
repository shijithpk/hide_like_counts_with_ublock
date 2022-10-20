### How to use uBlock Origin to hide like counts on Twitter and karma points on Reddit
This is for people who want to change how Twitter, Tweetdeck and Reddit look on their desktops. Install the [uBlock Origin](https://github.com/gorhill/uBlock) extension for your browser, copy the text below and paste it into uBlock's 'My filters' section. For more info, check the [blog post](https://shijith.com/blog/hiding-like-upvote-counts/).

~~~
! ######## REDDIT.COM ##############
! Hides your karma count on your user profile page on reddit.com
www.reddit.com###profile--id-card--highlight-tooltip--karma

! Hides your user karma in the top right of a page on reddit.com
www.reddit.com##span.Rz5N3cHNgTGZsIQJqBfgk > span

! removes the no. of votes for a post in reddit.com 
www.reddit.com##div[id*=vote-arrows] > div

! removes the comment count for posts in reddit.com
www.reddit.com##i[class*=icon-comment] + span

! removes the karma scores that appears in the popup when you hover over a username in reddit.com
www.reddit.com##div._1Tg84WxamVCCD1zg-nbbP8

! removes karma points from comments on user profile pages
www.reddit.com##span._2ETuFsVzMBxiHia6HfJCTQ._3_GZIIN1xcMEC5AVuv4kfa

! removes karma points and no. of comments for a cross-posted post
www.reddit.com##div._2ED-O3JtIcOqp8iIL1G5cg > div._3Dd3XvAr-WcOJyMTx4y35x

! removes awards next to post titles
www.reddit.com##span._2OYwDdghtXEuTF67C95YLY


! ######## TWITTER.COM ##############

! Hides reply count for tweets in twitter.com
twitter.com##div[aria-label*=Reply] > div > div.css-1dbjc4n.r-xoduu5.r-1udh08x

! Hides retweet count for tweets in twitter.com
twitter.com##div[aria-label*=Retweet] > div > div.css-1dbjc4n.r-xoduu5.r-1udh08x

! Hides like count for tweets in twitter.com
twitter.com##div[aria-label*=Like] > div > div.css-1dbjc4n.r-xoduu5.r-1udh08x

! Removes the followers and following count from user profiles and user popups on twitter.com
twitter.com##div.r-1w6e6rj.r-18u37iz.r-13awgt0.css-1dbjc4n

! Hides the verified tick from accounts in twitter
twitter.com##svg[aria-label="Verified account"]

! Hides info about who an account is followed by on the profile page
twitter.com##a[aria-label="Followers you know"] > div

! Removes counts from tweets in trending sidebar on Twitter
twitter.com##div[data-testid=metadata]

! Removes total tweet counts for a user on their profile page
twitter.com##div.css-1dbjc4n.r-1habvwh > div[dir=auto].css-901oao.css-bfa6kz.r-14j79pv.r-37j5jr.r-n6v787.r-16dba41.r-1cwl3u0.r-bcqeeo.r-qvutc0

! Removes "Not followed by anyone you’re following" from a user's profile page
twitter.com##div.css-901oao.r-14j79pv.r-37j5jr.r-n6v787.r-16dba41.r-1cwl3u0.r-bcqeeo.r-qvutc0 > span.css-901oao.css-16my406.r-poiln3.r-bcqeeo.r-qvutc0:has-text(followed)

! Remove "Followed by John Doe and n others" in the "Who to follow" section
   ! Also removes the "Retweeted by John Doe and 29 others" or "John Doe liked" in the home page timeline
twitter.com##div.css-1dbjc4n.r-15zivkp > div.css-1dbjc4n.r-18u37iz

! Removes the reply, retweet and like counts for a tweet on its own page
twitter.com##div.css-1dbjc4n.r-1dgieki.r-1efd50x.r-5kkj8d.r-13awgt0.r-18u37iz.r-tzz3ar.r-s1qlax.r-1yzf0co

! Removes the reply, retweet and like counts for a tweet on its own page -- Version 2
twitter.com##span.r-1b43r93.r-b88u0q.r-1cwl3u0 span.css-901oao.css-16my406.r-poiln3.r-bcqeeo.r-qvutc0


! ######## TWEETDECK.TWITTER.COM ##############

! Hides the verified tick from accounts in tweetdeck in main view
tweetdeck.twitter.com##i[class*=sprite-verified-mini]

! Hides the reply counts for tweets in every column
tweetdeck.twitter.com##span[class*=reply-count]

! Hides the retweet counts for tweets in every column
tweetdeck.twitter.com##span[class*=retweet-count]

! Hides the like counts for tweets in every column
tweetdeck.twitter.com##span[class*=like-count]

! In tweetdeck, if you click on a tweet, you get an enlarged view of the tweet in the column itself with all the reply/like/retweet counts showing. This rule gets rid of them.
tweetdeck.twitter.com##span.js-ticker-value

! In tweetdeck, if you click on a tweet, you get an enlarged view of the tweet in the column itself with all the reply/like/retweet counts showing. This rule gets rid of them. Version 2
tweetdeck.twitter.com##span.r-1enofrn.r-b88u0q.r-1akm30i span.css-901oao.css-16my406.r-poiln3.r-bcqeeo.r-qvutc0

! When viewing a single tweet in a column, if you click on the words 'retweets' or 'likes', it tells you how many people have liked/retweeted that tweet. This rule hides the numbers
tweetdeck.twitter.com##div[class*=social-proof-for-tweet-title]

! Hides the verified tick when viewing a single tweet in a column
tweetdeck.twitter.com##+js(remove-class, badge-verified, span[class*=fullname-badged-container] > b, stay)

! Hides the followers/following stats from the popup that comes when you click on a handle in tweetdeck
tweetdeck.twitter.com##ul[class=prf-stats]

! Hides the verified tick from the popup that comes when you click on the handle
tweetdeck.twitter.com##i[class*=sprite-verified]

! Hides info about who an account is followed by from the popup that comes when you click on the handle
tweetdeck.twitter.com##div[class*=social-proof-container]

~~~
