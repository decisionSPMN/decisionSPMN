REFERENCE SOURCE
================

Probability Concepts in Electric Power Systems 
Georgia J. Anders
Wiley, ISBN 0-471-50229-4, 1990


DESCRIPTION OF DATA
===================

The problem, influenced by a problem in Probability Concepts in Electric Power Systems by George Anders, is that a power plant is presented with new air pollution regulations it must meet. There are three options to consider installing: new scrubbers, ordering new cleaner coal and constructing a new transmission line to a hydro plant with excess capacity. The company that would supply the new cleaner coal has a chance that the workers will go on strike. The utility company can decide whether or not to intervene resolving the situation but at an increased cost. 



VARIABLES
=========

('Installation_Type', (['Install_scrubbers', 'New_cleaner_coal'], [0, 1]))
('Coal_Worker_Strike', (['No', 'Yes'], [0, 1]))
('Strike_Resolution', (['Quick', 'Lengthy'], [0, 1]))
('Strike_Intervention', (['Yes', 'No'], [0, 1]))


PARTIAL ORDER
=============

partial_order = [
    ('decision', 'Installation_Type'),    
    ('chance', ['Coal_Worker_Strike']),
    ('decision', 'Strike_Intervention'),
    ('chance', ['Strike_Resolution']),
]