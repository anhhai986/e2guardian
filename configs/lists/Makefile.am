DISTCLEANFILES = Makefile.in \
		bannedphraselist bannedsitelist bannedurllist \
		exceptionphraselist nocheckcertsitelist weightedphraselist \
		newbannedphraselist \
		newexceptionphraselist newweightedphraselist

DGDATADIR = $(DGCONFDIR)/lists

SUBDIRS = newphraselists phraselists . authplugins bannedrooms

if NEED_CSLISTS
SUBDIRS += contentscanners
endif
if NEED_DMLISTS
SUBDIRS += downloadmanagers
endif

WLISTS = addheaderregexplist \
bannedsearchoveridelist \
authexceptionsiteiplist \
authexceptioniplist \
authexceptionsitelist \
authexceptionurllist \
bannedextensionlist \
bannediplist \
bannedclientlist \
bannedmimetypelist \
bannedphraselist \
newbannedphraselist \
bannedregexpheaderlist \
bannedregexpurllist \
bannedregexpuseragentlist \
bannedsearchlist \
bannedsiteiplist \
exceptionvirussiteiplist \
bannedsitelist \
bannedsslsiteiplist \
bannedsslsitelist \
bannedurllist \
contentregexplist \
embededreferersiteiplist \
embededreferersitelist \
embededrefererurllist \
exceptionextensionlist \
exceptionvirusextensionlist \
exceptionfilesiteiplist \
exceptionfilesitelist \
exceptionfileurllist \
exceptioniplist \
exceptionclientlist \
exceptionmimetypelist \
exceptionphraselist \
newexceptionphraselist \
exceptionregexpurllist \
exceptionregexpuseragentlist \
exceptionsiteiplist \
exceptionsitelist \
exceptionregexpheaderlist \
exceptionurllist \
filtergroupslist \
greysiteiplist \
greysitelist \
greysslsiteiplist \
greysslsitelist \
greyurllist \
headerregexplist \
localbannedsearchlist \
localbannedsiteiplist \
localbannedsitelist \
localbannedsslsiteiplist \
localbannedsslsitelist \
localbannedurllist \
localexceptionsiteiplist \
localexceptionsitelist \
localexceptionurllist \
localgreysiteiplist \
localgreysitelist \
localgreysslsiteiplist \
localgreysslsitelist \
localgreyurllist \
logregexpurllist \
logsiteiplist \
logsitelist \
logurllist \
nocheckcertsiteiplist \
nocheckcertsitelist \
refererexceptionsiteiplist \
refererexceptionsitelist \
refererexceptionurllist \
searchregexplist \
sslsiteregexplist \
urlredirectregexplist \
urlregexplist \
ipnobypass \
domainsnobypass \
urlnobypass \
weightedphraselist \
newweightedphraselist
 
EXTRA_DIST = bannedphraselist.in \
newbannedphraselist.in \
bannedsitelist.in \
bannedurllist.in \
exceptionphraselist.in \
newexceptionphraselist.in \
domainsnobypass.in \
urlnobypass.in \
weightedphraselist.in \
newweightedphraselist.in

install-data-local: 
	$(mkinstalldirs) $(DESTDIR)$(DGDATADIR) && \
		for l in $(WLISTS) ; do \
		echo "$(INSTALL_DATA) $$l $(DESTDIR)$(DGDATADIR)/$$l"; \
		$(INSTALL_DATA) $$l $(DESTDIR)$(DGDATADIR)/$$l; \
	done


uninstall-local:
	for l in $(WLISTS) ; do \
		rm -f $(DESTDIR)$(DGDATADIR)/$$l ; \
	done
