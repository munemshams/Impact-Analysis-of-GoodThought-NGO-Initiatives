**Project Summary**

This project performs a SQL-based analysis of donation activity and assignment performance for GoodThought, an NGO focused on global education, healthcare, and sustainable development initiatives.

The objectives were to:

Identify the top five assignments based on the total value of donations received, categorized by donor type

Determine the highest-impact assignment in each region, limited to assignments that have received at least one donation

These insights help GoodThought understand which initiatives attract the most financial support and which deliver the strongest impact across different regions.

**What This Project Achieved (Using MySQL Only)**

-Joined the assignments, donations, and donors tables to analyze donor behavior

-Calculated total donation amounts grouped by assignment and donor type

-Extracted the top five highest-funded assignments

-Counted the total number of donations per assignment

-Applied SQL window functions to identify the highest-impact assignment in every region

-Filtered out assignments with zero donations to ensure accuracy

-Generated two structured SQL result tables for reporting and insights

**Files Included**

-notebook.ipynb → SQL notebook containing the analysis

-README.md → Project documentation

-highest_donation_assignments.csv → Export of SQL result

-top_regional_impact_assignments.csv → Export of SQL result

**Dataset Structure (SQL Tables)**

The analysis uses three related SQL tables:

assignments
assignment_id, assignment_name, region, impact_score, budget, dates

donations
donation_id, assignment_id, donor_id, amount, donation_date

donors
donor_id, donor_type, donor_name

**SQL Queries Used in the Analysis**

Two SQL queries were used to obtain the required outputs, both included inside the project notebook:

highest_donation_assignments → Top five assignments by total donation amount

top_regional_impact_assignments → Highest-impact assignment per region with at least one donation

**Results Overview**

highest_donation_assignments contains:
assignment_name, region, rounded_total_donation_amount, donor_type

top_regional_impact_assignments contains:
assignment_name, region, impact_score, num_total_donations

Each row in the final outputs represents either:

A top-funded assignment by donor type, or

The highest-impact assignment in its region with at least one donation.
