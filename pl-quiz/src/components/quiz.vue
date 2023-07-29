<template>
  <div v-if="starting === true">
    <button @click="start">Start</button>
  </div>
  <div id="q1" v-if="question1 === true">
    <h3 class="question">
      You’re in a restaurant and you’re starving. The waitress finally brings you your order, but it
      has the wrong toppings on it. Other than that, it’s fine though. You…
    </h3>
    <button
      class="answer"
      @click="
        next();
        heroic()
      "
    >
      A. Tell the waiter the toppings are wrong.
    </button>
    <button
      class="answer"
      @click="
        next();
        sassy()
      "
    >
      B. Refuse to eat the order.
    </button>
    <button
      class="answer"
      @click="
        next();
        relaxed()
      "
    >
      C. Eat it anyways, I'm hungry.
    </button>
    <button
      class="answer"
      @click="
        next();
        quirky()
      "
    >
      D. Swap your food with a friend.
    </button>
  </div>
  <div id="q2" v-if="question2 === true">
    <h3 class="question">
      You’re taking a test and the teacher leaves the room. Someone slides one of the answers in
      your direction. You…
    </h3>
    <button
      class="answer"
      @click="
        next1();
        bashful()
      "
    >
      A. Quietly write down the answer and slide it back.
    </button>
    <button
      class="answer"
      @click="
        next1();
        mischevious()
      "
    >
      B. Too bad! I’m already cheating on this thing!
    </button>
    <button
      class="answer"
      @click="
        next1();
        heroic()
      "
    >
      C. Tell the teacher.
    </button>
    <button
      class="answer"
      @click="
        next1();
        relaxed()
      "
    >
      D. Bold of you to assume I even wrote my name!
    </button>
  </div>
  <div id="q3" v-if="question3 === true">
    <h3 class="question">
      You’re on a picnic, but you forgot to bring food! Luckily, a friend brings a huge assortment
      of snacks. What are you eating?
    </h3>
    <button
      class="answer"
      @click="
        next2();
        childish()
      "
    >
      A. My favorite! Duh!
    </button>
    <button
      class="answer"
      @click="
        next2();
        bashful()
      "
    >
      B. Whatever’s left after everyone else is done.
    </button>
    <button
      class="answer"
      @click="
        next2();
        feeble()
      "
    >
      C. Eh, I’m not hungry.
    </button>
    <button
      class="answer"
      @click="
        next2();
        awkward()
      "
    >
      D. I’d feel bad if I ate anything.
    </button>
  </div>
  <div id="q4" v-if="question4 === true">
    <h3 class="question">
      Your friend owes you money. It’s been a while, and they still haven’t paid you back. You…
    </h3>
    <button
      class="answer"
      @click="
        next3();
        heroic()
      "
    >
      A. Remind them that they owe you money.
    </button>
    <button
      class="answer"
      @click="
        next3();
        feeble();
        awkward()
      "
    >
      B. Say nothing.
    </button>
    <button
      class="answer"
      @click="
        next3();
        sassy()
      "
    >
      C. Bring it up when you want them to pay for you.
    </button>
    <button
      class="answer"
      @click="
        next3();
        mischevious()
      "
    >
      D. Steal.
    </button>
  </div>
  <div id="q5" v-if="question5 === true">
    <h3 class="question">Someone is talking bad about you behind your back. You…</h3>
    <button
      class="answer"
      @click="
        next4();
        relaxed()
      "
    >
      A. Ignore it. Who cares?
    </button>
    <button
      class="answer"
      @click="
        next4();
        heroic()
      "
    >
      B. Fight the bully.
    </button>
    <button
      class="answer"
      @click="
        next4();
        sassy()
      "
    >
      C. Confront the bully.
    </button>
    <button
      class="answer"
      @click="
        next4();
        awkward()
      "
    >
      D. Don’t say anything. Maybe you did something to upset them.
    </button>
  </div>
  <div id="q6" v-if="question6 === true">
    <h3 class="question">
      It’s late at night and you’re about to go to bed when a friend messages you asking for the
      homework. What do you say?
    </h3>
    <button
      class="answer"
      @click="
        next5();
        childish()
      "
    >
      A. Yeah, I can send it to you!
    </button>
    <button
      class="answer"
      @click="
        next5();
        awkward()
      "
    >
      B. Leave them on read.
    </button>
    <button
      class="answer"
      @click="
        next5();
        quirky()
      "
    >
      C. Who are you?
    </button>
    <button
      class="answer"
      @click="
        next5();
        relaxed()
      "
    >
      D. Uh… we had homework?
    </button>
  </div>
  <div id="q7" v-if="question7 === true">
    <h3 class="question">It’s your birthday, but nobody remembered… What do you do?</h3>
    <button
      class="answer"
      @click="
        next6();
        awkward()
      "
    >
      A. Eh, it’s okay. I like spending time by myself.
    </button>
    <button
      class="answer"
      @click="
        next6();
        bashful()
      "
    >
      B. Maybe they’re just busy. I’ll ask to hang out later.
    </button>
    <button
      class="answer"
      @click="
        next6();
        childish()
      "
    >
      C. Call them now.
    </button>
    <button
      class="answer"
      @click="
        next6();
        feeble()
      "
    >
      D. Cry.
    </button>
  </div>
  <div id="q8" v-if="question8 === true">
    <h3 class="question">
      You’re trying to beat a difficult level in a video game, but you just can’t get past the last
      obstacle. You…
    </h3>
    <button
      class="answer"
      @click="
        next7();
        relaxed()
      "
    >
      A. Give up.
    </button>
    <button
      class="answer"
      @click="
        next7();
        feeble()
      "
    >
      B. Maybe just… one more try…
    </button>
    <button
      class="answer"
      @click="
        next7();
        quirky()
      "
    >
      C. Ask a friend for help.
    </button>
    <button
      class="answer"
      @click="
        next7();
        childish()
      "
    >
      D. Rage quit.
    </button>
  </div>
  <div id="q9" v-if="question9 === true">
    <h3 class="question">
      You get into a fight with your parents and storm away. It’s been a few hours, but they haven’t
      said anything to you. What do you do?
    </h3>
    <button
      class="answer"
      @click="
        next8();
        awkward()
      "
    >
      A. Go and apologize. Maybe they were right…
    </button>
    <button
      class="answer"
      @click="
        next8();
        sassy()
      "
    >
      B. Good! I didn’t want to see them anyway.
    </button>
    <button
      class="answer"
      @click="
        next8();
        relaxed()
      "
    >
      C. Talk to a friend about it.
    </button>
    <button
      class="answer"
      @click="
        next8();
        feeble()
      "
    >
      D. Wait for them to say something first.
    </button>
  </div>
  <div id="q10" v-if="question10 === true">
    <h3 class="question">
      You’re on the subway when you see a homeless person get on the train. They’re walking around,
      asking for money. You…
    </h3>
    <button
      class="answer"
      @click="
        next9();
        heroic()
      "
    >
      A. Give them money.
    </button>
    <button
      class="answer"
      @click="
        next9();
        quirky()
      "
    >
      B. Comfort them.
    </button>
    <button
      class="answer"
      @click="
        next9();
        awkward()
      "
    >
      C. Ignore them.
    </button>
    <button
      class="answer"
      @click="
        next9();
        bashful()
      "
    >
      D. Get off the train.
    </button>
  </div>
  <div id="q11" v-if="question11 === true">
    <h3 class="question">
      You’re criticizing a game you don’t like when your friend gets upset at you. It’s their
      favorite game! You…
    </h3>
    <button
      class="answer"
      @click="
        next10();
        bashful()
      "
    >
      A. Apologize.
    </button>
    <button
      class="answer"
      @click="
        next10();
        quirky()
      "
    >
      B. Agree to disagree.
    </button>
    <button
      class="answer"
      @click="
        next10();
        sassy()
      "
    >
      C. Really? THAT’s your favorite?
    </button>
    <button
      class="answer"
      @click="
        next10();
        awkward()
      "
    >
      D. Well… now that I think about it…
    </button>
  </div>
  <div id="q12" v-if="question12 === true">
    <h3 class="question">It’s April Fools Day! You…</h3>
    <button
      class="answer"
      @click="
        next11();
        mischevious()
      "
    >
      A. PRANK SOMEONE!!!
    </button>
    <button
      class="answer"
      @click="
        next11();
        bashful()
      "
    >
      B. Stay home.
    </button>
    <button
      class="answer"
      @click="
        next11();
        feeble()
      "
    >
      C. Resign yourself to your fate.
    </button>
    <button
      class="answer"
      @click="
        next11();
        quirky()
      "
    >
      D. I’ll finally get back at my friend!
    </button>
  </div>
  <div id="q13" v-if="question13 === true">
    <h3 class="question">
      You’ve been given an assignment from your teacher. Create a presentation about anything you
      want! You…
    </h3>
    <button
      class="answer"
      @click="
        next12();
        bashful()
      "
    >
      A. Pick something easy.
    </button>
    <button
      class="answer"
      @click="
        next12();
        childish()
      "
    >
      B. Make it about my favorite cartoon show!
    </button>
    <button
      class="answer"
      @click="
        next12();
        quirky()
      "
    >
      C. Talk about something nobody else has heard of before.
    </button>
    <button
      class="answer"
      @click="
        next12();
        sassy()
      "
    >
      D. Talk bad about something you don’t like.
    </button>
  </div>
  <div id="q14" v-if="question14 === true">
    <h3 class="question">You’re at a party, and everyone is taking a slice of the cake. You…</h3>
    <button
      class="answer"
      @click="
        next13();
        heroic()
      "
    >
      A. Remind them that they owe you money.
    </button>
    <button
      class="answer"
      @click="
        next13();
        mischevious()
      "
    >
      B. Maybe take a little more…
    </button>
    <button
      class="answer"
      @click="
        next13();
        childish()
      "
    >
      C. Get one of the cool decorations.
    </button>
    <button
      class="answer"
      @click="
        next13();
        feeble()
      "
    >
      D. Can’t get any… you’re at the back of the line…
    </button>
  </div>
  <div id="q15" v-if="question15 === true">
    <h3 class="question">
      You’re at a friend’s house when you notice that they have something that’s yours. You…
    </h3>
    <button
      class="answer"
      @click="
        next14();
        mischevious()
      "
    >
      A. Steal it back.
    </button>
    <button
      class="answer"
      @click="
        next14();
        heroic()
      "
    >
      B. Confront them.
    </button>
    <button
      class="answer"
      @click="
        next14();
        bashful()
      "
    >
      C. Ignore it. Maybe they needed it.
    </button>
    <button
      class="answer"
      @click="
        next14();
        sassy()
      "
    >
      D. Oh HELL no!
    </button>
  </div>
  <div id="q16" v-if="question16 === true">
    <h3 class="question">Your friends are planning a prank on someone. You…</h3>
    <button
      class="answer"
      @click="
        next15();
        mischevious()
      "
    >
      A. Help them out! It’ll be fun!
    </button>
    <button
      class="answer"
      @click="
        next15();
        sassy()
      "
    >
      B. Well… they never did pay me back from last time…
    </button>
    <button
      class="answer"
      @click="
        next15();
        quirky()
      "
    >
      C. Join, but add a surprise twist at the end!
    </button>
    <button
      class="answer"
      @click="
        next15();
        heroic()
      "
    >
      D. Say no.
    </button>
  </div>
  <div id="q17" v-if="question17 === true">
    <h3 class="question">You find a ditch on the side of a forest trail. You…</h3>
    <button
      class="answer"
      @click="
        next16();
        childish()
      "
    >
      A. Play with the mud!
    </button>
    <button
      class="answer"
      @click="
        next16();
        feeble()
      "
    >
      B. Accidentally fall in it.
    </button>
    <button
      class="answer"
      @click="
        next16();
        mischevious()
      "
    >
      C. Build a pitfall trap.
    </button>
    <button
      class="answer"
      @click="
        next16();
        relaxed()
      "
    >
      D. Meh. Not my problem.
    </button>
  </div>
  <div id="q18" v-if="question18 === true">
    <h3 class="question">You have a crush on someone. You…</h3>
    <button
      class="answer"
      @click="
        next17();
        mischevious()
      "
    >
      A. Do something to get their attention.
    </button>
    <button
      class="answer"
      @click="
        next17();
        childish()
      "
    >
      B. Daydream about them.
    </button>
    <button
      class="answer"
      @click="
        next17();
        feeble()
      "
    >
      C. Give up. What’s the point?
    </button>
    <button
      class="answer"
      @click="
        next17();
        sassy()
      "
    >
      D. Scold yourself for liking someone so weird.
    </button>
  </div>
  <div v-if="ending === true">
    <p>end</p>
    <button @click="retry">Retry?</button>
  </div>
