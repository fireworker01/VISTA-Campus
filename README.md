<div style="position: relative; text-align: center;">
  <img src="src/image/show.png" alt="Header Image" style="width: 100%;"/>
  <h1 style="
    position: absolute;
    top: 35%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: black;  /* 改为黑色 */
    border-bottom: none;  /* 移除下划线 */
    box-shadow: none;  /* 移除可能的阴影线 */
    text-shadow: 1px 1px 2px rgba(255,255,255,0.5);  /* 适配黑色的反色阴影 */
    font-size: 2.5em;
    width: 100%;
    margin: 0;  /* 移除默认外边距 */
    padding: 0;  /* 移除默认内边距 */
  ">
    VISTA-Campus: VersatIle SLAM suiTe with All-around Cameras for campus Environment
  </h1>
</div>

In the VISTA-Campus. We have constructed a multi-sensor hardware platform designed to accommodate diverse existing and future perception modalities, thereby addressing limitations in current datasets. Our platform integrates a stereo camera, six wide-angle cameras configured for omnidirectional coverage, two 32-beam LiDAR units, an IMU, and an RTK positioning system. The dataset, collected across campus environments, encompasses data under varying temporal and illumination conditions, diverse pedestrian traffic levels, and distinct scenarios including residential areas and open spaces. It incorporates multiple loop closure detection conditions while providing prolonged and long-distance data sequences, making it particularly suitable for long-term SLAM testing and evaluation. Additionally, we have provided object detection annotations for certain sequences containing densely populated objects.

## <center> Dataset Demo </center>
<!-- 视频方案 -->
<div style="text-align: center; margin-top: 20px;">
  <video controls style="max-width: 80%; border-radius: 8px;">
    <source src="your-video.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <p style="color: #666; font-size: 0.9em;"></p>
</div>

<!-- GIF -->
<!-- <div style="text-align: center; margin-top: 20px;">
  <img src="demo.gif" alt="Dataset Demo" style="max-width: 80%; border-radius: 8px;">
  <p style="color: #666; font-size: 0.9em;">GIF演示说明文字</p>
</div> -->

## <center> Sensor Platform </center>

<div style="display: flex; gap: 20px; justify-content: space-between; margin: 20px 0;">
  <div style="flex: 1;">
    <img src="src/image/car.png" alt="Left Image" style="width: 100%; border-radius: 8px;">
    <p style="text-align: center; color: #666; margin: 8px 0;">Dataset Collection Equipment.</p>
  </div>
  
  <div style="flex: 1;">
    <img src="src/image/vertical.png" alt="Right Image" style="width: 100%; border-radius: 8px;">
    <p style="text-align: center; color: #666; margin: 8px 0;">Sensor Location.</p>
  </div>
</div>

<center> The entire platform uses a shuttle vehicle controlled by a handle as the mobile device, and all sensors are rigidly connected. The sensors used are as follows: </center>

<div style="text-align: center;">
  <ul style="
    display: inline-block;
    text-align: left;
    list-style-type: disc;
    padding-left: 20px;
    /* color: #444; */
    line-height: 1.5;
    margin: 15px 0;
    font-size: 0.95em;
  ">
    <li style="margin: 10px 0;"><strong>1 ×</strong> Stereolabs Zed mini stereo camera, 480 x 360 x 2, 15Hz, 102°(H) x 57°(V) x 118°(D), 1/3” 4MP CMOS, 3.06mm (0.12”) - f/2.0, Electronic synchronized rolling shutter.</li>
    <li style="margin: 10px 0;"><strong>1 ×</strong> 6DOF imu in Zed mini.</li>
    <li style="margin: 10px 0;"><strong>2 ×</strong> Robosense Helios 32 3DLiDARs, 600rpm, 10Hz 360°, 905nm laser wavelength.</li>
    <li style="margin: 10px 0;"><strong>6 ×</strong> SY011HD-V1 RGBwide-angle cameras, 1920 x 1080 x 6, 10Hz, 2.4mm, 143°(H) x 170°(D).</li>
    <li style="margin: 10px 0;"><strong>1 ×</strong> CHCNAV CGI-410 integrated navigation system.</li>
  </ul>
