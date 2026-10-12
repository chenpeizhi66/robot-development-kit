# NIO Robot Development Kit

Camera and perception software for NIO’s Robot Development Kit (RDK). I built it on the chip middleware team in Shenzhen, from March 2024. The stack runs as ROS 2 nodes on Ubuntu 24.04 and on NIO’s in-house chip.

This repository is a public summary. It does not contain NIO source code, internal diagrams, customer data, or unreleased product details.

## Service

The design is client/server. It is meant to stay up under multiple processes and high concurrency. The same service also ships on the NIO driving stack, which is on more than 500,000 vehicles.

## Pipeline

A state machine and a modular image pipeline carry images across processes and from chip to chip (IPC and C2C). The control plane is gRPC and Protobuf, so more than one client can connect.

## Models on the same chip

- A vision-language-action (VLA) model, deployed as ROS 2 nodes on the same SoC.
- ROS-LLM, brought up for language-conditioned robot control on the RDK.

## Media

Add public photos and short videos to [`media/`](media/) when they are cleared to share. Nothing is in that folder yet.
