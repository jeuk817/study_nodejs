# Path

## path.parse(path)
- 객체를 반환한다.
- 반환된 객체는 다음과 같은 속성을 갖는다.
```js
path.parse('/home/user/dir/file.txt');
return :
// { root: '/',
//   dir: '/home/user/dir',
//   base: 'file.txt',
//   name: 'file',
//   ext: '.txt' }
```

- Windows의 경우
```js
path.parse('C:\\path\\dir\\file.txt');
// Returns:
// { root: 'C:\\',
//   dir: 'C:\\path\\dir',
//   base: 'file.txt',
//   name: 'file',
//   ext: '.txt' }
```
