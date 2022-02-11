
# Wordpress
WordPress is a free and open-source content management system written in PHP and paired with a MySQL or MariaDB database. Features include a plugin architecture and a template system, referred to within WordPress as Themes

# Testing the wordpress site
There are few steps we can keep in mind while testing a wordpress site. 
* Identify the installed wordpress version and installed plugins

The wordpress instance version can be easily enumerated by wappalyzer

![image](https://user-images.githubusercontent.com/25907213/150394169-c945b54d-71f8-4eba-9106-600b5d89a5a7.png)

* once the version of wordpress has been enumerated, we can search for any CVEs for that specipic version. If found, try to exploit it
* Netx thing we can do is to run a open source tool called wpscan which can be found here https://github.com/wpscanteam/wpscan.git

# Wordpress 

Google dork: `site:https://hackerone.com/reports intext:wordpress`

# checklist for wordpress
 1. check for the outdated wordpress version and related CVEs
 2. check for the outdated plugins and related CVEs
 3. Wordpress theme confusion attack


# H1 disclosed reports
1.Wordpress user admin information discloure
https://hackerone.com/reports/727870

2. Stored XSS 
https://hackerone.com/reports/406289

3. Reflexted XSS 
https://hackerone.com/reports/230234

4. Stored XSS in comment
https://hackerone.com/reports/707720


 # References
 
  #### Youtube 
  https://www.youtube.com/watch?v=C2qEh5NMczo&ab_channel=Nahamsec
  
  #### Blogs
  https://medium.com/@harrmahar/how-i-get-my-first-p1-sensitive-information-disclosure-using-wpscan-c2fba00ac361

  https://corneacristian.medium.com/top-25-wordpress-bug-bounty-reports-f208ea2dad3f
  
  https://medium.com/codex/wordpress-hacking-8b1ed1765d72
  
  
# Tools
https://github.com/wpscanteam/wpscan
  
