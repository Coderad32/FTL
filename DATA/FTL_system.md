```perl

#!/usr/bin/env perl
use strict;
use warnings;

# =====================================================================
# APPLICATION DATA EXAMPLE DATA GUIX - REWRITTEN IN PERL
# SOURCE CODE MIT CC - CA - CS - CB - CV Version 2.3.0
# Serial Build: 1 | Sector 9 | Version Number 3 | CLASSIFICATION: ALPHA
# =====================================================================

package Application::FTL;

use subs qw(
    CONNECTING_TOPDIR
    RELAY_SERVICE_MODULE
    SERVICE_MODULE
    SUPPORT_MODULE
    handle_menu_choice
);

# Global configurations and constants
our $VERSION = '2.3.0';
use constant TOPDIR => 'DATA/application';

sub CONNECTING_TOPDIR {
    my ($target) = @_;
    print "[INFO] Connecting to TOPDIR: $target ... LOADING UIX\n";
    # Simulated connection and patch updates
    print "[INFO] Update Linux stat for patchwork complete.\n";
    return 1;
}

sub RELAY_SERVICE_MODULE {
    my ($service_id) = @_;
    print "[RELAY] Relaying service module for ID: $service_id\n";
    return { status => 'success', id => $service_id };
}

sub SERVICE_MODULE {
    my ($service_id) = @_;
    print "[SERVICE] Initializing service module for: $service_id\n";
    return 1;
}

sub SUPPORT_MODULE {
    my ($division) = @_;
    print "[SUPPORT] Engaging support module for division: " . ($division // 'default') . "\n";
    return 1;
}

sub run_pipeline {
    my %config = (
        user      => 'coderad32',
        name      => 'github.com/coderad32',
        service_id => 'shields.io',
        route     => 'application/route/path'
    );

    print "========================================\n";
    print " FTL OPEN ONLINE - SYSTEM INITIALIZED\n";
    print "========================================\n";

    # Load hardware device simulation
    print "[USB1] Loading from device hardware...\n";
    
    # Connect and index TOPDIR
    CONNECTING_TOPDIR(TOPDIR);

    # Authentication and Service ID Routing
    print "[AUTH] Authenticating to mainframe for service: $config{service_id}\n";
    SERVICE_MODULE($config{service_id});
    RELAY_SERVICE_MODULE($config{service_id});

    # Simulated asynchronous execution loop
    my $counter = 0;
    while ($counter < 1) {
        # OPSEC Service ID Array Caller Callback Simulation
        SUPPORT_MODULE('array caller division');
        $counter++;
    }

    return %config;
}

# Interactive Menu Interface (GUIX / UIX Simulation)
sub display_menu {
    print "\n" . ("=" x 40) . "\n";
    print " GUIX: INTERFACE LOADED FROM USB1 SANDISK USB-DEVICE\n";
    print ("=" x 40) . "\n";
    print "0. Exit Program\n";
    print "1. Launch setup.exe*\n";
    print "2. <-- Settings -->\n";
    print "3. \$: Configurations\n";
    print "4. // OpenFiles Quick Fixes Patchwork\n";
    print "5. XTTPS XSSL ( Custom Protocol UIX )\n";
    print "6. VMOS VIRTUAL BOX ISO\n";
    print "7. Mars Preserve Co-Op\n";
    print "8. AI BLOCKCHAIN\n";
    print "9. SIGIL CUBE MATRIX\n";
    print "----------------------------------------\n";
    print "Select an option [0-9]: ";
}

sub handle_menu_choice {
    my ($choice) = @_;
    
    # Handle user choice cleanly using conditional logic
    if (!defined $choice) {
        return 0;
    }

    for ($choice) {
        /^0$/ && do { print "Exiting program...\n"; return 0; };
        /^1$/ && do { print "Launching setup.exe...\n"; last; };
        /^2$/ && do { print "Opening Settings...\n"; last; };
        /^3$/ && do { print "Loading Configurations...\n"; last; };
        /^4$/ && do { print "Applying OpenFiles Quick Fixes Patchwork...\n"; last; };
        /^5$/ && do { print "Initializing XTTPS XSSL Custom Protocol UIX...\n"; last; };
        /^6$/ && do { print "Loading VMOS VIRTUAL BOX ISO...\n"; last; };
        /^7$/ && do { print "Connecting to Mars Preserve Co-Op...\n"; last; };
        /^8$/ && do { print "Initializing AI BLOCKCHAIN...\n"; last; };
        /^9$/ && do { print "Rendering SIGIL CUBE MATRIX...\n"; last; };
        print "Invalid selection or unhandled command.\n";
    }
    return 1;
}

# Main Execution Guard
if (caller0) { # Standard execution check
    my %result_data = run_pipeline();
    
    # If running interactively, show menu loop
    if (-t STDIN) {
        my $running = 1;
        while ($running) {
            display_menu();
            chomp(my $input = <STDIN>);
            $running = handle_menu_choice($input);
        }
    }
}
1;
__END__
```
