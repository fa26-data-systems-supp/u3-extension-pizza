#Dataset
In this project, we plan to use the Museum of Modern Art collection dataset.

#Code authors
Peter Tran, Kate Yu, Chris Wei

#Driving question
How does the Museum of Modern Art’s collection differ from four different departments.
###Sub-questions
How many artworks did each MoMA department collect each decade, and how many different artists created those works in the 21st century?
(We haven’t fully figured out all the subquestions yet, this is just our initial idea)

#Data details
The dataset comes from The Museum of Modern Art’s collection records, published in their GitHub repository. MoMA should be credited for collecting and publishing the data, and Dr. Supp should be credited for introducing the data to us.
The database contains artworks, artist records, artwork-artist relationships, and four departments: Film, Fluxus Collection, Media and Performance, and Painting & Sculpture. It records artwork details, acquisition dates, departments, artist information, and links between artworks and their creators. These figures only describe the subset, not MoMA entire collection.
Our report will focus on data from 2000-2026 as we want to see how MoMA’s collecting pattern changed over time and how many artists are represented in each department.
                                                                                                                                                                                                            
#Brief outline
###Main tables and fields
- artists(constituent_id, display_name, nationality, gender)
- artwork_artists(object_id, constituent_id)
- artworks(object_id, title, date_text, medium, classification, department_id, date_acquired)
- department(department_id, department)

                                                                                                                                    ###Two data problems
- We plan to check whether the data_text column in the artworks table contains different date formats, since it may impact us to analyze data.
- We plan to check whether there are missing values in the classification column in the artworks table. Since our leading question is mainly focusing on different departments, the classification column plays an important role for our following data analysis.

                                                                                                                                    ###3 new sql methods
- CASE WHEN: We plan to use it in the data exploration part, and this new method can help us classify artworks based on their creation year.
- NULLIF: We plan to use it in the data audit part, since it can help convert empty value into NULL. We will mainly use it to check for missing values in the classification and date_text columns.
- WITH (CTE): We plan to use it in the data exploration part, so it can help us calculate and compare the number of artworks across different departments. 


