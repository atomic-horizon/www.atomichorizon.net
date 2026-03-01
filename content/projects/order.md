+++
title = 'Order'
+++

![Order banner](https://github.com/atomic-horizon/order/blob/gh-pages/img/embed_banner.png?raw=true)

**[View the Order documentation →](https://order.atomichorizon.net/)**

Order is a configurable module-loader framework for Roblox, featuring fast lookups, cyclic dependency support, and a fully customizable initialization pipeline. It powers the architecture behind Combat Arena and is freely available for any Roblox developer to use.

## Why Order?

Order removes the barriers between modules so you can focus on building great experiences.

### Cyclic Dependency Support

The standout feature of Order. Modules can freely reference each other — no more restructuring your code to avoid circular imports. Order handles the complexity behind the scenes through a metatable-based approach.

### Effortless Module Loading

Replace lengthy `require()` chains with a single call: `shared("ModuleName")`. Resolve modules by name, partial path, or direct instance reference — Order finds them for you.

```lua
-- Load a module by name (no path required)
local DataManager = shared("DataManager")

-- Or by partial path for disambiguation
local GetRemote = shared("lib/GetRemote")

-- Or by direct ModuleScript reference
local Util = shared(game.ReplicatedStorage.Shared.Util)
```

### Customizable Init Sequence

Define your own initialization pipeline. The default **Prep → Init** pattern gives you a synchronous setup phase followed by an async runtime phase — and you can override or extend it per-task or project-wide.

### Task Priority Control

Set a `Priority` value on any task to control its position in the load order. Higher values go first, negatives go last. Fine-grained startup control without tangled dependency chains.

### Multi-Place Universe Support

First-class support for Roblox game universes. Map Place IDs to named types, then define which Code Groups are active per type — share exactly the right code across your lobby, game servers, and more.

### Built-In Developer Tools

Toggle verbose module-loading logs and cyclic-dependency analysis straight from `Settings.luau`. Silent mode keeps production output clean while keeping Studio output rich.

## Links

- [Documentation](https://atomic-horizon.github.io/order/docs/intro)
- [API Reference](https://atomic-horizon.github.io/order/api)
- [GitHub](https://github.com/atomic-horizon/order)
- [Roblox Marketplace](https://www.roblox.com/library/11152308855/)
