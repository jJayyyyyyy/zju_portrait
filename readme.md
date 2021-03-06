灵感来自于浙大校庆，因为当时浙大同学的头像上都印着校徽，而这个Python小程序可以完成相同功能~

##	Dependency

![badge](https://github.com/jJayyyyyyy/zju_portrait/blob/master/Python-3.4%2B-brightgreen.svg)

```bash
$ pip3 install pillow
```
	
##	Usage

```bash
$ python3 zju_portrait.py octocat.png
```

where `octocat.png` could be any type of image, whose size is better to be larger than 600*600.

##	Demo

<table>
<tr>
<td><img src="./demo/octocat.png" width="320"/>
</td>
<td><img src="./demo/portrait_with_logo.png" width="320"/></td>
<tr>
</table>

##	Workflow

1.  make the input file `portrait.jpg` a square image by adding white space.

2.  resize the image to `640*640`

3.  expand the image to `800*800` by adding white space as its frame

4.  process `logo.png` to get a circle with radius of 100

5.  paste the processed logo onto the bottom-right of the portrait image(that has a white frame)

    ps: the out-of-radius part of the logo has a special alpha value, so it won't be pasted onto the portrait

There is also a [demo](https://github.com/jJayyyyyyy/zju_portrait/tree/master/demo) folder which could help describe the workflow.

##  Reference

*   [alpha band](http://blog.csdn.net/robinzhou/article/details/6960345)

*   [cut a circle](http://www.webtag123.com/python/43461.html)
    
    ps: only part 1 of this page is useful

*   [PIL intro](http://www.cnblogs.com/way_testlife/archive/2011/04/17/2019013.html)

*   [PIL intro2](http://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000/0014320027235877860c87af5544f25a8deeb55141d60c5000)

*   [pillow docs](https://python-pillow.org/)

*   [pillow docs2](http://pillow.readthedocs.io/en/4.1.x/index.html)
