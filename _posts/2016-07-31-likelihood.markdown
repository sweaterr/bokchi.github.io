---
layout: post
title:  "Likelihood"
date:  2016-07-31 23:52
categories: ml
---

### Likelihood Function
어떤 표본공간<sup>sample space</sup> 에서 정의된 확률변수 \\(A\\)의 값 \\(a\\)의 확률밀도함수는 조건부 확률밀도함수 \\(p(a\|b)\\)로 나타낸다. \\(b\\)는 확률모델의 모수<sup>parameter</sup>로 함수의 모양을 결정짓는다. 이때 우도 함수<sup>likelihood function</sup>의 수식은 확률밀도함수 \\(p(a\|b)\\)의 수식과 완전히 동일하다.

둘의 차이는 함수를 다루는 맥락에 있다. 확률은 \\(a\\)에 대한 함수로 \\( b \\)는 고정된 상수로 취급한다. 반면 우도는 \\(b\\)에 대한 함수로 \\(a\\)가 고정되어 있다고 본다. \\(a\\)가 고정되어 있다는 의미를 담아서 우도를 \\(\mathcal{L}(a\|x)\\)로 나타내기도 하는데 그다지 중요한 사항은 아니다. 수식상 \\(\mathcal{L}(a\|x) =  p(x\|a)\\) 로 정의되기 때문에, 그냥 우도함수 \\(p(a\|b)\\)라고 적으면 된다. 특히, 베이지안 추론에서는 고정된 관측데이터를 가지고 모수를 추정 하기 때문에 보통 \\(p(a\|b)\\)를 우도함수로써 다룬다.

다음의 정규분포 함수를  \\(x\\)에 대한 확률밀도함수로, \\(\mu\\)에 대한 우도함수로 그려보았다.
\\[
p(x|\mu, \sigma) = \frac{1}{\sigma \sqrt {2 \pi }} e^{ { - \left( {x - \mu } \right)^2 } / {2\sigma ^2 } }
\\]

![probability_likelihood](/images/likelihood-fig1.png)


### References
* Doing Bayesian Data Analysis, Second Edition, p125
* https://en.wikipedia.org/wiki/Likelihood_function
* https://en.wikipedia.org/wiki/Probability_density_function
* https://en.wikipedia.org/wiki/Conditional_probability_distribution
