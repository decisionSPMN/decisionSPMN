REFERENCE SOURCE
================

Use of influence diagrams to structure medical decisions.
Nease RF Jr, Owens DK. Washington University St Louis, USA
Medical Decision Making. 1997 Jul-Sep;17(3):263-75.


DESCRIPTION OF DATA
===================

Suppose that we wish to analyze the decision
of whether to perform a bacterial culture for
a 15-year-old male patient who presents with sore
throat. Our concern is that the patient may have a
streptococcal infection; failure to treat such an infection
with antibiotics may lead to unnecessary
morbidity, or even to mortality. If the patient’s sore
throat is not due to streptococcal infection, however,
antibiotics will be ineffective and will incur unnecessary
financial costs and health risks. For this example,
we ignore monetary costs and make our decision
based on quality-adjusted life expectancy
QALE). We assume that failure to treat a streptococcal
infection imposes a small but nonzero
chance of developing rheumatic heart disease. We
also assume that early treatment of a streptococcal
infection may reduce the number of days in which
the patient has a sore throat (controversial, although
useful for our example), but imposes a small chance
of death from anaphylaxis.


VARIABLES
=========

('Test_Decision', (['Yes', 'No'], [0, 1]))
('Test_Result', (['Positive', 'NA', 'Negative'], [0, 1, 2]))
('Streptococcal_Infection', (['Strep_absent', 'Strep_present'], [0, 1]))
('Treatment_Decision', (['Yes', 'No'], [0, 1]))
('Rheumatic_Heart_Disease', (['No', 'Yes'], [0, 1]))
('Die_from_Anaphylaxis', (['No', 'Yes'], [0, 1]))
('Days_with_sore_throat', (['Four', 'Three'], [0, 1]))

PARTIAL ORDER
=============
partial_order = [
    ('decision', 'Test_Decision'),    
    ('chance', ['Test_Result']),
    ('decision', 'Treatment_Decision'),  
    ('chance', ['Streptococcal_Infection']),    
    ('chance', ['Rheumatic_Heart_Disease']),
    ('chance', ['Days_with_sore_throat']),
    ('chance', ['Die_from_Anaphylaxis']),    
]