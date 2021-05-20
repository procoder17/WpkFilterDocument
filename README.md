# WpkFilterDocument

Windows Packet Filter
Windows Packet Filter (WinpkFilter) is a high performance packet filtering framework for Windows that allows developers to transparently filter (view and modify) raw network packets at the NDIS level of the network stack with minimal impact on network activity and without having to write any low level driver code.

Windows Packet Filter includes NDIS 3.1/4 hooking VxD driver (Windows 95/ME), NDIS 4 hooking filter driver (Windows NT/2000/XP), NDIS 5 Intermediate (Windows XP/2003) and NDIS 6 Lightweight Filter (LWF) drivers as well as companion user-mode API DLL and samples.

Key advantage of Windows Packet Filter in comparison to other packet filtering frameworks for Windows (based on Windows Filtering Platform (WFP) callout drivers, Layered Service Poviders (LSP), TDI filters and etc..) is the ability to manipulate raw Ethernet frames achieved by installing driver below all network protocol drivers and just above network interface driver. Thus WinpkFilter driver has an ultimate control over all network traffic flow destined to or originated from your system and allows you modify any packet, drop it or even forge and insert a completely new one. Using Windows Packet Filter requires no experience in kernel mode programming on your behalf since it provides you with a powerful user level API. However, if you need to implement your solution (to achieve better performance) in kernel mode, you can do that as well by adding your functional code directly to Windows Packet Filter driver’s code.