</template>

<script>
export default {
  name: 'quiz',
  data() {
    return {
      starting: true,
      question1: false,
      question2: false,
      question3: false,
      question4: false,
      question5: false,
      question6: false,
      question7: false,
      question8: false,
      question9: false,
      question10: false,
      question11: false,
      question12: false,
      question13: false,
      question14: false,
      question15: false,
      question16: false,
      question17: false,
      question18: false,
      personality: [{
            Awkward: 0,
            Bashful: 0,
            Childish: 0,
            Feeble: 0,
            Heroic: 0,
            Mischevious: 0,
            Relaxed: 0,
            Sassy: 0,
            Quirky: 0,
      }],

      ending: false,
    }
  },
  methods: {
    start: function () {
      this.starting = false
      this.question1 = true
    },
    next: function () {
      this.question1 = false
      this.question2 = true
    },
    next1: function () {
      this.question2 = false
      this.question3 = true
    },
    next2: function () {
      this.question3 = false
      this.question4 = true
    },
    next3: function () {
      this.question4 = false
      this.question5 = true
    },
    next4: function () {
      this.question5 = false
      this.question6 = true
    },
    next5: function () {
      this.question6 = false
      this.question7 = true
    },
    next6: function () {
      this.question7 = false
      this.question8 = true
    },
    next7: function () {
      this.question8 = false
      this.question9 = true
    },
    next8: function () {
      this.question9 = false
      this.question10 = true
    },
    next9: function () {
      this.question10 = false
      this.question11 = true
    },
    next10: function () {
      this.question11 = false
      this.question12 = true
    },
    next11: function () {
      this.question12 = false
      this.question13 = true
    },
    next12: function () {
      this.question13 = false
      this.question14 = true
    },
    next13: function () {
      this.question14 = false
      this.question15 = true
    },
    next14: function () {
      this.question15 = false
      this.question16 = true
    },
    next15: function () {
      this.question16 = false
      this.question17 = true
    },
    next16: function () {
      this.question17 = false
      this.question18 = true
    },
    next17: function () {
      this.question18 = false
      this.ending = true
      console.log(
        Math.max(
            this.personality.Awkward,
            this.personality.Bashful,
            this.personality.Childish,
            this.personality.Feeble,
            this.personality.Heroic,
            this.personality.Mischevious,
            this.personality.Relaxed,
            this.personality.Sassy,
            this.personality.Quirky)
            )
        const result =
        Math.max(
            this.personality.Awkward,
            this.personality.Bashful,
            this.personality.Childish,
            this.personality.Feeble,
            this.personality.Heroic,
            this.personality.Mischevious,
            this.personality.Relaxed,
            this.personality.Sassy,
            this.personality.Quirky)
        
    },
    retry: function () {
      this.ending = false
      this.starting = true
    },
    awkward: function () {
      this.personality.Awkward = this.personality.Awkward + 1
    },
    bashful: function () {
      this.personality.Bashful = this.personality.Bashful + 1
    },
    childish: function () {
      this.personality.Childish = this.personality.Childish + 1
    },
    feeble: function () {
      this.personality.Feeble = this.personality.Feeble + 1
    },
    heroic: function () {
      this.personality.Heroic = this.personality.Heroic + 1
    },
    mischevious: function () {
      this.personality.Mischevious = this.personality.Mischevious + 1
    },
    relaxed: function () {
      this.personality.Relaxed = this.personality.Relaxed + 1
    },
    sassy: function () {
      this.personality.Sassy = this.personality.Sassy + 1
    },
    quirky: function () {
      this.personality.Quirky = this.personality.Quirky + 1
    }
  }
}
</script>

<style scoped></style>
