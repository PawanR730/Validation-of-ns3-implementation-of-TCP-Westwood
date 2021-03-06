# Validation of ns3 implementation of TCP-Westwood
<h3>Computer Networks Course Project.</h3>
Brief: TCP Westwood is designed to improve the performance of TCP in wireless networks. It estimates the available bandwidth in the network to adjust its cwnd. In this project, the aim isto validate ns-3 TCP Westwood implementation by comparing the results obtained from it to those obtained by simulating Linux TCP Westwood.
Required experience: C and C++. <br>
Bonus experience: Knowledge of TCP Westwood and TCP implementation in ns-3. <br>
Difficulty: Moderate.<br>
Recommended Reading: <br> ● Direct Code Execution (Link: https://www.nsnam.org/overview/projects/direct-code-execution/) <br>
● Linux kernel code (Link: https://elixir.bootlin.com/linux/v4.4/source/net/ipv4/tcp_westwood.c) <br>
● Tcp Westwood Paper (Link: ​https://dl.acm.org/citation.cfm?id=381704) <br>
● ns-3 code for TCP Westwood (Path: ns-3.xx/src/internet/model/tcp-westwood.{h, cc})
<br>
<br>
<br>
<h3>Team Members</h3>
<a href="https://github.com/failedcoder12/">Divyansh Verma(16CO110)</a><br>

<a href="https://github.com/PawanR730">Pawan Rahangdale(16CO237)</a><br>

<a href="https://github.com/roshanls1997">Roshan lal Sahu(16CO242)</a><br>



# TCP WESTWOOD DCE

Comparison of **ns-3** and **Linux kernel** implemetations of **TCP WESTWOOD** using **Direct Code Execution** (DCE)

# Final Result

- Congestion Window

- Queue Size

We have identified possible resons for the deviation in the results. This can be found [here]()

## Network Topology
Dumbbell Topology - With 2 Routers and 5 nodes on each side of the router

(5 nodes) -- (1 router) -- (1 router) -- (5 nodes)

With each node having a point to point connection to the router


## Configurations
#### Inside the `main` function
- `stack` - ("linux"/"ns3")
- `transport_prot` - TcpWestwood
- `linux_prot` - westwood
- `queue_disc_type` - FIFO

#### Adjustments made
- PRR is enabled

## Files
- `dce-gfc-dumbbell-new.cc` - Merged code for running tcp high speed implementations of ns-3 and linux kernel
- `plot-scripts/plot_cwnd_comparison.sh` - Script to plot congestion window data from ns-3 and linux stacks 
- `plot-scripts/plot_queue_size_comparison.sh` - Script to plot queue size data from ns-3 and linux stacks  
- `plot-scripts/gnuplot_cwnd` - gnuplot commands to plot congestion window data
- `plot-scripts/gnuplot_queue_size` - gnuplot commands to plot queue size data
