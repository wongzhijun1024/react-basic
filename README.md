# install the next

```
npx create-next-app@latest

npx create-next-app@latest nextjs-blog --use-npm --example "https://github.com/vercel/next-learn/tree/master/basics/learn-starter"

cd nextjs-blog

npm run dev

```

## 1，Create a New Page

1，Create the `posts` directory under `pages`

2，Create a file called `first-post.js` inside the `posts` directory

```
export default function FirstPost() {
  return <h1>First Post</h1>;
}
```

3，http://localhost:3000/posts/first-post

## 2，Navigate Between Pages

1，import Link

```
import Link from 'next/link';
```

2，change the page

```
<h1 className="title">
  Read <Link href="/posts/first-post">this page!</Link>
</h1>
```

3，change the first-post page

replace its content of pages/posts/first-post

```
import Link from 'next/link';

export default function FirstPost() {
  return (
    <>
      <h1>First Post</h1>
      <h2>
        <Link href="/">Back to home</Link>
      </h2>
    </>
  );
}
```

