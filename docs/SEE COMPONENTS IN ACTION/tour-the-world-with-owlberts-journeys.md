---
title: Tour the World with Owlbert's Journeys!
deprecated: false
hidden: false
metadata:
  robots: index
---
<Icon name="fa-binoculars" /> Hey there explorer! :owlbert:

Welcome to the developer hub for Owlbert's Journeys. Additionally, to being a fun owl, <Glossary>Owlbert</Glossary> is also a great navigator, travel guide, and all-around companion!

You can keep reading to learn more about Owlbert and the kinds of journeys he offers or jump to one of these sections depending on how you want to integrate with the Owlbert's Journeys API.

<Cards columns={4}>
  <Card title="Owlbert's Interactive Tours" href="https://owlberts-journeys-demo.readme.io/docs/interactive-tours" icon="fa-person-walking" target="_blank">
    See what tours Owlbert offers and by type (walking, biking, or driving) for your iOS or Android app!
  </Card>

  <Card title="Owlbert's Audio Guides" href="https://owlberts-journeys-demo.readme.io/docs/audio-guides" icon="fa-headphones">
    Prefer to listen to Owlbert as you stroll? See all available audio guides, and which are available for offline downloading!
  </Card>

  <Card title="Owlbert's Tips & Recommendations" href="https://owlberts-journeys-demo.readme.io/docs/tips-and-recs" icon="fa-pizza-slice">
    Let Owlbert share tips about the history and architecture of a place, plus suggestions for nearby cafes and restaurants!
  </Card>

  <Card title="Owlbert's Journeys in Spanish" href="https://owlberts-journeys-demo.readme.io/docs/spanish-availability" icon="fa-map">
    We offer a selection of guided tours in Spanish, plus downloaded subtitles for any interactive tours that are currently English-only!
  </Card>
</Cards>

Anything that's available as an offline audio guide will be <Highlight>highlighted in blue</Highlight> across Owlbert's Journeys API documentation, while anything that can be downloaded as transcript for reading is <Highlight color="lightgreen">highlighted in light green.</Highlight>

# Take Owlbert in Your Pocket

Well, not really...but sort of! Connect your app to Owlbert Journey via our API to get Owlbert's personalized tips, hidden facts, and audio and video recordings to help personalize your trip in many major cities throughout the U.S. and cities abroad too.

<Image align="center" className="border" border={true} width="30% " src="https://files.readme.io/f731c62-Sports.psd.png" />

## Owlbert Walking Guides 🚶‍♀️

We believe the best way to see a city is by walking 👣, and why not do that with Owlbert as your guide? Our API connects with most map apps so Owlbert can easily share fun facts and recommendations while your listeners can ensure that they don't get lost!

<Callout icon="🚴‍♀️" theme="default">
  ### Looking to cycle with Owlbert?

  These walking guides can easily work if you're biking too! Just make sure you're not looking at your phone while you're listening!
</Callout>

## Owlbert Audio Guides 🎧

Owlbert's a real hoot (get it?!). But really, Owlbert's audio guides make it even easier—and lots more fun—to navigate a new city. Owlbert's audio guides are like if an audio book and a music playlist had a baby. They're fact-filled and song-filled, and perfect for listening to on the go! Sync Owlbert's audio guides with all of the major podcasting and music apps via our API.

#### Languages Supported

<Tabs>
  <Tab title="English Version">
    Our native tongue and Owlbert's. Transcripts of everything are also available in English!
  </Tab>

  <Tab title="Spanish Version">
    Habla español? Tenemos todas las guias en español!
  </Tab>

  <Tab title="French Version">
    Coming soon! 🇫🇷
  </Tab>
</Tabs>

Owlbert Journey Maps are a great way to spruce up any trip and make it more fun! They're family-friendly and a great way to uncover hidden facts about a new place. And don't worry, if you get stuck integrating with Owlbert Journey Maps' API, [shoot us an email](mailto:support@readme.io) and we'll be sure to get back to within one week!

:blue_heart:

export const Gradient = ({ children, start, stop, color = 'white' }) => (    
  <div style={{ background: `linear-gradient(${start}, ${stop})`, color: color, padding: '10px' }}>
    {children}
  </div>
);

export const Color = ({ children, color }) => (    
  <span style={{ color }}>{children}</span>
);

export const Highlight = ({ children, color = 'lightblue' }) => (    
  <span style={{ backgroundColor: color }}>{children}</span>
);

export const Column = ({ children }) => <div style={{ flex: 1, padding: '0 10px' }}>{children}</div>;

export const Columns = ({ children }) => <div style={{ display: 'flex' }}>{children}</div>;

export const Icon = ({ style = 'fa-regular', name }) => <i className={`${style} ${name}`} />;

