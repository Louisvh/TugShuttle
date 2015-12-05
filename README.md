TugShuttle
===============
## Purpose
TugShuttle is a command line tool that starts a DigitalOcean Droplet and tunnels your traffic to it over SSH making it a temporary VPN. As the name suggests, it uses Tugboat to interface with DigitalOcean and Sshuttle to tunnel your traffic to the Droplet.

![An example use case for a temporary VPN. Watching all of Blackadder would cost $0.09 in DigitalOcean credit. Art style "borrowed" from Randall Munroe (xkcd.com)](https://cloud.githubusercontent.com/assets/6605273/11608014/c05a5cda-9b5d-11e5-8873-fa5b1c9f971c.png)

VPNs have many valid use cases and can be quite convenient at times, but they tend to require a monthly subscription. That is hard to justify if you *almost* never use it. What's special about TugShuttle tunnels is that it's really easy to quickly spin one up *and down again* without needing a monthly subscription for anything (as is the nature of DigitalOcean Droplets). Droplets only cost $0.007 per hour (not a typo, that's less than one cent) so watching a region locked movie only sets you back approximately one additional cent. It's pretty manageable.

## Prerequisites / Dependencies
1) A DigitalOcean account with some credit. Renting a Droplet is very cheap, but it's not free. If you don't have one, you can make an account [here](https://www.digitalocean.com/?refcode=433d02d1a833) (note: this is a referral link, meaning you get $10 starting credit. If you don't feel comfortable using that, you can sign up on the non-referral page [here](https://cloud.digitalocean.com/registrations/new))

2) A valid SSH key linked to your DigitalOcean account. You can link one [here](https://cloud.digitalocean.com/settings/security). If you've never used SSH keys before, learn how to create them [here](help.github.com/articles/generating-ssh-keys/).

3) Sshuttle. It's in the repositories. You can also grab it from the [Github page](https://github.com/apenwarr/sshuttle).

4) Tugboat. Get it with "gem install tugboat" (requires Ruby)

## Installation
Clone the repository and put "tugshuttle" in any folder in your $PATH. 

## Usage
`tugshuttle $server`, where $server is one of: `ams1`, `ams2`, `ams3`, `fra1`, `lon1`, `nyc1`, `nyc2`, `nyc3`, `sfo1`, `sgp1`, `tor1`. This connects you to a server in Amsterdam, Frankfurt, New York City, San Francisco, Singapore or Toronto respectively.

## License
:[MIT LICENSE](LICENSE)
