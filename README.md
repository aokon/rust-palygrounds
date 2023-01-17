# Rust playground

## Usefull links

* [Rust packages](https://crates.i)

## Known issues

### Fetching crate packages

It looks like that I have some issue with ssh-agent and I have received authentication error during fetching deps via cargo. I have had to use following workflow:

```
eval `ssh-agent -s`
ssh-add
CARGO_NET_GIT_FETCH_WITH_CLI=true cargo add rand
```
