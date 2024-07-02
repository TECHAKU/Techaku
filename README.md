```Rust
trait Introduce {
    fn intro(&self);
}

struct Me {
    name: String,
    job: String,
    code: String,
    skills: String,
}

impl Introduce for Me {
    fn intro(&self) {
        println!(
            "Ciallo! I am {},{} an otaku who primarily crafts code with {}. My skills? {}",
            self.name, self.job, self.code, self.skills
        );
    }
}

fn main() {
    let me = Me {
        name: String::from("Techaku"),
        job: String::new(),
        code: String::from("Rust"),
        skills: String::from("surfing 🏄"),
    };

    me.intro();
}
```
> This portion of content derives inspiration from [moonD4rk](https://github.com/moonD4rk/moonD4rk).
