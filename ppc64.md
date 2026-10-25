# Port Qubes OS to ppc64 (POWER9)

Tracking document for porting Qubes OS to the ppc64/POWER9 architecture, so that
Qubes can run on fully open hardware such as the Raptor Computing Systems
Talos II and Blackbird.

## Motivation

Qubes OS is currently x86-only, which ties it to unauditable firmware. The Power
architecture (POWER9) ships with open schematics, open firmware and open
software, making it a much better fit for a security-focused OS.

## Status

**Decision (2022-03-26): option 1, Xen on Power.** All participants agree that
the Xen ppc64 port is the way forward. The other options below are kept for
reference only.

## Options considered

1. **Xen ppc64 port** (chosen). Raptor Computing Systems has offered free
   hardware to incentivize the work.
2. **seL4 microkernel** (see #3894). seL4 is already looking into Power support,
   but Qubes integration on seL4 is far from ready.
3. **KVM via the Hypervisor Abstraction Layer (HAL).** HAL uses libvirt and is
   meant to support multiple hypervisors, but today only Xen is implemented.

## Funding

Bounty: 3 bitcoin (see issue title).

| Date | Contributor | Amount |
|------|-------------|--------|
| 2022-05-07 | Robert Spigler | 0.35 BTC + Blackbird bundle |
| 2022-05-07 | @leo-lb | 0.8 BTC (to be confirmed) |
| | **Total pledged** | **1.15 BTC** |

@madscientist159 offered to do the Xen port for 2 BTC (Xen port only, no Qubes
integration). The OpenPOWER Foundation has issued a statement of support.

## Work breakdown

### Phase 1: Xen on ppc64

- [ ] Build Xen for ppc64 on POWER9 hardware
- [ ] Bring up the Xen hypervisor on Talos II / Blackbird
- [ ] Domain 0 boot
- [ ] Basic domU creation and destruction
- [ ] PCI passthrough
- [ ] Upstream the Xen ppc64 patches

### Phase 2: Qubes integration

- [ ] `core-vchan-xen` on ppc64
- [ ] `core-qrexec` on ppc64
- [ ] `core-qubesdb` on ppc64
- [ ] `core-admin` / `core-admin-client` on ppc64
- [ ] `core-libvirt` on ppc64
- [ ] `gui-daemon` / `gui-agent-linux` on ppc64
- [ ] dom0 userspace packages for ppc64
- [ ] Installer and ISO for ppc64

### Phase 3: Hardening and release

- [ ] Verify IOMMU support on POWER9
- [ ] Verify measured boot / TPM integration
- [ ] Document hardware requirements
- [ ] Continuous integration on ppc64

## Hardware

- Raptor Computing Systems Talos II
- Raptor Computing Systems Blackbird

## References

- Issue: Port Qubes to ppc64
- seL4 tracking issue: #3894
- OpenPOWER Foundation statement of support
