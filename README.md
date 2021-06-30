# About vue router

* ## 현재 페이지 확인법
```javascript
this.$router.currentRoute
```
예)  
콘솔 로그시 아래와 같은 정보 반환해주므로 필요한거 찾아서 쓰자
```html
{name: "AutostandMaster", meta: {…}, path: "/autostand-master/1", hash: "", query: {…}, …}
fullPath: "/autostand-master/1"
hash: ""
matched: [{…}]
meta: {}
name: "AutostandMaster"
params: {currentpage: "1"}
path: "/autostand-master/1"
query: {}
__proto__: Object
```
  
* ## 다른 라우터로 이동
   
name에는 지정한 라우터 이름을 쓰면 된다

```javascript
toMyPage() {
  this.$router
    .push({
      name: "MyPage",
    })
    .catch((err) => {});
},
```

* ## 1페이지 전으로 이동
```html
<a @click="$router.go(-1)">back</a>
```
