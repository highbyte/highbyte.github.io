---
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
published: true
author_profile: true
---

`READY.`

Software developer by day, retro computing tinkerer by night. Based in Stockholm.

#### Now

Consultant at [Ecrucial][ecrucial] in Stockholm — Development and DevOps in the .NET space.

```yaml
role:     Consultant @ Ecrucial, Stockholm
focus:    [.NET, DevOps]
projects: github.com/highbyte
also:     [home-automation, gaming]
```

#### Earlier

Coding professionally since 1990, across a lot of different technologies and domains.

```
$ git log --format="%ad  %s" --date=format:'%Y'
2010s  .NET Core, Cloud, CI/CD pipelines
2000s  .NET Framework, on-prem enterprise systems
1990s  VB6, VBA, tools and product development
1990   First summer job, C & Basic
```

#### Even Earlier

First programs in the 80s on a [ZX81][zx81] in BASIC, then deeper into C128 and Amiga in Assembler. Got involved in the [Demoscene][demoscene] and picked up the alias [Highbyte][highbyte_demoscene] around then. That nostalgia eventually turned into a project — a [6502 CPU / C64 emulator][emulator] you can run in your browser:

```basic
10 REM * HIGHBYTE C64 MINI DEMO *
20 PRINT CHR$(147)
30 FOR I=0 TO 15
40 POKE 53280,I:POKE 53281,15-I
50 PRINT "HELLO FROM 1987! "
60 FOR T=1 TO 200:NEXT T
70 NEXT I
```

[Start This BASIC Program In The Emulator](#){: #run-basic-btn .btn .btn--success target="_blank" rel="noopener noreferrer" }

<script>
	(function () {
		const runBasicBtn = document.getElementById("run-basic-btn");
		if (!runBasicBtn) return;

		function toBase64Utf8(text) {
			const bytes = new TextEncoder().encode(text);
			let binary = "";
			for (const b of bytes) binary += String.fromCharCode(b);
			return btoa(binary);
		}

		runBasicBtn.addEventListener("click", function (event) {
			event.preventDefault();

			const basicCode = document.querySelector("code.language-basic");
			if (!basicCode) return;

			const basicText = (basicCode.textContent || "").trimEnd().toLowerCase();
			const encodedBasic = encodeURIComponent(toBase64Utf8(basicText));
			const emulatorUrl =
				"https://highbyte.se/dotnet-6502/app2/?system=C64&start=1&waitForSystemReady=1&basicText=" +
				encodedBasic +
				"&runBasic=1";

			window.open(emulatorUrl, "_blank", "noopener,noreferrer");
		});
	})();
</script>

[To emulator →][emulator]{: target="_blank" rel="noopener noreferrer" }

[github_user]: https://github.com/highbyte
[demoscene]: https://en.wikipedia.org/wiki/Demoscene
[zx81]: https://en.wikipedia.org/wiki/ZX81
[highbyte_demoscene]: http://janeway.exotica.org.uk/author.php?id=18992
[ecrucial]: https://ecrucial.se
[home_automation]: https://www.home-assistant.io
[emulator]: https://highbyte.se/dotnet-6502/app2/
