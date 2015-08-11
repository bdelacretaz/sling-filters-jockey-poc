# sling-filters-jockey-poc
Test using service-jockey to change the service properties of Sling filters for SLING-2920

To test this bundle, install it and the companion service-jockey-core bundle, both at start level 1, on
a Sling launchpad instance.

After restarting the instance, the /system/console/status-slingfilter console page shows the 
org.apache.sling.i18n.impl.I18NFilter with a service.ranking of 42, which was injected by the service-jockey
bundle based on the sj.xml file provided by this bundle.

The service-jockey-core bundle is found at https://github.com/bdelacretaz/service-jockey, based on David 
Bosschaert's code which I just Mavenized for this experiment.
