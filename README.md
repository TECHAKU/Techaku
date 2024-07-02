```Rust
trait Introduce {
    fn intro(&self);
}

struct Me {
    name: &'static str,
    job: Option<&'static str>,
    code: &'static str,
    skills: &'static str,
}

impl Introduce for Me {
    fn intro(&self) {
        let job_str = match &self.job {
            Some(job) => format!("{}", job),
            None => "an otaku".to_string(),
        };
        println!(
            "Ciallo! I am {}, {} who primarily crafts code with {}. My skills? {}",
            self.name, job_str, self.code, self.skills
        );
    }
}

fn main() {
    let me = Me {
        name: "Techaku",
        job: None,
        code: "Rust",
        skills: "surfing 🏄",
    };

    me.intro();
}
```
> This portion of content derives inspiration from [moonD4rk](https://github.com/moonD4rk/moonD4rk).
