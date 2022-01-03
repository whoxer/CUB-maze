# CUB-maze
CUB maze é um jogo de labirinto e quebra-cabeça inspirado no jogo de video-game pra Atari 2600 chamado Adventure lançado em 1979, considerado o primeiro jogo de ação e aventura e também o primeiro a permitir com que o jogador soubesse o nome do seu criador por meio de um easter-egg.

Você é um quadrado branco dentro de um labirinto escuro e precisa de chaves para abrir as portas e fugir dele. Você as encontra espalhadas pelo mapa. Mas cuidado. Você não pode encostar nas paredes brancas, e a cada vez que você pega uma chave a sua velocidade aumenta um pouquinho a mais. Esse é CUB maze. Conseguirá você fugir dessa prisão?

## Desenvolvimento

O jogo foi desenvolvido com blocos de código usando a engine do Construct 2, após isso converti o arquivo do projeto em HTML5. Trechos do código ainda possuem comentários que mostram isso.

``` javascript function OnRegisterSWError(e)
		{
			console.warn("Failed to register service worker: ", e);
		};
		
		// Runtime calls this global method when ready to start caching (i.e. after startup).
		// This registers the service worker which caches resources for offline support.
		window.C2_RegisterSW = function C2_RegisterSW()
		{
			if (!navigator.serviceWorker)
				return;		// no SW support, ignore call
			
			try {
				navigator.serviceWorker.register("sw.js", { scope: "./" })
				.then(function (reg)
				{
					console.log("Registered service worker on " + reg.scope);
				})
				.catch(OnRegisterSWError);
			}
			catch (e)
			{
				OnRegisterSWError(e);
			}
		};
```
## Download via Gamejolt

https://gamejolt.com/games/CUB-maze/640507


