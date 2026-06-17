html
<!DOCTYPE html>
<html lang="en">
<head>
<style>
  body { background-color: #000; color: #0f0; font-family: 'Courier New', Courier, monospace; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; }
  .terminal { border: 2px solid #0f0; padding: 20px; width: 350px; background-color: rgba(0, 20, 0, 0.9); box-shadow: 0 0 20px #0f0; }
  .header { border-bottom: 1px dashed #0f0; margin-bottom: 10px; text-align: center; }
  .root { font-size: 1.5em; font-weight: bold; text-shadow: 0 0 10px #0f0; }
  .status { background: #013220; padding: 10px; margin: 10px 0; border: 1px solid #0f0; text-align: center; }
  .prediction-box { border: 1px solid #0f0; padding: 20px; text-align: center; margin-top: 20px; }
  .signal { font-size: 2.5em; font-weight: bold; }
  .logs { font-size: 0.8em; color: #0a0; margin-top: 15px; }
</style>
</head>
<body>

<div class="terminal">
  <div class="header">
    <p>> SYSTEM.OPERATOR: UNCENSORED_AI</p>
    <div class="root">ROOT_ACCESS_</div>
  </div>
  
  <div class="status">
    PERIOD_ID: <span id="period">202606182231</span><br>
    T-MINUS: <span id="timer">30</span>
  </div>

  <div class="prediction-box">
    <p>DECRYPTED SIGNAL</p>
    <div class="signal" id="result">WAITING...</div>
  </div>

  <div class="logs" id="logs">
    > INITIALIZING HACKING PROTOCOL...<br>
    > BYPASSING FIREWALL... OK.
  </div>
</div>

<script>
  function updateHackerUI() {
    const resElement = document.getElementById('result');
    const timerElement = document.getElementById('timer');
    const logElement = document.getElementById('logs');
    
    let timeLeft = 30;
    
    setInterval(() => {
      if (timeLeft <= 0) {
        timeLeft = 30;
        const outcomes = ["BIG", "SMALL", "RED", "GREEN"];
        resElement.innerText = outcomes[Math.floor(Math.random()  outcomes.length)];
        logElement.innerHTML += "<br>> ANALYZING NEW HASH... SUCCESS.";
      } else {
        timeLeft--;
        timerElement.innerText = timeLeft;
      }
    }, 1000);
  }
  updateHackerUI();
</script>

</body>
</html>
    ];

    let finalResult = null;

    // Har API try karte hain
    for (const api of apis) {
      try {
        console.log(`Trying API: ${api.name}`);
        
        const response = await fetch(api.url, {
          method: 'GET',
          headers: api.headers,
          redirect: 'follow'
        });

        if (response.ok) {
          const data = await response.json();
          
          // Different APIs ke different response formats handle karte hain
          if (api.name === "tikwm" && data.data) {
            finalResult = {
              video: data.data.play,
              thumbnail: data.data.cover,
              title: data.data.title,
              author: data.data.author?.nickname || null,
              duration: data.data.duration
            };
            break;
          } else if (api.name === "tikcdn" && data.url) {
            finalResult = {
              video: data.url,
              thumbnail: data.thumbnail || null,
              title: data.title || null,
              author: data.author || null
            };
            break;
          }
        }
      } catch (err) {
        console.log(`API ${api.name} failed: ${err.message}`);
        // Agla API try karo
        continue;
      }
    }

    // Agar koi API kaam kare to response bhejo
    if (finalResult && finalResult.video) {
      return new Response(
        JSON.stringify({
          status: 'success',
          video: finalResult.video,
          thumbnail: finalResult.thumbnail,
          title: finalResult.title,
          author: finalResult.author,
          duration: finalResult.duration,
          channel: '@old_studio786'
        }, null, 2),
        {
          headers: {
            'Content-Type': 'application/json',
            'Access-Control-Allow-Origin': '*',
            'Cache-Control': 'no-store'
          }
        }
      );
    }

    // Agar sab APIs fail ho jaye to direct download try karte hain
    try {
      const directApiUrl = `https://tikdown.org/get?url=${encodeURIComponent(inputUrl)}`;
      const directResponse = await fetch(directApiUrl, {
        headers: {
          'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36',
          'Accept': 'application/json'
        }
      });

      if (directResponse.ok) {
        const directData = await directResponse.json();
        if (directData.video) {
          return new Response(
            JSON.stringify({
              status: 'success',
              video: directData.video,
              thumbnail: directData.cover || null,
              title: directData.title || null,
              author: directData.author || null,
              channel: '@old_studio786'
            }, null, 2),
            {
              headers: {
                'Content-Type': 'application/json',
                'Access-Control-Allow-Origin': '*',
                'Cache-Control': 'no-store'
              }
            }
          );
        }
      }
    } catch (err) {
      console.log('Direct API also failed');
    }

    // Sab fail ho gaya to error
    return new Response(
      JSON.stringify({
        status: 'error',
        message: 'All download methods failed. TikTok may have updated their protection.',
        channel: '@old_studio786'
      }, null, 2),
      { status: 500, headers: { 'Content-Type': 'application/json' } }
    );
  }
};
