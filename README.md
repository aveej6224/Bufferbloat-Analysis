# Bufferbloat Analysis (Mininet · Python/Jupyter · Linux VM)

## What’s included
- **Notebooks**:  
  - `bufferbloat-analysis/Assignment2_Notebook.ipynb`  
  - `bufferbloat-analysis/cs24mtech14011_Asg2.ipynb`
- **Experiment & plotting utilities**: `bufferbloat-analysis/{helper.py, monitor.py, plot_ping.py, plot_qsize.py, plot_queue.py, plot_cwnd.py}`, custom Matplotlib defaults in `plot_defaults.py`
- **HTTP demo**: `bufferbloat-analysis/http/{webserver.py, index.html}` 
- **VM setup**: `Vagrantfile`, `setup.sh`, configs in `config_files/`
- **Figures**: example diagrams in `bufferbloat-analysis/figures/`
- **Assignment PDF**: `Programming Assignment 2_ Bufferbloat Analysis .pdf`

## Method (high level)
1. **Topology**: Single bottleneck link with a sized queue (Mininet).  
2. **Load**: Start a long-lived TCP/HTTP flow (iperf/webserver).  
3. **Probing**: Run `ping` in parallel to capture RTT inflation during queue build-up.  
4. **Parsing & Plots**: Parse raw command outputs and visualize RTT vs time, queue occupancy, and cwnd.

## Getting started

### Option A — Vagrant VM (recommended)
1. Install Vagrant (+ provider: VirtualBox/Libvirt).
2. From the repo root:
   ```bash
   vagrant up
   vagrant ssh
