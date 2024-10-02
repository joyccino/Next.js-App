# Next.js-App Tutorial

## Hood 선생님's comment - Sep 25 2024
일단 React 자체가 익숙치 않으신 경우라면 Nextjs나 ReactNative를 살펴보기 이전에 React의 기본 라이프 사이클과 철학, 개념 등을 익히고 (Done) 그 다음 Nextjs 프레임워크 실습을 하면 좋을 것 같아요 (Goal Now).

* Tutorial to follow: [https://developer.mozilla.org/ko/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/React_getting_started](https://nextjs.org/learn-pages-router/basics/create-nextjs-app)
* 실습 기간: 2024/10/02 ~ (0일)

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
- Next.JS does code-splitting automatically: 초기 렌더링시 초반에 불필요한 요소 (JS, 라이브러리, 페이지, 컴포넌트 등) 을 코드 스플리팅 통해 나중에 들고옴 => 성능 면에서 매력적.

## 3. Assets, Metadata, and CSS (Oct 02 2024 수)
### Assets
- Files inside 'public' directory can be referenced from the root of the application.
### Metadata
### Third-Party JavaScript
### CSS Styling
### Layout Component
### Global Styles
### Polishing Layout
### Styling Tips

## 4. Pre-rendering and Data Fetching (Oct ? 2024 ?)
### Setup
### Pre-rendering
### Two Forms and Pre-rendering
### Static Generation with and without Data
### Blog Data
### Implement getStaticProps
### getStaticProps Details
### Fetching Data at Request Time

## 5. Dynamic Routes (Oct ? 2024 ?)
### Setup
### Page Path Depends on External Data
### Implement getStaticPaths
### Implement getStaticProps
### Rendering MArkdown
### Polishing the Post Page
### Polishing the Index Page
### DYnamic Routes Details

## 6. API Routes (Oct ? 2024 ?)
### Setup
### Creating API Routes
### API Routes Details

## 7. Deploying your Next.JS App (Oct ? 2024 ?)
### Setup
### Push to GitHub
### Deploy to Vercel
### Next.JS and Vercel
### Other Hosting Options
### Finally
