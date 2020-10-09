MK=`echo $(MAKE) | $(AWK) '{printf "%5s\n", $$0}' `

all:
	## delete@suy:2020-9-27
	## <anno@suy:2020-9-27> 去掉安装时的freeswitch提示信息
	## 
	## @echo " +---------- FreeSWITCH Build Complete ----------+"
	## @echo " + FreeSWITCH has been successfully built.       +"
	## @echo " + Install by running:                           +"
	## @echo " +                                               +"
	## @echo " +               $(MK) install                   +"
	## @echo " +                                               +"
	## @echo " + While you're waiting, register for ClueCon!   +"
	## @echo " + https://www.cluecon.com                       +"
	## @echo " +                                               +"
	## @echo " +-----------------------------------------------+"
	## @cat $(switch_srcdir)/cluecon2.tmpl
	##
	## <anno@suy end> 
	## delete@suy end

	## create@suy:2020-9-27
	@echo " +---------------- Build Complete ---------------+"
	@echo " + successfully built.                           +"
	@echo " + Install by running:                           +"
	@echo " +                                               +"
	@echo " +               $(MK) install                   +"
	@echo " +                                               +"
	@echo " +-----------------------------------------------+"
	## create@suy end

install:
	## delete@suy:2020-9-27
	## <anno@suy:2020-9-27> 去掉安装时的freeswitch提示信息
	## 
	## @echo " +---------- FreeSWITCH install Complete ----------+"
	## @echo " + FreeSWITCH has been successfully installed.     +"
	## @echo " +                                                 +"
	## @echo " +       Install sounds:                           +"
	## @echo " +       (uhd-sounds includes hd-sounds, sounds)   +"
	## @echo " +       (hd-sounds includes sounds)               +"
	## @echo " +       ------------------------------------      +"
	## @echo " +               $(MK) cd-sounds-install           +"
	## @echo " +               $(MK) cd-moh-install              +"
	## @echo " +                                                 +"
	## @echo " +               $(MK) uhd-sounds-install          +"
	## @echo " +               $(MK) uhd-moh-install             +"
	## @echo " +                                                 +"
	## @echo " +               $(MK) hd-sounds-install           +"
	## @echo " +               $(MK) hd-moh-install              +"
	## @echo " +                                                 +"
	## @echo " +               $(MK) sounds-install              +"
	## @echo " +               $(MK) moh-install                 +"
	## @echo " +                                                 +"
	## @echo " +       Install non english sounds:               +"
	## @echo " +       replace XX with language                  +"
	## @echo " +       (ru : Russian)                            +"
	## @echo " +       (fr : French)                             +"
	## @echo " +       ------------------------------------      +"
	## @echo " +               $(MK) cd-sounds-XX-install        +"
	## @echo " +               $(MK) uhd-sounds-XX-install       +"
	## @echo " +               $(MK) hd-sounds-XX-install        +"
	## @echo " +               $(MK) sounds-XX-install           +"
	## @echo " +                                                 +"
	## @echo " +       Upgrade to latest:                        +"
	## @echo " +       ----------------------------------        +"
	## @echo " +               $(MK) current                     +"
	## @echo " +                                                 +"
	## @echo " +       Rebuild all:                              +"
	## @echo " +       ----------------------------------        +"
	## @echo " +               $(MK) sure                        +"
	## @echo " +                                                 +"
	## @echo " +       Install/Re-install default config:        +"
	## @echo " +       ----------------------------------        +"
	## @echo " +               $(MK) samples                     +"
	## @echo " +                                                 +"
	## @echo " +                                                 +"
	## @echo " +       Additional resources:                     +"
	## @echo " +       ----------------------------------        +"
	## @echo " +       https://www.freeswitch.org                +"
	## @echo " +       https://freeswitch.org/confluence         +"
	## @echo " +       https://freeswitch.org/jira               +"
	## @echo " +       http://lists.freeswitch.org               +"
	## @echo " +                                                 +"
	## @echo " +       irc.freenode.net / #freeswitch            +"
	## @echo " +                                                 +"
	## @echo " +       Register For ClueCon:                     +"
	## @echo " +       ----------------------------------        +"
	## @echo " +       https://www.cluecon.com                   +"
	## @echo " +                                                 +"
	## @echo " +-------------------------------------------------+"
	## @cat $(switch_srcdir)/cluecon2.tmpl
	## @sh $(switch_srcdir)/build/modcheck.sh $(DESTDIR)$(modulesdir)
	## 
	## <anno@suy end> 
	## delete@suy end

	## create@suy:2020-9-27
	@echo " +---------------- install Complete ---------------+"
	@echo " + successfully installed.                         +"
	@echo " +                                                 +"
	@echo " +       Install sounds:                           +"
	@echo " +       (uhd-sounds includes hd-sounds, sounds)   +"
	@echo " +       (hd-sounds includes sounds)               +"
	@echo " +       ------------------------------------      +"
	@echo " +               $(MK) cd-sounds-install           +"
	@echo " +               $(MK) cd-moh-install              +"
	@echo " +                                                 +"
	@echo " +               $(MK) uhd-sounds-install          +"
	@echo " +               $(MK) uhd-moh-install             +"
	@echo " +                                                 +"
	@echo " +               $(MK) hd-sounds-install           +"
	@echo " +               $(MK) hd-moh-install              +"
	@echo " +                                                 +"
	@echo " +               $(MK) sounds-install              +"
	@echo " +               $(MK) moh-install                 +"
	@echo " +                                                 +"
	@echo " +       Install non english sounds:               +"
	@echo " +       replace XX with language                  +"
	@echo " +       (ru : Russian)                            +"
	@echo " +       (fr : French)                             +"
	@echo " +       ------------------------------------      +"
	@echo " +               $(MK) cd-sounds-XX-install        +"
	@echo " +               $(MK) uhd-sounds-XX-install       +"
	@echo " +               $(MK) hd-sounds-XX-install        +"
	@echo " +               $(MK) sounds-XX-install           +"
	@echo " +                                                 +"
	@echo " +       Upgrade to latest:                        +"
	@echo " +       ----------------------------------        +"
	@echo " +               $(MK) current                     +"
	@echo " +                                                 +"
	@echo " +       Rebuild all:                              +"
	@echo " +       ----------------------------------        +"
	@echo " +               $(MK) sure                        +"
	@echo " +                                                 +"
	@echo " +       Install/Re-install default config:        +"
	@echo " +       ----------------------------------        +"
	@echo " +               $(MK) samples                     +"
	@echo " +                                                 +"
	@echo " +-------------------------------------------------+"
	@sh $(switch_srcdir)/build/modcheck.sh $(DESTDIR)$(modulesdir)
	## create@suy end

.PHONY: check dvi html info install-data \
        install-dvi install-exec install-html install-info install-pdf install-ps installcheck installdirs pdf \
        ps uninstall mostlyclean clean distclean maintainer-clean
