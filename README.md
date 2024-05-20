# cats-rock

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Run your unit tests

```
npm run test:unit
```

### Lints and fixes files

```
npm run lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).

### How would you improve page speed load time?

There are some ways to improve page speed load time.

- Optimize Images: First, we need to ensure all images are compressed and in the right format. We can use ImageOptim for reducing file sizes without losing quality.
- Lazy Loading: Also, we can implement lazy loading for images and other heavy content. That means only loading them when they come into the user's view, which can drastically cut down initial load times.
- Caching: Implementing proper caching strategy, like using service workers to cache assets and data on the client-side, can also make a big differ.
  Excep for these, there will be several ways like Reducing Http requests, Using a CDN, etc

### If you use Server Side or Client side rendering what would be some pros and cons (if any) in your chosen method?

In this assessment, I used Client side rendering (CSR).

As far as I know, there will be some pros and cons.

Pros:

- If we use CSR, we only need to send a minimal HTML and necessary assets, and can reduce the load.
- Also, CSR can handle complex, interactive apps more efficiently once the initial load is done.
- It's easier to scale since the server doesn't render HTML for every request.

Cons:

- It takes the time to wait for JavaScript to download and execute before users see anything, which can be slow.
- Also, performance on slow devices, Users with older devices or slow connections might experience poor performance.

Anyway, if we need better SEO and faster initial load times, SSR could be beneficial, although it might be more complex to implement.
On the other hand, if our app is highly interactive and we are targeting users with modern devices, CSR could be a good choice.

At this time, this task has done by using CSR.
