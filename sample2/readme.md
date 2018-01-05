# YMF825Board Sample Module

## About this Sample Module

This is a software module for using YMF825 as a MIDI tone generator. It supports the following MIDI Commands.
+ Note On / Note Off
+ Program Change
+ Control Change #1
+ Control Change #7
+ Control Change #64
+ Pitch Bend
+ System Exclusive(YMF825 Tone Data)

## How to run on Arduino

+ Create a folder and copy all files in /common and files in /arduino to the folder.
+ Open the .ino file from Arduino IDE.
+ Each file will appear on the tab area, after loading. Verify and Upload as is, Arduino will work.
+ ymf825board_sample2.ino is a sketch that automatically plays ascending semitones for an octave.

## How to run on Raspberry Pi

+ Requires the bcm2835 library.
+ (If note installed)Install the bcm2835 library.
+ Please configure setting of makefile so that all files in /common and files in /raspi are compiled.


## Module Interface
| Function Name | details | When it's called | include file |
|---|---|---|---|
|initSPI()|initialize SPI|in an application initialization section|fmsd1.h|
|initSD1()|initialize YMF825(SD1)|in an application initialization section(after initSPI())|fmsd1.h|
|Fmdriver_init()|initialize the module|after initSD1()|fmif.h|
|Fmdriver_sendMidi()|send MIDI messages to the module|when it recieves a MIDI message|fmif.h|

+ In the case of Arduino, please wrap '#include fmif.h' in 'extern "C"{}'.


## ���̃T���v���ɂ���

�{�T���v���v���O�����́AYMF825��MIDI���������邽�߂̃\�t�g�E�F�A���W���[���ł��B�ȉ���MIDI Command�ɑΉ����Ă��܂��B
+ Note On / Note Off
+ Program Change
+ Control Change #1
+ Control Change #7
+ Control Change #64
+ Pitch Bend
+ System Exclusive(YMF825���F�f�[�^)

## Arduino�ł̎g����

+ �J���p�̃t�H���_�����A������ /common ���̃t�@�C���ƁA /arduino ���̃t�@�C����S�Ă��̃t�H���_�ɃR�s�[���܂��B
+ ���̏�ԂŁAArduino IDE ���� .ino �t�@�C�����J���܂��B
+ ����ɓǂݍ��߂���A�e�t�@�C�����^�u��Ɍ���܂��B���̂܂܌��؂Ə������݂��s���΁AArduino�����삵�܂��B
+ ymf825board_sample2.ino �͔����P�ʂ�1octave�������ɔ�������v���O�����ł��B


## Raspberry Pi�ł̎g����

+ bcm2835���C�u�����̎g�p���O��ƂȂ��Ă��܂��̂ŁAbcm2835���C�u�������C���X�g�[�����Ă��������B
+ /common ���̃t�@�C���ƁA/raspi ���̃t�@�C�����S���R���p�C�������悤�ɁAmakefile�̐ݒ���s���Ă��������B


## Module Interface
| �֐��� | �������e | �R�[������^�C�~���O | include file |
|---|---|---|---|
|initSPI()|SPI�̏�����|�A�v���̏���������|fmsd1.h|
|initSD1()|YMF825(SD1)�̏�����|�A�v���̏���������(initSPI()�̌�)|fmsd1.h|
|Fmdriver_init()|���̃��W���[���̏�����|initSD1()�̌�|fmif.h|
|Fmdriver_sendMidi()|���̃��W���[����MIDI�𑗂�|MIDI���b�Z�[�W��M��|fmif.h|

+ Arduino�Ŏg�p����ꍇ '#include fmif.h' �� 'extern "C"{}'�ň͂�ł��������B


