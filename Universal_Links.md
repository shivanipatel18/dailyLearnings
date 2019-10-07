# Universal links

Universal links strengthen the relationship between your website and your mobile app, and allow your users to be taken directly where they want to go.

A universal link is the same web URL, but now your mobile app can handle it and redirect to the appropriate place in your app. After you have implemented universal links, iOS and Android will automatically open your app if they encounter a universal link, such as pasting it into a web browser or tapping a hyperlink in a different app. In Android, universal links are called “app links”.

### Universal links or deep links?

Traditional deep links use custom URL schemes such as my-app://action?parameter=value, which then redirect to the corresponding view in the app. These types of deep links do not always work cross-platform and fail if the user does not have the app installed.

Universal links work the same as custom URL schemes, but they use real web addresses instead. They are still deep links and handled by the app in the same way. In fact if your app uses deep links, then you can most likely reuse a lot of the same code to handle universal links.


#### Advantages of universal links:-

##### 1.Simple:-
Use one URL for both your app and website.

##### 2. Seamless user experience:-
One of the biggest advantages of using universal links is the fall back to web. If a user encounters a universal link and doesn’t have your app installed, then they will be gracefully redirected to the correct place on your website instead.

##### 3.Inter-App Communication:-
Other apps can communicate with your app using universal links, without needing to know if your app is installed.

##### 4.Search Indexing:-
It allows search engines to easily index your content and direct users to your app.

##### 5.Secure and specific: Android App Links use HTTP URLs that link to a website domain you own, so no other app can use your links. One of the requirements for Android App Links is that you verify ownership of your domain through one of our website association methods.


### The general steps for creating Android App Links are as follows:

- Create deep links to specific content in your app: In your app manifest, create intent filters for your website URIs and configure your app to use data from the intents to send users to the right content in your app. Learn more in Create Deep Links to App Content.

- Add verification for your deep links: Configure your app to request verification of app links. Then, publish a Digital Asset Links JSON file on your websites to verify ownership through Google Search Console. Learn more in Verify App Links.


https://developer.android.com/training/app-links
