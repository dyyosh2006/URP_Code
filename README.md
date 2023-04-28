# URP_Code
some works with urp

# 湖水渲染

## 浅深水+分层白沫+折射+法线混合+高光+扰动+cubemap反射
![img_v2_51a4ed74-1909-4610-a343-3782f177b00g](https://user-images.githubusercontent.com/22925948/234750196-2a1f7d12-3d24-463c-8d11-04ba1cf96ec7.jpg)
![image](https://user-images.githubusercontent.com/22925948/234749768-123cb7df-3666-41da-9707-8fd12498b755.png)

# 局部平面反射

## renderlayer区分反射层控制，控制vertex.y基于固定平面高度做镜像偏转
![img_v2_eec8eac4-d7e3-47a7-b7ba-0e29d573a0cg](https://user-images.githubusercontent.com/22925948/234751902-1ffe8182-f617-4caa-8270-795ff5856815.jpg)

# 屏幕空间平面反射

## SSPR,基于SSR的一种优化反射方案
https://zhuanlan.zhihu.com/p/353824362

![image](https://user-images.githubusercontent.com/22925948/234754038-d044b050-e2ce-4e0c-af2e-3eece015a232.png)


# 雾效渲染

## 基于后处理的线性雾+高度雾+mask剔除+扰动
![image](https://user-images.githubusercontent.com/22925948/234753795-97572c20-1c5c-4573-b8ce-921e80bd2ec6.png)


# 体积光

## 基于顶点偏移的一种体积光
![image](https://user-images.githubusercontent.com/22925948/234754323-05970a48-3b66-4fb8-a795-5983a4a6271f.png)


# 自定义Shadowmap

## renderfeature+AABB单角色检测+blur+noise+bias+PCSS
![img_v2_6ddcd231-f8c9-452b-8e82-f1edb808306g](https://user-images.githubusercontent.com/22925948/234754888-74e0b246-9f6c-49cb-aa52-07cabc83fb98.jpg)


# 透明材质整合

## 透明prez+单双面单独处理渲染+透明阴影处理
![image](https://user-images.githubusercontent.com/22925948/234755239-2f4fdb1f-5a28-4daa-8e4e-610ff0c7b64d.png)


# 描边方案处理

## 基于sobel+深度检测+法线检测+color检测+ndotV的阈值bug处理+stencilRenderFeature控制分层描边
![img_v2_e3353cd9-4ea9-4501-81d2-42c298c7adbg](https://user-images.githubusercontent.com/22925948/234755607-35e5cde6-92c8-4e9a-92d5-a25e23452e60.jpg)
![img_v2_3535b8fa-4d4f-4262-bcdc-c56a1cd614bg](https://user-images.githubusercontent.com/22925948/234755641-6d3ccb71-d38e-483f-853d-124da66f5ace.jpg)


# 特效基础shader集成

## 基础贴图+颜色映射+扰动+溶解+扭曲+顶点偏移+遮罩+软粒子+shaderGUI

![image](https://user-images.githubusercontent.com/22925948/234756081-b9646634-74b4-461c-9f43-5fe42b3693a7.png)


# 角色渲染

## PBR+NPR+ramptonecolor+rampRimlight+customGI+heightColor+smoothNormaldoubelPassOutline

## kajiyaDiffuse+MarshaSpeluar+flowmap头发

## customcubemap+自定义GI眼睛

## 双层高光+blurN+LUTSSS+customAO皮肤

## clothTilingNormal+fuzzyColor衣服

![image](https://user-images.githubusercontent.com/22925948/234779576-39888353-4ae2-4c7d-b5bd-3714893a54a4.png)


# 实时AO

## SSAO + HBAO + GTAO

性能测试iphone11

SSAO: 

1.35ms = 1.09ms + 146.95us + 113.85us

HBAO:

1.53ms = 965.85us + 298.02us + 266.40us(4等分，步进2次)

GTAO:

1.98ms = 1.37ms + 351.88us + 139.85us + 119.36us

原图

![image](https://user-images.githubusercontent.com/22925948/234782736-944390bb-a2f6-4ea1-925f-5ef97aee0085.png)
![image](https://user-images.githubusercontent.com/22925948/234782765-6a05831f-d835-4dd9-a769-0544faa2dab0.png)
![image](https://user-images.githubusercontent.com/22925948/234782812-3da3cee5-d2cc-4089-856f-7d51e1998fe9.png)
![image](https://user-images.githubusercontent.com/22925948/234782863-131b7312-ef0f-43d0-8965-ed39f344fbd9.png)
![image](https://user-images.githubusercontent.com/22925948/234783083-0ced0d5e-e598-4d45-9051-6167e6bd2bdc.png)
![image](https://user-images.githubusercontent.com/22925948/234783212-f4cb8c98-70f3-428b-b688-ef281e5dc839.png)
![image](https://user-images.githubusercontent.com/22925948/234783248-31a23267-30a7-49c6-8a42-ff328b5176f7.png)


# 折射效果

## renderfeature+maskRT+uberpost

## 可以渲染在半透之后折射，且避开grabpass

![image](https://user-images.githubusercontent.com/22925948/234787690-3d26261b-7d77-4f84-8581-b43c01003279.png)


# 草坪渲染


## DrawMeshInstancedIndirect+wind+AABBCulling+alphaToCoverage+mipmap处理高度太高culling问题+草交互

![image](https://user-images.githubusercontent.com/22925948/234811644-b188cd2a-1000-42df-b692-c1b047348378.png)


https://zhuanlan.zhihu.com/p/625400372


# UI外发光内描边处理

## sobel+alpha检测+blur

![image](https://user-images.githubusercontent.com/22925948/234811444-6f3c62b3-78a4-40c6-b4ae-c34b176f7a9e.png)


https://zhuanlan.zhihu.com/p/266242695


# 地表混合图层优化

## indexmap+特殊处理

https://zhuanlan.zhihu.com/p/625411409

![image](https://user-images.githubusercontent.com/22925948/234811288-e732530f-9ae4-4383-b25f-320ced3fde63.png)


# 海水渲染

## 多层法线融合+高度tiling变化+顶点波形变化+海水退潮痕迹+浅水焦散

![image](https://user-images.githubusercontent.com/22925948/234835274-0be416a5-2e8d-4606-b03d-a353edf2952c.png)



# 写实类特效

## 球形法线固定方向+粒子方向范围+自定义光源方向

![image](https://user-images.githubusercontent.com/22925948/234836578-ada7abca-af1f-498c-9fab-ed2ad8145d49.png)


#  多语种文字合并字体

## 16国语言合并成1个ttf,压缩至5m

https://zhuanlan.zhihu.com/p/625447544

![image](https://user-images.githubusercontent.com/22925948/234840025-c15391f1-2aa4-44c3-867c-023f46e3e5a2.png)


# 前向渲染screenspaceDecal


## stencil控制decal分层 + Z轴面UV处理


![9VP2PY P6BE R_T3 QB4A_F](https://user-images.githubusercontent.com/22925948/235040787-154eef92-f19b-41c8-b81a-10b44126d08f.png)



