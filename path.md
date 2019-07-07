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

## path.join([...paths])
- string을 반환한다.
- path 플랫폼 별 구분기호를 사용하여 지정된 세그먼트들을 모두 join한 경로를 정규화합니다.
- 길이가 0인 path세그먼트는 무시합니다. (문자열 길이가 0이면 '.'현재작업 디렉토리와 같습니다.)
- '..'이면 상위 디렉토리로 이동합니다.(앞에 있는 path세그먼트를 무시하는것과 같음)
```js
path.join('/foo', 'bar', 'baz/asdf', 'quux', '..'); // '..'은 상위 디렉토리로 이동 = 앞의 path세그먼트를 무시
// Returns: '/foo/bar/baz/asdf'

path.join('foo', {}, 'bar');
// Throws 'TypeError: Path must be a string. Received {}'
```
