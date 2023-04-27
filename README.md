# URP_Code
some works with urp

湖水渲染

浅深水+分层白沫+折射+法线混合+高光+扰动+cubemap反射
![img_v2_51a4ed74-1909-4610-a343-3782f177b00g](https://user-images.githubusercontent.com/22925948/234750196-2a1f7d12-3d24-463c-8d11-04ba1cf96ec7.jpg)
![image](https://user-images.githubusercontent.com/22925948/234749768-123cb7df-3666-41da-9707-8fd12498b755.png)

局部平面反射

renderlayer区分反射层控制，控制vertex.y基于固定平面高度做镜像偏转
![img_v2_eec8eac4-d7e3-47a7-b7ba-0e29d573a0cg](https://user-images.githubusercontent.com/22925948/234751902-1ffe8182-f617-4caa-8270-795ff5856815.jpg)

屏幕空间平面反射

SSPR,基于SSR的一种优化反射方案
https://zhuanlan.zhihu.com/p/353824362

![image](https://user-images.githubusercontent.com/22925948/234754038-d044b050-e2ce-4e0c-af2e-3eece015a232.png)


雾效渲染

基于后处理的线性雾+高度雾+mask剔除+扰动
![image](https://user-images.githubusercontent.com/22925948/234753795-97572c20-1c5c-4573-b8ce-921e80bd2ec6.png)

