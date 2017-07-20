# TIL (aka Today I Learned):
> A collection of random little tips that documented elsewhere, but TIL it

 # __*Git*__

> Add the remote, call it "upstream":

`|> git remote add upstream https://github.com/whoever/whatever.git`

> Fetch all the branches of that remote into remote-tracking branches,
> such as upstream/master:

`|> git fetch upstream`

> Make sure that you're on your master branch:

`|> git checkout master`

> Rewrite your master branch so that any commits of yours that
> aren't already in upstream/master are replayed on top of that
> other branch:

`|> git rebase upstream/master`

 # __*PostgreSQL*__

> Display all available roles

`|> psql postgres`
`|> postgres=# \du`

> Grant a role attributes

`|> ALTER ROLE <role name> <attribute name>;`

# __*Ruby*__

## Strings

> Translate method replaces

```
#irb |> string = 'ABCD'
#irb |> string.tr!('ABC', '123')
#irb => "123"
```

## Iterators

> Inject method shorthand

```
#irb |> [1,2,3,4,5,6,7].inject(0) { |sum, elem| sum + elem }
#irb => 28
#irb |> [1,2,3,4,5,6,7].inject(:+)
#irb => 28
```
