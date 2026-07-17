---
title: KMP算法实现
published: 2026-07-17
description: 利用C++实现KMP算法,以https://www.luogu.com.cn/problem/P3375为参考
tags: [C++,开发]
category: 算法
draft: false
---

## 以[LuoguProblem-P3375 【模板】KMP](https://www.luogu.com.cn/problem/P3375)为基准

``` cpp
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'
const int N=1e6+10;
int nextt[N]={-1};
string s1,s2;
void tonext(){
	int k=-1;
	for(int i=1;i<s2.size();i++){
		while(k>-1&&s2[i]!=s2[k+1]) k=nextt[k];
		if(s2[i]==s2[k+1]) k++;
		nextt[i]=k;
	}
}
void kmp(){
	tonext();
	int k=-1,len1=s1.size(),len2=s2.size();
	for(int i=0;i<len1;i++){
		while(k>-1&&s1[i]!=s2[k+1]) k=nextt[k];
		if(s1[i]==s2[k+1]) k++;
		if(k==len2-1){
			cout<<i-len2+2<<endl;
		}
	}
	return;
}
signed main(){
	cin>>s1>>s2;
	kmp();
    for(int i=0;i<s2.size();i++) cout<<nextt[i]+1<<' ';
}
```