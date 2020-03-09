# kxSurveillanceUnitTestPackage

This is an alert test pack to work off Refinery order and execution tables:
https://confluence.firstderivatives.com/display/KS/Unit+Test+Package




For TR Data Scope files, need kzcat reader:
cp /home/centos/scripts/utils/kzcat.so /home/centos/autodeploy/install/<yourname>/delta-bin/software/KDBPlus_3_6_0/l64/

and to ingest one, run (in non-HDB proc) the following:

(untick the timed query box so diabled timeout)

.al.loadgroupfunctions`kxSurveillanceUnitTests

.test.writeDownTRDataScopeFile[`$"/home/jquinn/kxSurveillanceDailyTAS_lessInstruments.csv.gz"]