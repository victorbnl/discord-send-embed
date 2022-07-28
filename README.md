# Discord send embed

Helper for sending embeds with discord.py or its forks

## Installation

```
pip install git+https://github.com/victorbnl/discord-send-embed
```

## Usage

This module provides the method `discord.abc.Messageable.send_embed` which takes as argument a dictionnary to be converted as embed, and all the arguments of [`discord.abc.Messageable.send`](https://discordpy.readthedocs.io/en/stable/api.html#discord.abc.Messageable.send)

## Example

<table>
<thead>
<tr>
<td>discord.py</td>
<td>helper</td>
</tr>
</thead>
<tbody>
<tr>
<td>

```python
embed = discord.Embed(
    title="Title",
    description="This is a description",
    colour=0x206de8
)

embed.add_field(
    name="First field",
    value="Value of the first field"
)

embed.add_field(
    name="Second field",
    value="Value of the second field"
)

embed.set_footer(text="This is the footer text")

await ctx.send("Message content", embed=embed)
```

</td>
<td>

```python
await ctx.send_embed({
    "title": "Title",
    "description": "This is a description",
    "color": 0x206de8,
    "fields": [
        {
            "name": "First field",
            "value": "Value of the first field"
        },
        {
            "name": "Second field",
            "value": "Value of the second field"
        }
    ],
    "footer": {"text": "This is the footer text"}
})
```

</td>
</tr>
</tbody>
</table>
