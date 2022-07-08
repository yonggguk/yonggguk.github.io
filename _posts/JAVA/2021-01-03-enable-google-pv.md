---
title: Enable Google Page Views
author: sille_bille
date: 2021-01-03 18:32:00 -0500
categories: [JAVA]
tags: [google analytics, pageviews]
---


This post is to enable Page Views on the [**Chirpy**][chirpy-homepage] theme based blog that you just built. This requires technical knowledge and it's recommended to keep the `google_analytics.pv.*` empty unless you have a good reason. If your website has low traffic, the page views count would discourage you to write more blogs. With that said, let's start with the setup.

## set up Google Analytics

### create GA account and property

First, you need to set up your account on Google analytics. While you create your account, you must create your first **Property** as well.

1. Head to <https://analytics.google.com/> and click on **Start Measuring**
2. Enter your desired _Account Name_ and choose the desired checkboxes
3. Enter your desired _Property Name_. This is the name of the tracker project that appears on your Google Analytics dashboard
4. Enter the required information _About your business_
5. Hit _Create_ and accept any license popup to set up your Google Analytics account and create your property

### create Data Stream

With your property created, you now need to set up Data Stream to track your blog traffic. After you signup, the prompt should automatically take you to create your first **Data Stream**. If not, follow these steps:

1. Go to **Admin** on the left column
2. Select the desired property from the drop-down on the second column
3. Click on **Data Streams**
4. Add a stream and click on **Web**
5. Enter your blog's URL

It should look like this:

![google-analytics-data-stream](/posts/20210103/01-google-analytics-data-stream.png){: width="1086" height="542"}

Now, click on the new data stream and grab the **Measurement ID**. It should look something like `G-V6XXXXXXXX`. Copy this to your `_config.yml`{: .filepath} file:

```yaml
google_analytics:
  id: 'G-V6XXXXXXX'   # fill in your Google Analytics ID
  # Google Analytics pageviews report settings
  pv:
    proxy_endpoint:   # fill in the Google Analytics superProxy endpoint of Google App Engine
    cache_path:       # the local PV cache data, friendly to visitors from GFW region
```
{: file="_config.yml"}

When you push these changes to your blog, you should start seeing the traffic on your Google Analytics. Play around with the Google Analytics dashboard to get familiar with the options available as it takes like 5 mins to pick up your changes. You should now be able to monitor your traffic in real time.

![google-analytics-realtime](/posts/20210103/02-google-analytics-realtime.png){: width="616" height="557"}

## ㅅㄷㅅㄷㄴㅅㄴㄷㅅ

넌 와ㅣㄴ얃마엄

### 제발

ㄴ이ㅏ러민아러