</div>

## <center> Route </center>

<div style="width: 100%; margin: 0; padding: 0;">
  <img src="src/image/route.png" 
       style="width: 100%; 
              height: auto;
              display: block;">
  <p style="text-align: center; margin: 8px 0;">the track of our dataset. Green markers indicate starting points while red marks denote endpoints. </p>
</div>

## <center> Sequence </center>

The complete dataset comprises 13 sequences encompassing variations in illumination conditions, pedestrian/vehicle traffic density, environmental scenarios, sequence durations, and specialized sequences focused on loop closure detection. The detailed sequence classification is shown in the table below.

| Sequence | Time/Light                          | Duration | Distance(km) | Crowded | Scene          | Category |
|----------|-------------------------------------|----------|--------------|---------|----------------|----------|
| 00       | Daytime/Natural Light               | 5'11''   | 1.048        | Y       | Building area  | Common   |
| 01       | Daytime/Natural Light               | 44'04''  | 9.755        | N       | Building area  | Common   |
| 02       | Daytime/Natural Light               | 3'54''   | 0.816        | N       | Open area      | Common   |
| 03       | Dusk/Natural Light & Artificial Light | 6'06''   | 1.003        | Y       | Building area  | Common   |
| 04       | Dusk/Natural Light & Artificial Light | 5'54''   | 1.229        | N       | Building area  | Common   |
| 05       | Dusk/Natural Light & Artificial Light | 4'58''   | 1.078        | N       | Open area      | Common   |
| 06       | Night/Artificial light              | 43'27''  | 9.754        | N       | Building area  | Common   |
| 07       | Night/Artificial light              | 3'03''   | 0.677        | N       | Open area      | Common   |
| 08       | Daytime/Natural Light               | 5'42''   | 1.154        | N       | Building area  | Special  |
| 09       | Daytime/Natural Light               | 4'45''   | 0.955        | N       | Building area  | Special  |
| 10       | Daytime/Natural Light               | 9'46''   | 2.094        | N       | Building area  | Special  |
| 11       | Daytime/Natural Light               | 8'21''   | 1.766        | N       | Building area  | Special  |
| 12       | Daytime/Natural Light               | 4'35''   | 0.886        | N       | Building area  | Special  |

<div style="display: flex; gap: 20px; justify-content: space-between; margin: 20px 0;">
  <div style="flex: 1;">
    <img src="src/image/time_1.png" alt="Left Image" style="width: 100%; border-radius: 8px;">
    <p style="text-align: center; color: #666; margin: 8px 0;">Daytime example.</p>
  </div>
  
  <div style="flex: 1;">
    <img src="src/image/time_2.png" alt="Right Image" style="width: 100%; border-radius: 8px;">
    <p style="text-align: center; color: #666; margin: 8px 0;">Dusk example.</p>
  </div>

  <div style="flex: 1;">
    <img src="src/image/time_3.png" alt="Right Image" style="width: 100%; border-radius: 8px;">
    <p style="text-align: center; color: #666; margin: 8px 0;">Night time example.</p>
  </div>
</div>

<center>
Comparison of different lighting conditions at the same location and time
In the figure, the same location is shown, with a natural light environment during the day (a), a dusk environment with both natural and artificial light sources (b), and a night time environment with only artificial light sources (c). The clarity and visibility of the images captured by the camera will be greatly affected by different light sources at different times.
</center>

## <center> File and Data Formats </center>

<center>
<div style="width: 30%; margin: 0; padding: 0;">
  <img src="src/image/folder.png" 
       style="width: 100%; 
              height: auto;
              display: block;">
  <!-- <p style="text-align: center; margin: 8px 0;"> </p> -->
</div>

### Catalog Layout of a Single Dataset


\<xx> represents the dataset number (ranging from 00 to 12);

\<x> represents the file number (starting from 0);

\<time_stamp> represents a timestamp in the format \<seconds.microseconds>.

</center>

## <center> How to get the data </center>



