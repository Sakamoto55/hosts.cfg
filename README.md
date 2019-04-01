# hosts.cfg
#nagios hosts.cfg file

;Quicksearch index of machined
; BLADES
; WEB NODES
; DB MACHINES
; DEV/QA
; NGMS MACHINE
; MISC MACHINES
; OFFICE SERVERS
; WEBSITE
; VIPS
; DENVER
;
;------------------------- CORP -----------------------
#define host{
#        use                     generic-host
#        host_name               jira
#        alias                   jira
#        check_command           PING
#        check_interval          1
#        retry_interval          1
#        address                 10.100.4.51
#        max_check_attempts      3
#        check_period            24x7
#        contact_groups          downpage
#        notification_interval   120 
#        notification_period     24x7
#        hostgroups              corp
#}
;------------------------- FILER -----------------------
define host{
        use                     generic-host
        host_name               netapp02
        alias                   netapp02
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.204
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   60
        notification_period     24x7
        hostgroups              dbmachines
}

define host{
        use                     generic-host
        host_name               netapp01
        alias                   netapp01
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.205
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   60
        notification_period     24x7
        hostgroups              dbmachines
}

define host{
        use                     generic-host
        host_name               netapp03
        alias                   netapp03
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.211
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   60
        notification_period     24x7
        hostgroups              dbmachines
}

define host{
        use                     generic-host
        host_name               netapp04
        alias                   netapp04
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.212
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   60
        notification_period     24x7
        hostgroups              dbmachines
}

define host{
        use                     generic-host
        host_name               nagios
        alias                   nagios
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.30
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   0
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               ns1-prod
        alias                   ns1-prod
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.103.1
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   0
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               ns2-prod
        alias                   ns2-prod
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.103.5
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   0
        notification_period     24x7
        hostgroups              misc
}

;------------------------- BLADES -----------------------
define host{
	use			generic-host
	host_name		web01
	alias			web01
	check_command		PING
	check_interval		1
        retry_interval          1
        address                 192.168.100.11
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   0
        notification_period     24x7
        hostgroups              webnodes
}	
define host{
        use                     generic-host
        host_name               web02
        alias                   web02
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.12
        max_check_attempts      5
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              webnodes
}

