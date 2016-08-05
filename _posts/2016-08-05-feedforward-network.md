---
layout: post
title:  "Neural Network"
date:  2016-08-05 23:39
categories: ml
---

### Feedforward Neural Network
신경망은 [뉴런]({% post_url 2016-08-03-perceptron %})이 층을 이루어 쌓여있는 네트워크이다. 각 층의 뉴런간에는 가중치를 가진 방향성 있는 연결이 존재한다. 입력 뉴런의 층을 입력층<sup>input layer</sup> 출력 뉴런의 층을 출력층<sup>output layer</sup>라 하고 이들 사이에 위치한 층들을 은닉층<sup>hidden layer</sup>라 한다. 층의 개수에는 입,출력 층이 포함된다. 3층이라고 하면 은닉층이 하나인 신경망을 의미한다.

피드포워드 신경망은 뉴런간 연결이 루프를 이루지 않는다. 모든 연결이 입력층에서 출력층 쪽으로만 향해있다. 루프가 있는 네트워크는 순환형 신경망<sup>recurrent nueral network</sup>라 불린다. 순환형 신경망이 두뇌와 더 닮아있는데 아직까지는 좋은 학습알고리즘이 나와있지 않다. 신경망 그림은 여기저기 많이 나와 있으니 생략.

### Heuristics
네트워크 설계에는 딱 떨어진 정답같은게 없어서 많은 휴리스틱들이 필요하다. 0~9사이의 이미지를 입력받아 숫자를 판별하는 3층 신경망을 생각해보자. 입력을 이미지의 픽셀로 주었다면 출력층에는 몇 개의 뉴런을 사용해야할까? 4bit이면 10개 숫자를 표현하고도 남으니 4개로도 가능은 하겠다. 4개의 뉴런을 비트순으로 생각해보면 네 번째 뉴런은 1,3,5,7,9일때 1에 가까운 수를 출력해야한다. 그런데 이 숫자들 사이에는 형태상의 공통점이 별로 없다. 입력인 이미지 픽셀을 홀수라는 특성으로 연결할 단서가 부족한 상황이다. 망의 복잡성이 증가하더라도 숫자마다 하나의 출력을 할당해 10개의 뉴런을 사용하면 더 쉽게 나은 성능을 얻을 수 있다.



### References
1. [http://neuralnetworksanddeeplearning.com/chap1.html](http://neuralnetworksanddeeplearning.com/chap1.html)
2. [http://www.webpages.ttu.edu/dleverin/neural_network/neural_networks.html](http://www.webpages.ttu.edu/dleverin/neural_network/neural_networks.html)
