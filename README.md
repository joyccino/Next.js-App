# Next.js-App Tutorial

## Hood 선생님's comment - Sep 25 2024
일단 React 자체가 익숙치 않으신 경우라면 Nextjs나 ReactNative를 살펴보기 이전에 React의 기본 라이프 사이클과 철학, 개념 등을 익히고 (Done) 그 다음 Nextjs 프레임워크 실습을 하면 좋을 것 같아요 (Goal Now).

* Tutorial to follow: [https://developer.mozilla.org/ko/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/React_getting_started](https://nextjs.org/learn-pages-router/basics/create-nextjs-app)
* 실습 기간: 2024/10/02 ~ 2024/10/04 (3일)

## 1. Create a Next.js App (Oct 02 2024 수)
### Setup
- Node.js version 18 or higher is required.
- Create the app via following command:
```
npx create-next-app@latest nextjs-blog --use-npm --example "https://github.com/vercel/next-learn/tree/main/basics/learn-starter"
```
- `cd nextjs-blog` then `npm run dev`
- Access `http://localhost:3000` then you will see the starter template page.
![image](https://github.com/user-attachments/assets/cf20c8c3-85a3-4f1a-975f-db116f45bc4f)

### Welcome to Next.js
### Editing the Page
![image](https://github.com/user-attachments/assets/3b103065-c932-46a5-b056-e8a02b204648)

## 2. Navigate Between Pages (Oct 02 2024 수)
### Pages in Next.JS
- In Next.js, a page is a <b>React Component</b> exported from a file in the **pages directory**.
- Create 'pages/posts/first-post.js'.
  
![image](https://github.com/user-attachments/assets/6cd60053-f207-43b7-a932-ddcdc26a35d0)

### Link Component
- We use <a> HTML tag for linking between pages on websites.
- In Next.JS, we can use the 'Link' Component => 'Link' allows us to do client-side navigation + accepts props that gives us better control over the navigation behaviour.

### Client-Side Navigation
- Next.JS does code-splitting automatically: 초기 렌더링시 초반에 불필요한 요소 (JS, 라이브러리, 페이지, 컴포넌트 등) 을 코드 스플리팅 통해 나중에 가져올것 => 성능 면에서 매력적.

## 3. Assets, Metadata, and CSS (Oct 02 2024 수)
### Assets
- Files inside 'public' directory can be referenced from the root of the application.
### Metadata
- Script component 에 additional properties 추가 가능 1) strategy: this controls when the third-party script should load. 2) onLoad: this one's used to run any JS code immediately after the script has finished loading.
### Third-Party JavaScript
### CSS Styling
- Important: To use CSS Modules, the CSS file name must end with .module.css.
### Layout Component
### Global Styles
### Polishing Layout
![image](https://github.com/user-attachments/assets/8454d68a-a204-4f13-9d94-d5a4c655ad5d)

### Styling Tips
- Using 'clsx' library to toggle classes
```
npm install clsx
```
- Next.JS compiles CSS using PostCSS with no configuration
```
npm install -D tailwindcss autoprefixer postcss
```
- Using Sass
```
npm install -D sass
```
## 4. Pre-rendering and Data Fetching (Oct 04 2024 금)
### Pre-rendering
- Data fetching 전에 Next.js 에서 중요한 concept 인 pre-rendering 다룰 것.
1. By default, Next.js pre-renders every page.
2. Next.js generates HTML for each page in advance, instead of having it all done by client-side JS.
3. Therefore, JS 를 disable 후 브라우저로 예시 페이지를 열어도 정상 동작 => 프리렌더링 했기 때문 (pure React.js App 에는 없는 것)
4. Pre-rendering can result in better performance & SEO.
### Two Forms of Pre-rendering
1. **Static Generation** is the pre-rendering method that generates the HTML at *build time*. ![image](https://github.com/user-attachments/assets/c82cf2bd-4f63-4b64-9e40-e7ae87ef0f8b)

2. **Server-side Rendering** is the pre-rendering method generates the HTML on *each request*. ![image](https://github.com/user-attachments/assets/873c0564-4a57-4462-9315-a436cbbd3b84)

![image](https://github.com/user-attachments/assets/6bdb7e0c-b7ac-4012-9be3-76a19cd15328)

### Static Generation with and without Data
![image](https://github.com/user-attachments/assets/3af27d92-104f-4783-806d-b6b8a2afffe4)
- Static Generation with Data using `getStaticProps`.
1. `getStaticProps` is an async function.
2. `getStaticProps` runs at build time in production
3. Inside the function, we can fetch external data and send it as props to the page.
4. `getStaticProps` 가 Next.js 에게 '해당 페이지에 some data dependencies 있으니 build time 에 pre-render 할 때 그 작업을 먼저 resolve 하도록' 알림.

실습 중 markdown file 의 metadata parsing 을 위해 gray-matter 인스톨
```npm install gray-matter```
### Blog Data
### Implement getStaticProps
### getStaticProps Details
### Fetching Data at Request Time
- SWR: The team behind Next.js has created a React hook for data fetching called SWR. Highly recommended if you’re fetching data on the client side. It handles caching, revalidation, focus tracking, refetching on interval, and more.


## 5. Dynamic Routes (Oct 04 2024 금)
### Page Path Depends on External Data
![image](https://github.com/user-attachments/assets/0f3a9214-bc5c-4eca-8c06-32f64e857690)

### Implement getStaticPaths
### Implement getStaticProps
### Rendering Markdown
![image](https://github.com/user-attachments/assets/782dd5ba-5813-4f28-9692-f386e95d8f83)
![image](https://github.com/user-attachments/assets/90fca823-7416-4213-a60e-103e6b5217b0)

### Polishing the Post Page
### Polishing the Index Page
### Dynamic Routes Details

## 6. API Routes (Oct 04 2024 금)
### Creating API Routes
### API Routes Details

## 7. Deploying your Next.JS App (Oct 04 2024 금)
### Setup
### Push to GitHub
### Deploy to Vercel
### Next.JS and Vercel
### Other Hosting Options
### Finally
