# Robot Development Kit

A camera and perception stack for a robot development kit. The services run as ROS 2 nodes on Ubuntu 24.04 and on the target chip.

This repository is a public summary. The implementation is not published here. Pictures and short videos can go in [`media/`](media/).

## Service

The design is client/server. It is meant to stay up under multiple processes and high concurrency.

## Pipeline

A state machine and a modular image pipeline carry images across processes and from chip to chip (IPC and C2C). The control plane is gRPC and Protobuf, so more than one client can connect.

## Models on the same chip

- A vision-language-action model, deployed as ROS 2 nodes on the same SoC.
- ROS-LLM, brought up for language-conditioned robot control on the kit.

## Media

Add photos and short videos to `media/` and link them from this README. Nothing is in that folder yet.
