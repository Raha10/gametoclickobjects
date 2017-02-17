var emitter;
var GameState={
preload:function(){
this.load.image('background','assets/images/background.png');


this.load.image('guava','assets/images/guava.png');
this.load.image('grapes','assets/images/grapes.png');
this.load.image('watermelon','assets/images/watermelon.png');
this.load.image('orange','assets/images/orange.png');


},
create:function(){
	this.background=this.game.add.sprite(500,300,'background');


	// this.guava = this.game.add.sprite(100,100,'guava');
	// this.guava.inputEnabled=true;
	// this.guava.input.useHandCursor=true;
	// this.guava.events.onInputDown.add(function destroy(){this.guava.destroy();},this);
	

	emitter = game.add.emitter(game.world.centerX, 0, 100);

    emitter.makeParticles('grapes');


    emitter.minParticleSpeed.setTo(-300, 30);
    emitter.maxParticleSpeed.setTo(300, 100);
    emitter.minParticleScale = 0.1;
    emitter.maxParticleScale = 0.5;
    emitter.gravity = 250;


    //  This will emit a quantity of 5 particles every 500ms. Each particle will live for 2000ms.
    //  The -1 means "run forever"
    emitter.flow(2000, 500, 5, -1);



    emitter = game.add.emitter(game.world.centerX, 0, 100);

    emitter.makeParticles('guava');


    emitter.minParticleSpeed.setTo(-300, 30);
    emitter.maxParticleSpeed.setTo(300, 100);
    emitter.minParticleScale = 0.1;
    emitter.maxParticleScale = 0.5;
    emitter.gravity = 250;
    


    //  This will emit a quantity of 5 particles every 500ms. Each particle will live for 2000ms.
    //  The -1 means "run forever"
    emitter.flow(2000, 500, 5, -1);




    //fruit1

    emitter = game.add.emitter(game.world.centerX, 0, 100);

    emitter.makeParticles('watermelon');


    emitter.minParticleSpeed.setTo(-300, 30);
    emitter.maxParticleSpeed.setTo(300, 100);
    emitter.minParticleScale = 0.1;
    emitter.maxParticleScale = 0.5;
    emitter.gravity = 250;


    //  This will emit a quantity of 5 particles every 500ms. Each particle will live for 2000ms.
    //  The -1 means "run forever"
    emitter.flow(2000, 500, 5, -1);




    //orange

    emitter = game.add.emitter(game.world.centerX, 0, 100);

    emitter.makeParticles('orange');


    emitter.minParticleSpeed.setTo(-300, 30);
    emitter.maxParticleSpeed.setTo(300, 100);
    emitter.minParticleScale = 0.1;
    emitter.maxParticleScale = 0.5;
    emitter.gravity = 250;


    //  This will emit a quantity of 5 particles every 500ms. Each particle will live for 2000ms.
    //  The -1 means "run forever"
    emitter.flow(2000, 500, 5, -1);







	this.heart.scale.setTo(0.5);
	this.fruit1.scale.setTo(0.05);

	



},

update:function(){



},
};
var game = new Phaser.Game(1000,1000, Phaser.AUTO);
game.state.add('GameState',GameState);
game.state.start('GameState');