define host{
        use                     generic-host
        host_name               web03
        alias                   web03
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.221
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              webnodes
}
define host{
        use                     generic-host
        host_name               pmta02
        alias                   pmta02
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.190
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              rmta
}
define host{
        use                     generic-host
        host_name               mp01
        alias                   mp01
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.84
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
#define host{
#        use                     generic-host
#        host_name               blade03-09
#        alias                   blade03-09
#        check_command           PING
#        check_interval          1
#        retry_interval          1
#        address                 192.168.100.19
#        max_check_attempts      3
#        check_period            24x7
#        contact_groups          downpage
#        notification_interval   90
#        notification_period     24x7
#        hostgroups              webnodes
#}
define host{
        use                     generic-host
        host_name               bounce01
        alias                   bounce01
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.20
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              rmta
}
define host{
        use                     generic-host
        host_name               vm0311
        alias                   vm0311
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.21
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              rmta
}
define host{
        use                     generic-host
        host_name               vm0312
        alias                   vm0312
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.22
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              rmta
}
define host{
        use                     generic-host
        host_name               vm0313
        alias                   vm0313
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.23
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               cron01 
        alias                   cron01 
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.212
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               mp03 
        alias                   mp03 
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.61 
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               mcglynn 
        alias                   mcglynn 
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.192 
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               cron02 
        alias                   cron02 
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.27 
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               export01 
        alias                   export01 
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.97 
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               earthworm2 
        alias                   earthworm2 
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.59 
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               earthworm4
        alias                   earthworm4 
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.80
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               earthworm1
        alias                   earthworm1
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.81
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              misc
}

define host{
        use                     generic-host
        host_name               blade04-01
        alias                   blade04-01
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.25
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              webnodes
}
define host{
        use                     generic-host
        host_name               vm0405
        alias                   vm0405
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.29
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              webnodes
}
define host{
        use                     generic-host
        host_name               pmta01
        alias                   pmta01
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.24
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              rmta
}
define host{
        use                     generic-host
        host_name               mp02
        alias                   mp02
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.85
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               blade04-08
        alias                   blade04-08
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.32
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   30
        notification_period     24x7
        hostgroups              webnodes
}
define host{
        use                     generic-host
        host_name               monitor2
        alias                   monitor2
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.33
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        #notification_interval   90
        notification_period     24x7
        hostgroups              webnodes
}
#define host{
#        use                     generic-host
#        host_name               console
#        alias                   console
#        check_command           PING
#        check_interval          1
###        retry_interval          1
#        address                 192.168.100.100
        #max_check_attempts      3
#        check_period            24x7
#        contact_groups          downpage
#        #notification_interval   90
##        notification_period     24x7
#        hostgroups              webnodes
#}
define host{
        use                     generic-host
        host_name               bounce02 
        alias                   bounce02
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.34
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              rmta
}
define host{
        use                     generic-host
        host_name               vm0411
        alias                   vm0411
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.35
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}
define host{
        use                     generic-host
        host_name               vm0412
        alias                   vm0412
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.36
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}
define host{
        use                     generic-host
        host_name               vm0413
        alias                   vm0413
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.37
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               vm0414
        alias                   vm0414
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.38
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}

define host{
        use                     generic-host
        host_name               jenkins
        alias                   jenkins
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.98
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}

define host{
        use                     generic-host
        host_name               jenkins-b
        alias                   jenkins-b
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.86
        max_check_attempts      3
        check_period            24x7
        contact_groups          ops
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}

define host{
        use                     generic-host
        host_name               ngms01
        alias                   ngms01
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.101
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}

define host{
        use                     generic-host
        host_name               ngms02
        alias                   ngms02
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.102
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}

define host{
        use                     generic-host
        host_name               ngms03
        alias                   ngms03
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.103
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}

define host{
        use                     generic-host
        host_name               ngms04
        alias                   ngms04
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.104
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}
define host{
        use                     generic-host
        host_name               ngms05
        alias                   ngms05
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.105
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}
define host{
        use                     generic-host
        host_name               ngms06
        alias                   ngms06
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.106
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}
define host{
        use                     generic-host
        host_name               ngms07
        alias                   ngms07
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.107
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}
define host{
        use                     generic-host
        host_name               ngms08
        alias                   ngms08
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.108
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}

define host{
        use                     generic-host
        host_name               vm0309 
        alias                   vm0309 
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.67
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}
define host{
        use                     generic-host
        host_name               ngms09 
        alias                   ngms09 
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.109
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}
define host{
        use                     generic-host
        host_name               ngms10 
        alias                   ngms10 
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.110
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}
define host{
        use                     generic-host
        host_name               ngms11
        alias                   ngms11
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.111
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}
define host{
        use                     generic-host
        host_name               ngms12
        alias                   ngms12
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.112
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}
define host{
        use                     generic-host
        host_name               ngms13
        alias                   ngms13
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.113
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}
define host{
        use                     generic-host
        host_name               ngms14
        alias                   ngms14
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.114
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              enigma
}

define host{
        use                     generic-host
        host_name               blade01-01
        alias                   blade01-01(webslave01)
        check_command           PING
        check_interval          5
        retry_interval          3
        address                 192.168.100.39
        max_check_attempts      5
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              dbmachines
}
define host{
        use                     generic-host
        host_name               blade01-02
        alias                   blade01-02(backup)
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.40
        max_check_attempts      3
        check_period            24x7
        contact_groups          mikeh
        notification_interval   90
        notification_period     24x7
        hostgroups              dbmachines
}
define host{
        use                     generic-host
        host_name               blade01-04
        alias                   blade01-04 (NGMS carecards slave)
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.42
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              dbmachines
}
#define host{
#        use                     generic-host
#        host_name               blade01-05
#        alias                   blade01-05
#        check_command           PING
#        check_interval          1
#        retry_interval          1
#        address                 192.168.100.43
#        max_check_attempts      3
#        check_period            24x7
#        contact_groups          downpage
#        notification_interval   90
#        notification_period     24x7
#        hostgroups              dbmachines
#}

define host{
        use                     generic-host
        host_name               redis1
        alias                   redis1
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.72
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               redis2
        alias                   redis2
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.74
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               redis3
        alias                   redis3
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.87
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               redis4
        alias                   redis4
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.88
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               redis5
        alias                   redis5
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.89
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               redis6
        alias                   redis6
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.90
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               blade01-12
        alias			blade01-12
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.50
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               blade01-13
        alias                   blade01-13(beslave01)
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.51
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              dbmachines
}
define host{
        use                     generic-host
        host_name               svpdb01
        alias                   svpdb01(master01)
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.52
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              dbmachines
}
define host{
        use                     generic-host
        host_name               blade02-01
        alias                   blade02-01(webslave03)
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.53
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              dbmachines
}
define host{
        use                     generic-host
        host_name               blade02-04
        alias                   blade02-04
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.56
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              dbmachines
}
define host{
        use                     generic-host
        host_name               blade02-10
        alias                   blade02-10
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.63 
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               webslave04
        alias                   webslave04
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.60 
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               utildb
        alias                   utildb
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.13
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               utildb2
        alias                   utildb2
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.49
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               blade02-12
        alias                   blade02-12
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.64
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               blade05-01
        alias                   blade05-01
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.69
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               blade02-13
        alias                   blade02-13(beslave02)
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.65
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              dbmachines
}

define host{
        use                     generic-host
        host_name               svpdb02
        alias                   svpdb02(master-standby)
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.66
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              dbmachines
}
define host{
        use                     generic-host
        host_name               puppet01
        alias                   puppet01
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.75
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               crondb01
        alias                   crondb01
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.119
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              dbmachines
}
define host{
        use                     generic-host
        host_name               crondb02
        alias                   crondb02
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.37
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              dbmachines
}
define host{
        use                     generic-host
        host_name               web04
        alias                   web04
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.222
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              webnodes
}
define host{
        use                     generic-host
        host_name               ws-prod1
        alias                   ws-prod1
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.91
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              webservices
}
define host{
        use                     generic-host
        host_name               ws-prod2
        alias                   ws-prod2
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.92
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              webservices
}
define host{
        use                     generic-host
        host_name               ws-prod3
        alias                   ws-prod3
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.93
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              webservices
}
define host{
        use                     generic-host
        host_name               ws-prod4
        alias                   ws-prod4
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.94
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              webservices
}
define host{
        use                     generic-host
        host_name               ws-prod5
        alias                   ws-prod5
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.47
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              webservices
}
define host{
        use                     generic-host
        host_name               ws-prod6
        alias                   ws-prod6
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.48
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              webservices
}
define host{
        use                     generic-host
        host_name               ws-prod7
        alias                   ws-prod7
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.223
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              webservices
}
define host{
        use                     generic-host
        host_name               ws-prod8
        alias                   ws-prod8
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.224
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              webservices
}
define host{
        use                     generic-host
        host_name               ws-prod9
        alias                   ws-prod9
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.225
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              webservices
}
define host{
        use                     generic-host
        host_name               ws-prod10
        alias                   ws-prod10
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.226
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              webservices
}
define host{
        use                     generic-host
        host_name               archive03
        alias                   archive03
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.58
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   0
        notification_period     24x7
        hostgroups              dbmachines
}
define host{
        use                     generic-host
        host_name               archive04
        alias                   archive04
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.54
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   0
        notification_period     24x7
        hostgroups              dbmachines
}
define host{
        use                     generic-host
        host_name               ops1a
        alias                   ops1a
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 10.100.4.12
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   0
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               syslog
        alias                   syslog
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.103.7
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   0
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               syslog-old
        alias                   syslog-old
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.95
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   0
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               att
        alias                   att 
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 10.100.0.1
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   0
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               redis-backend-s1
        alias                   redis-backend-s1
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.73
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               redis-backend-s2
        alias                   redis-backend-s2
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.14
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               redis-backend-m1
        alias                   redis-backend-m1
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.100
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              misc
}

;----------------- WEBSITE --------------------
define host{
        use                     generic-host
        host_name               www.care2.com
        alias                   www.care2.com
        check_command           check_vhost!8.47.77.87!/!aw4y1n
        check_interval          1
        retry_interval          1
        address                 8.47.77.87
        max_check_attempts      5
        check_period            24x7
        contact_groups          downpage,eng1,eng2
        notification_interval   90
        notification_period     24x7
        hostgroups              websites
}
define host{
        use                     generic-host
        host_name               www.thepetitionsite.com
        alias                   www.thepetitionsite.com
        check_command           check_vhost!www.thepetitionsite.com!/!UA-41501525-1
        check_interval          1
        retry_interval          1
        address                 192.168.103.38
        max_check_attempts      5
        check_period            24x7
        contact_groups          downpage,eng1,eng2
        notification_interval   90
        notification_period     24x7
        hostgroups              websites
}

;---------------- VIPS -----------------------
define host{
        use                     generic-host
        host_name               vip-http-cdn
        alias                   VHTTP cdn.care2.com
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.52
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}

define host{
        use                     generic-host
        host_name               vip-http-care2
        alias                   VHTTP www.care2.com
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.200
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
define host{
        use                     generic-host
        host_name               vip-http-thepetitionsite
        alias                   VHTTP www.thepetitionsite.com
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.201
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
define host{
        use                     generic-host
        host_name               vip-http-webservices
        alias                   VHTTP Web Services
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.102
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
define host{
        use                     generic-host
        host_name               vip-http-maint-page
        alias                   VHTTP Maintenance Page
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.51
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
define host{
        use                     generic-host
        host_name               vip-mysql-backend-slave
        alias                   VMySQL Backend Slave
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.4
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
define host{
        use                     generic-host
        host_name               vip-mysql-ecards-slave
        alias                   VMySQL eCards Slave
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.8
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
define host{
        use                     generic-host
        host_name               vip-mysql-gallery-master
        alias                   VMySQL Gallery Master
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.32
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
define host{
        use                     generic-host
        host_name               vip-mysql-gallery-slave
        alias                   VMySQL Gallery Slave
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.33
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
define host{
        use                     generic-host
        host_name               vip-mysql-mail-master
        alias                   VMySQL Mail Master
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.10
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
define host{
        use                     generic-host
        host_name               vip-mysql-mail-slave
        alias                   VMySQL Mail Slave
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.34
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
define host{
        use                     generic-host
        host_name               vip-mysql-master-master
        alias                   VMySQL Master DB
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.2
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
define host{
        use                     generic-host
        host_name               vip-mysql-ngms-slave
        alias                   VMySQL NGMS Slave
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.14
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
define host{
        use                     generic-host
        host_name               vip-mysql-pm-master
        alias                   VMySQL PM Master
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.11
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
define host{
        use                     generic-host
        host_name               vip-mysql-pm-slave
        alias                   VMySQL PM Slave
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.47
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
define host{
        use                     generic-host
        host_name               vip-mysql-search-slave
        alias                   VMySQL Search Slave
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.7
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
define host{
        use                     generic-host
        host_name               vip-mysql-sessions-slave
        alias                   VMySQL Sessions Slave
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.9
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
define host{
        use                     generic-host
        host_name               vip-mysql-web-slave
        alias                   VMySQL Web Slave
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.101.6
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   90
        notification_period     24x7
        hostgroups              vips
}
#define host{
#        use                     generic-host
#        host_name               unittest1
#        alias                   unittest1
#        check_command           PING
#        check_interval          1
#        retry_interval          1
#        address                 192.168.100.76
#        max_check_attempts      3
#        check_period            24x7
#        contact_groups          downpage
#        notification_interval   0
#        notification_period     24x7
#        hostgroups              misc
#}
#define host{
#        use                     generic-host
#        host_name               unittest2
#        alias                   unittest2
#        check_command           PING
#        check_interval          1
#        retry_interval          1
#        address                 192.168.100.202
#        max_check_attempts      3
#        check_period            24x7
#        contact_groups          downpage
#        notification_interval   0
#        notification_period     24x7
#        hostgroups              misc
#}
#define host{
#        use                     generic-host
#        host_name               unittest3
#        alias                   unittest3
#        check_command           PING
#        check_interval          1
#        retry_interval          1
#        address                 192.168.100.203
#        max_check_attempts      3
#        check_period            24x7
#        contact_groups          downpage
#        notification_interval   0
#        notification_period     24x7
#        hostgroups              misc
#}
#define host{
#        use                     generic-host
#        host_name               edgecast01
 #       alias                   edgecast01
#        check_command           PING
#        check_interval          1
#        retry_interval          1
#        address                 192.168.100.210
#        max_check_attempts      3
#        check_period            24x7
#        contact_groups          downpage
#        notification_interval   0
#        notification_period     24x7
#        hostgroups              misc
#}
#define host{
#        use                     generic-host
#        host_name               vlan-stack
#        alias                   vlan-stack
#        check_command           PING
#        check_interval          1
#        retry_interval          1
#        address                 172.40.255.254
#        max_check_attempts      3
#        check_period            24x7
#        contact_groups          downpage
#        notification_interval   0
#        notification_period     24x7
#        hostgroups              misc
#}
define host{
        use                     generic-host
        host_name               qa-esx02
        alias                   qa-esx02
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.102.190
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   0
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               qa-db01
        alias                   qa-db01
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.102.100
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   0
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               devdb-test
        alias                   devdb-test
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.102.141
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   0
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               vpn-rwc
        alias                   vpn-rwc
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 10.100.2.1
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   0
        notification_period     24x7
        hostgroups              misc
}
define host{
        use                     generic-host
        host_name               vpn-cage
        alias                   vpn-cage
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.102.50
        max_check_attempts      3
        check_period            24x7
        contact_groups          downpage
        notification_interval   0
        notification_period     24x7
        hostgroups              misc
}

define host{
        use                     generic-host
        host_name               tableau-windows
        alias                   tableau-windows
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.117
        max_check_attempts      3
        check_period            24x7
        contact_groups          ops
        notification_interval   0
        notification_period     24x7
        hostgroups              misc
}

define host{
        use                     generic-host
        host_name               ops-windows
        alias                   ops-windows
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 192.168.100.194
        max_check_attempts      3
        check_period            24x7
        contact_groups          ops
        notification_interval   0
        notification_period     24x7
        hostgroups              misc
}

define host{
        use                     generic-host
        host_name               rwc-windows
        alias                   rwc-windows
        check_command           PING
        check_interval          1
        retry_interval          1
        address                 10.100.4.160
        max_check_attempts      3
        check_period            24x7
        contact_groups          ops
        notification_interval   0
        notification_period     24x7
        hostgroups              misc
}

