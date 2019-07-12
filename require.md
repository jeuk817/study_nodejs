# cache
- 모듈을 require할 때 cache에 모듈이 객체로 저장된다.
- 그래서 두번 째 require에서는 cache에 저장되어있는 객체를 가지고 와서 사용한다.
- 이 때문에 서로다른 파일에서 같은 모듈을 require하여 사용하면 cache에 있는 모듈을 공유하여 사용하게 된다.
- 그래서 새롭게 모듈을 require 하고 싶다면 delete require.cache[key]를 사용하여 cache에서 해당 모듈을 지우고 다시 require하는 방법을 사용할 수 있다.