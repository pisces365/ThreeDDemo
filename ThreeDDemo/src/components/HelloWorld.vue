<template>
  <div>
    <canvas id="three"></canvas>
    <div id="label"></div>
  </div>
</template>

<script>
import * as THREE from 'three'
import {GLTFLoader} from 'three/examples/jsm/loaders/GLTFLoader.js'
import {OrbitControls} from 'three/examples/jsm/controls/OrbitControls'
// import {OBJLoader} from 'three/examples/jsm/loaders/OBJLoader.js'
// import {MTLLoader} from 'three/examples/jsm/loaders/MTLLoader.js'

export default {
  data () {
    return {

    }
  },
  mounted () {
    this.initThree()
  },
  methods: {
    initThree () {
      const scene = new THREE.Scene()
      scene.background = new THREE.Color('#eee')
      scene.fog = new THREE.Fog('#eee', 20, 100)

      const canvas = document.querySelector('#three')
      const renderer = new THREE.WebGLRenderer({canvas, antialias: true})
      renderer.shadowMap.enabled = true

      const camera = new THREE.PerspectiveCamera(
        20,
        window.innerWidth / window.innerHeight,
        0.1,
        1000
      )
      camera.position.z = -10
      camera.position.y = 10
      camera.position.x = 10

      var selectObject

      // new MTLLoader().load('/static/house本体.mtl', function (materials) {
      //   materials.preload()
      //   new OBJLoader().setMaterials(materials).load('/static/house本体.obj', function (object) {
      //     object.traverse((child) => {
      //       child.castShadow = true
      //       child.receiveShadow = true
      //     })
      //     scene.add(object)
      //   })
      // })

      const gltfLoader = new GLTFLoader()
      gltfLoader.load('/static/houseonly.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader2 = new GLTFLoader()
      gltfLoader2.load('/static/housedooronly.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader3 = new GLTFLoader()
      gltfLoader3.load('/static/washmachine.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader4 = new GLTFLoader()
      gltfLoader4.load('/static/sofa.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader5 = new GLTFLoader()
      gltfLoader5.load('/static/canzhuo.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader6 = new GLTFLoader()
      gltfLoader6.load('/static/chaji.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader7 = new GLTFLoader()
      gltfLoader7.load('/static/dianshigui.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader8 = new GLTFLoader()
      gltfLoader8.load('/static/chufangzuhe.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader9 = new GLTFLoader()
      gltfLoader9.load('/static/xiaocesuo.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader10 = new GLTFLoader()
      gltfLoader10.load('/static/xiaowoshichuanglian1.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader11 = new GLTFLoader()
      gltfLoader11.load('/static/xiaowoshichuanglian2.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader12 = new GLTFLoader()
      gltfLoader12.load('/static/xiaowoshitaozhuang.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader13 = new GLTFLoader()
      gltfLoader13.load('/static/zhumatong.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader14 = new GLTFLoader()
      gltfLoader14.load('/static/zhuwoshichuanglian1.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader15 = new GLTFLoader()
      gltfLoader15.load('/static/zhuwoshichuanglian2.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader16 = new GLTFLoader()
      gltfLoader16.load('/static/zhuwoshitaozhuang.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader17 = new GLTFLoader()
      gltfLoader17.load('/static/zhuxishouchi.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      const gltfLoader18 = new GLTFLoader()
      gltfLoader18.load('/static/zhuyugang.glb', (gltf) => {
        let model = gltf.scene
        // 遍历模型每部分
        model.traverse((o) => {
          if (o.isMesh) {
            o.castShadow = true
            o.receiveShadow = true
          }
        })
        scene.add(model)
      })

      // const gltfLoader2 = new GLTFLoader()
      // gltfLoader2.load('/static/.gltf', (gltf) => {
      //   let model = gltf.scene
      //   // 遍历模型每部分
      //   model.traverse((o) => {
      //     // 将图片作为纹理加载
      //     let explosionTexture = new THREE.TextureLoader().load(
      //       '/static/2.png'
      //     )
      //     // 调整纹理图的方向
      //     explosionTexture.flipY = false
      //     // 将纹理图生成基础网格材质(MeshBasicMaterial)
      //     const material = new THREE.MeshBasicMaterial({
      //       map: explosionTexture
      //     })
      //     // 给模型每部分上材质
      //     o.material = material
      //     if (o.isMesh) {
      //       o.castShadow = true
      //       o.receiveShadow = true
      //     }
      //   })
      //   scene.add(model)
      // })

      let light = new THREE.AmbientLight(0x000000)
      scene.add(light)

      const hemLight = new THREE.HemisphereLight(0xffffff, 0xffffff, 0.8)
      hemLight.position.set(0, 48, 0)
      scene.add(hemLight)

      const dirLight = new THREE.DirectionalLight(0xffffff, 0.1)
      // 光源等位置
      dirLight.position.set(-4, 8, -5)
      // 可以产生阴影
      dirLight.castShadow = true
      dirLight.shadow.mapSize = new THREE.Vector2(1024, 1024)
      scene.add(dirLight)

      let floorGeometry = new THREE.PlaneGeometry(8000, 8000)
      let floorMaterial = new THREE.MeshPhongMaterial({
        color: 0x857ebb,
        shininess: 0
      })

      let floor = new THREE.Mesh(floorGeometry, floorMaterial)
      floor.rotation.x = -0.5 * Math.PI
      floor.receiveShadow = true
      floor.position.y = -0.001
      scene.add(floor)

      const controls = new OrbitControls(camera, renderer.domElement)
      controls.enableDamping = true
      controls.target = new THREE.Vector3(0, 0, 0)

      function animate () {
        controls.update()
        renderer.render(scene, camera)
        requestAnimationFrame(animate)
        if (selectObject !== undefined && selectObject != null) {
          renderDiv(selectObject)
        }
        if (resizeRendererToDisplaySize(renderer)) {
          const canvas = renderer.domElement
          camera.aspect = canvas.clientWidth / canvas.clientHeight
          camera.updateProjectionMatrix()
        }
      }

      animate()

      function resizeRendererToDisplaySize (renderer) {
        const canvas = renderer.domElement
        var width = window.innerWidth
        var height = window.innerHeight
        var canvasPixelWidth = canvas.width / window.devicePixelRatio
        var canvasPixelHeight = canvas.height / window.devicePixelRatio

        const needResize =
          canvasPixelWidth !== width || canvasPixelHeight !== height
        if (needResize) {
          renderer.setSize(width, height, false)
        }
        return needResize
      }

      // 鼠标双击触发的方法
      function onMouseDblclick (event) {
        // 获取 raycaster 和所有模型相交的数组，其中的元素按照距离排序，越近的越靠前
        var intersects = getIntersects(event)

        // 获取选中最近的 Mesh 对象
        if (intersects.length !== 0 && intersects[0].object instanceof THREE.Mesh) {
          selectObject = intersects[0].object
          changeMaterial(selectObject)
        }
      }

      // 改变对象材质属性
      function changeMaterial (object) {
        var material = new THREE.MeshLambertMaterial({
          color: 0x9089ca,
          transparent: !object.material.transparent,
          opacity: 1
        })
        var materialRecord = object.material
        object.material = material
        setTimeout(function () {
          object.material = materialRecord
        }, 3000)
      }

      // 获取与射线相交的对象数组
      function getIntersects (event) {
        event.preventDefault()
        console.log('event.clientX:' + event.clientX)
        console.log('event.clientY:' + event.clientY)

        // 声明 raycaster 和 mouse 变量
        var raycaster = new THREE.Raycaster()
        var mouse = new THREE.Vector2()

        // 通过鼠标点击位置,计算出 raycaster 所需点的位置,以屏幕为中心点,范围 -1 到 1
        mouse.x = (event.clientX / window.innerWidth) * 2 - 1
        mouse.y = -(event.clientY / window.innerHeight) * 2 + 1

        // 通过鼠标点击的位置(二维坐标)和当前相机的矩阵计算出射线位置
        raycaster.setFromCamera(mouse, camera)

        // 获取与射线相交的对象数组，其中的元素按照距离排序，越近的越靠前
        var intersects = raycaster.intersectObjects(scene.children)

        // 返回选中的对象
        return intersects
      }

      // 窗口变动触发的方法
      function onWindowResize () {
        camera.aspect = window.innerWidth / window.innerHeight
        camera.updateProjectionMatrix()
        renderer.setSize(window.innerWidth, window.innerHeight)
      }

      // 更新div的位置
      function renderDiv (object) {
        // 获取窗口的一半高度和宽度
        var halfWidth = window.innerWidth / 2
        var halfHeight = window.innerHeight / 2

        // 逆转相机求出二维坐标
        var vector = object.position.clone().project(camera)

        // 修改 div 的位置
        document.getElementById('label').style.left = (vector.x + halfWidth) + 'px' // setAttribute("style","left:"+(vector.x * halfWidth + halfWidth))
        document.getElementById('label').style.top = (vector.y + halfHeight) +
          'px' // setAttribute("style","top:"+(-vector.y * halfHeight + halfHeight - object.position.y))
        // - object.position.y
        // 显示模型信息
        document.getElementById('label').innerHTML = ('这是个物体（逻辑还没写好）')
        document.getElementById('label').style.zIndex = 3000
      }

      addEventListener('dblclick', onMouseDblclick, false)
      addEventListener('resize', onWindowResize, false)
    }
  }
}
</script>

<style scoped>
#three {
  width: 100%;
  height: 100%;
  position: fixed;
  left: 0;
  top: 0;
}

#label {
  position: absolute;
  z-index: 100;
  padding: 10px;
  background: rgba(255, 255, 255, 0.6);
  line-height: 1;
  border-radius: 5px;
}
</style>
