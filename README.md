# TMUAV: Datasets for Managing UAV Traffic

This repository provides the datasets used in the paper  
**“Scalable management of unmanned aerial vehicle traffic in dense urban low-altitude airspace”**,  

The datasets support the empirical analyses in the *Discussion* section, including:
1. Efficiency gains of UAV deployment in high-demand urban logistics
2. First- and last-mile delivery performance across cities
3. Accessibility and equity impacts in remote and mountainous regions

All datasets are anonymized and processed for research and reproducibility purposes.

---

Each dataset corresponds to a specific empirical analysis reported in the paper.


## 1. Urban On-Demand Delivery Dataset (Meituan)

**Used in:** Discussion – *Efficiency gains from UAV deployment in high-demand logistics*  

### Description

This dataset contains **anonymized on-demand delivery trips** from Meituan in a third-tier northern Chinese city.  
The data include encrypted pickup–dropoff locations and detailed timestamps of realized courier deliveries.

To evaluate potential UAV performance, UAV delivery analogs are constructed by:
- Extracting origin–destination pairs
- Identifying feasible delivery time windows
- Approximating aerial travel time using Euclidean distance and a nominal cruising speed of 45 km/h

## 2. First- and Last-Mile Delivery Dataset (Cainiao)

**Used in:** Discussion – *Efficiency gains from UAV deployment in logistics*  

### Description

This dataset includes **anonymized parcel delivery records** from Cainiao, covering five Chinese cities:
- Shanghai
- Hangzhou
- Jilin
- Yantai
- Chongqing

The cities span coastal megacities, inland plains, and mountainous regions.

For each origin–destination pair, UAV travel time is estimated using the same assumptions as in the Meituan analysis and compared with recorded courier delivery times.

### Key Fields

- `city`: city name  
- `origin_x, origin_y`: encrypted origin location  
- `destination_x, destination_y`: encrypted destination location  
- `delivery_type`: first-mile or last-mile  
- `courier_time`: observed delivery time  
- `uav_time_est`: estimated UAV travel time  

