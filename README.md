# HAIC_MLProject
Exploring trust and behavior in Human AI collaboration through data analysis.

**PROJECT OVERVIEW**
As AI tools become more integrated into daily workflows, understanding user behavior and trust dynamics is critical.

**This project analyzes:**

1) How often users accept AI outputs
2) How much they edit responses
3) How trust evolves over time
4) Whether users over-rely or under-utilize AI

**DATASET**  
The dataset (human_ai_collab_log.csv) contains interaction logs with features such as:

acceptance -> whether the AI output was accepted  
edit_distance -> how much the output was modified  
ai_response_length  
time_to_edit  
ai_quality -> user-rated quality  
timestamp  

**KEY STEPS**
1) **Data Loading & Exploration**
   Loaded dataset using pandas  
   Initial inspection using .head(), .info(), .describe()  

2) **Feature Engineering**
   New features were created to better capture behavior:

  i)Acceptance Rate  
    Rolling average of acceptance decisions  
  ii)Edit Intensity  
    edit_distance / ai_response_length  
  iii)Efficiency  
    ai_response_length / time_to_edit  
  iv)Normalized AI Quality  
    Scaled between 0 and 1  
  v)Trust Score  
    Composite metric combining acceptance, quality, and edits  

3) **Time Series Analysis**
   Visualized trust score over time  
   Applied rolling averages to observe trends  
   Identified patterns in how user trust evolves  

4) **Behavioral Classification**
   Users were categorized into three types:

  i)Over-reliant  
   Accept low-quality AI responses  
  ii)Under-utilizing  
   Reject high-quality AI responses  
  iii)Well-calibrated  
   Balanced and rational usage  

  5) **Visualizations**
     Trust score over time  
     Rolling trust trends  
     Behavioral distribution  

**INSIGHTS**
1) Trust is not static — it evolves with interaction history
2) Some users show over-reliance, accepting poor AI outputs
3) Others demonstrate under-utilization, rejecting good outputs
4) A balanced user shows calibrated trust, which is ideal
