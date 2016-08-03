---
layout: post
title:  "Likelihood"
date:  2016-08-03 13:16
categories: ml
---

### Likelihood Function
조건부 확률함수 \\(p(a\|b)\\)는 \\(b\\)가 주어졌을때 어떤 \\(a\\)가 발생할 확률을 나타낸다. (여기서는 논의상 확률질량함수<sup>probability mass function</sup>, 확률밀도함수<sup>probability density function</sup>의 차이가 없어 확률함수로 통칭하였다.) 이 확률함수는 \\(a\\)에 대한 함수로 \\(b\\)는 고정된 것으로 취급한다. 반대로 \\(b\\)에 대한 함수로써 \\(a\\)가 고정되어 있다고 보면 우도함수<sup>likelihood function</sup>가 된다. 동일한 함수를 관점에 따라 다르게 부르는 것 이다.

물론 \\(a\\)와 \\(b\\)의 값이 특정한 값으로 정해지면 확률함수와 우도함수의 결과 값은 같다. 수식상 같은 함수이니 당연하다. 다시 말하면, \\(p(a\|b)\\)는 \\(a\\)에 대한 확률함수이자, \\(b\\)에 대한 우도함수이다. 같은 함수를 ~에 대한에 따라 이름을 바꾸어 부르는게 어색할 수는 있는데, 그냥 익숙함의 문제일 뿐이다.

우도는 확률이 아니라는 것에 특히 주의해야 한다. 어떤 사건의 발생 가능성을 일상에서 '확률'이라는 용어로 이야기 하는 경우가 많은데, 확률론에서의 정의는 그보다 좀 더 엄격하여 우도와 확률을 분명히 구분하는게 필요하다. \\(a\\)의 확률함수 \\(p(a\|b)\\)는 \\(b\\)가 고정된 상황에서 특정한 \\(a\\)값의 발생 가능성을 숫자로 표현해 주는데, 모든 가능한  \\(a\\)에 대해 함수값을 합하거나 적분하면 정확히 1.0이 얻어진다. 고정해 둔 \\(b\\)값이 무엇이든간에 말이다. 이는 확률함수가 반드시 따라야만하는 성질이다. 반면에 \\(a\\)를 고정하고 모든 \\(b\\)에 대해 함수값을 합하거나 적분하면 무엇이 나올지 정해져있지 않다. 이처럼 우도는 분명 고정된 \\(a\\)하에서 각각의 \\(b\\)가 어느정도의 가능성이 있는지를 나타내지만 확률의 성질을 띄지는 않는다.

둘을 구분하기 위해 우도함수를 \\(\mathcal{L}(b\|a) \\)이나 \\(p_{b}(a)\\)와 같이 표기하기도 하지만, 표현방법은 아무래도 좋다. (사실 정확한 표기법이 뭔지 찾다가 관뒀다.) 문맥상 혼동의 우려가 없으면 \\(p(a\|b)\\)라 쓰고 우도함수로 취급해도 된다.

특히 베이지안 추론에서 \\(p(a\|b)\\) 형태의 우도함수가 자주 등장한다. 베이지안 추론에서는 고정된 관측데이터 하에서 모수<sup>parameter</sup>의 발생확률 \\(p(\theta\|\mathcal{D})\\)을 다룬다. 베이즈 정리를 따르면 이는 \\( p(\\mathcal{D}\|\theta) p(\\mathcal{D}) / p(\theta) \\) 가 되는데, \\( p(\\mathcal{D}\|\theta) \\) 항이 \\(\theta\\)에 대한 우도함수에 해당한다.

추가로, 아래와 같은 베이즈 정리 각 항의 비례관계 설명에서도 혼동이 오기 쉬운데
\\[\text{posterior} \propto \text{likelihood} \times \text{prior} \\]
무엇에 대한 항인지 자세히 써놓고 보면 명확해진다.   
\\\[\text{posterior probability of}\ \theta \propto \text{likelihood of}\ \theta \times \text{prior probability of}\ \theta\\]


예시로 다음의 정규분포식을 \\(x\\)에 대한 확률밀도함수로, \\(\sigma\\)에 대한 우도함수로 각각 그려보았다.
\\[
p(x|\mu, \sigma) = \frac{1}{\sigma \sqrt {2 \pi }} e^{ { - \left( {x - \mu } \right)^2 } / {2\sigma ^2 } }
\\]

![probability_likelihood](/images/likelihood-fig1.png)

당연하게도 형태가 상당히 다르다. 특히 왼쪽그래프는 확률의 특성상 적분하면 1이 얻어지지만 오른쪽 그래프는 1이 얻어지지 않는다. 무슨 값이 나오는지 계산해보진 않았지만 일단 모양이 많이 다르다.

### References
* Bayesian Data Analysis, Second Edition, p9
* Doing Bayesian Data Analysis, Second Edition, p125
* https://en.wikipedia.org/wiki/Likelihood_function
  * 여기의 표기법은 좀 혼동스럽다. 확률, 확률질량함수, 확률밀도함수는 표기법을 구분해놓고 우도는 구분을 안한거 같은데 안해도 될거 같기도 하고..
* https://en.wikipedia.org/wiki/Probability_density_function
* https://en.wikipedia.org/wiki/Conditional_probability_distribution
