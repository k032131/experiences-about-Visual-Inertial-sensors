# 
The contents in this file are referenced from https://github.com/ethz-asl/mav_tools_public/wiki/Visual-Inertial-Sensors.

<p>Visual inertial sensors are a popular sensor choice for SLAM due to a large number of advantages over other sensor setups</p>
<ul>
<li>Unlike monocular SLAM, the maps have an absolute scale.</li>
<li>State estimation and feature tracking is more robust to motion blur and fast rotations than visual only systems.</li>
<li>IMU predictions can be used to give near instant state-estimates at over 100 Hz.</li>
<li>The setup is cheaper, smaller, lighter and lower power then lidar or stereo setups.</li>
</ul>
<p>However, there are two large downsides</p>
<ul>
<li>Small errors in the relative timestamps of the IMU and camera can cause large errors or divergence in the state estimation</li>
<li>The system must continually estimate and compensate for biases in the IMU readings.</li>
</ul>
<p>Some odometry systems (e.g. VINS mono) will attempt to compensate for timing errors, while others (e.g. ROVIO) require that all timestamps are accurate.</p>
<h1>
<a id="user-content-timestamp-accuracy" class="anchor" href="#timestamp-accuracy" aria-hidden="true"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true">

