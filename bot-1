const puppeteer = require('puppeteer');
const site="https://soundcloud.com/lizard-boy666/sets";
console.log("----start----");

(async () => {
  const browser = await puppeteer.launch({
    headless: false,
    args:['--start-fullscreen']
  });
  const page = await browser.newPage();
  await page.setViewport({width:600, height:600});
  await page.goto(site, {
    waitUntil: 'networkidle2',
  });
     console.log("artiste trouvé")
  //Cookie
  await page.click('#onetrust-accept-btn-handler');
     console.log('cookie accepté');

  function delay(n){
      return new Promise(function(resolve){
          setTimeout(resolve,n*1000);
      });
  }

  await delay(10);
  await page.click('.soundTitle__playButton > a')
  console.log('1er music lancé');
  let a = 1;
  while (a=1) {
    await delay(30);
    await page.mouse.click(100,580);
  }
})();
