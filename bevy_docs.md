# [BEVY](https://bevy.org/)

Bevy oyun motoru Rust dilinde yazılmış bir oyun motorudur. ECS tabanlıdır. Burada bazı bilgiler bulunmaktadır.


Basic Concepts
``` Rust
use bevy::prelude::*;

fn test_system(query: Query<&Name>) {
    for name in query.iter() {
        info!("Name: {}", name);
    }
}

#[derive(Component)]
struct Player;

fn spawn(mut commands: Commands) {
    commands.spawn((
        Player,
        Name::new("PLAYER TEST"),
        Transform::from_xyz(0.0, 0.0, 0.0),
    ));
}

fn main() {
    App::new()
        .add_plugins(DefaultPlugins)
        .add_systems(Update, test_system)
        .add_systems(Startup, spawn)
        .run();
}
```


Cargo.toml
``` toml
[package]
name = "project_name"
version = "0.1.0"
edition = "2024"

[dependencies]
bevy = { version = "0.18", features = ["dynamic_linking"] }
# Physics Engine
avian3d = "0.5"

[profile.dev]
opt-level = 1

[profile.dev.package."*"]
opt-level = 3
```
