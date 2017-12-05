# Notes 

Gemfile requirement is best control over resolution.

The old-school `bundle install` conservative updating and the --source hack all comes down to this:
- name it and claim it if you care about it moving.
- https://github.com/chrismo/bundler-source-hack#why-then-does-the-hack-sometimes-not-work
- https://github.com/bundler/bundler/issues/4690#issuecomment-227252419: "If you want bar to stay put, you gotta declare it as a dependency in the Gemfile"

- quick history of rubygems/bundler?
- conservative updates
- - under the hood
- bundle outdated
- bundler-patch
- - unique features
- - vulns
- other bundler interesting bits
- - gem _version_ hack
- - binstubs (rails 4 does this automagically now)
- - checksums
- - bundler/inline
- - bundle config auto_install
- - bundle config suppress_install_using_messages
- - debug dump of stuff
- - troubleshooting a resolution problem?
- - GEM_PATH/GEM_HOME to simulate what bundler does automatically
- - bundler_bungler
- rubytogether
- realcodez.com


# Quick History of Bundler

HT: @indirect - https://www.youtube.com/watch?v=4DqzaqeeMgY

require - 1994
setup.rb - 2000
RubyGems - 2003
- runtime resolution
Bundler - 2009
- install-time resolution

---

# RubyTogether

HT: @indirect - https://www.youtube.com/watch?v=SJddsEfvcW8
http://andre.arko.net/2016/09/26/a-year-of-ruby-together/

Since ~Mar 2015

100,000 gems - 1,000,000 versions

2004-2014 - 2 billion gem downloads
2015 - 4 billion downloads

Bundler has never had more than 2 people working on it, mostly 1 person.
RubyGems never more than 4, most often 2 people working on it.

These are volunteers with full-time jobs.

Used to be a few volunteers was enough.

$25,000 a month to run the RubyGems.org infrastructure.

rubygems.org was hacked - 4 days downloading gems and check-summing them

What the business that pay devs to work on full-time. There are some exceptions, but
it's not as much as you think, and companies change their mind. 

One objective of RubyTogether is to spread this out across more companies and contributions.
 
RubyTogether is a Trade Association, non-profit. 
 
RubyTogether (18 months ending Oct 2016)
- has paid 1,100 hours of developer time
- - 5 significant versions, Stripe funded the Molinillo resolution engine
- - 1.12 - compact index!!
- - 1.13 - required ruby version, and don't install | doctor
- 2 RGSoC and GSoC summers -- 11 students
- in last 9 months, took over maintenance of RubyGems code. Eric Hodel was let go.
- RubyGems.org and Bundler API (extreme makeover). Gem files and metadata hosted separately.
- - merging these is underway
- - rubygems.org is CDN agnostic - switched to Fastly
- - RubyGems.org would have been down in noticeable ways if we weren't paying folks to help keep it up.
- Gemstash is a thing.
- Bundler 2.0 is on its way (side-by-side compat with 1.0)
- Merging RubyGems and Bundler is also still on its way.

Membership between 12 months in and 18 months in is flat.

No significant companies have joined in the last 6 months.


---


