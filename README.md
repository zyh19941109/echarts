## echarts

### tips

        貌似现在的echarts已经支持resize

### 安装jquery

        npm install jquery

### 安装echarts

        npm install echarts

### 安装jquery-resizable插件

        npm install jquery-resizable-dom

### 引入

        <script src="./echarts.min.js"></script>
        <script src="./jquery.min.js"></script>
        <script src="./jquery-resizable.min.js"></script>

        import $ from 'jquery'
        import echarts from 'echarts'

### 配置

        // 可根据窗口大小而改变

            // 方法1（引入jq的方法）
            $(window).resize(function(){
                myChart.resize();
            });

            // 方法2（原生的方法）
            window.addEventListener('resize',_=>{
                this.myChart.resize();
            })

            // 方法3（原生的方法）
            window.onresize = function(){
                this.myChart.resize();
            }
        
        /*
            可根据设备窗口大小而改变（没有onresize）
            在打开页面的时候就已经固定尺寸
        */

            //引入jq和jquery-resizable的方法
            $('#main').resizable({
                resizeWidth:true
            });
