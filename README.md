# sfa_health - Monitor the health of a DDN SFA

    Monitor the health of multiple DDN SFA controllers.

## Dependencies

    DDN SFA library

    The DDN SFA library must be obtained through your
    DDN support contract (https://www.ddn.com)

### CentOS/RedHat

    python3
    python-configparser
    python36-tabulate

## Usage
    usage: sfa_health [-h] [-C CONFIG_FILE] [-d] [-l] [-t] [--no-stdout]
                    [-c CONTROLLERS] [-e EMAIL_RECIPIENTS] [--reply-to REPLY_TO]
                    [-m MAIL_SERVER] [--subject-extra SUBJECT_EXTRA]
                    [--no-email-healthy] [-k KEEP_DAYS] [-r REPORT_DIR] [-s]

    Check SFA system for failed components

    optional arguments:
    -h, --help            show this help message and exit

    General control options:
    -C CONFIG_FILE, --config CONFIG_FILE
                            Specify an alternate configuration file [default:
                            /usr/local/etc/sfa_health.conf]
    -d, --debug           Print debugging messages
    -l, --syslog          Log progress to syslog
    -t, --timestamp       Add timestamp to notification messages
    --no-stdout           Do not print the report to stdout

    Controller options:
    -c CONTROLLERS, --controller CONTROLLERS
                            Specify a SFA controller (use multiple times for
                            multiple controllers

    Email control options:
    -e EMAIL_RECIPIENTS, --recipient EMAIL_RECIPIENTS
                            Specify email recipient (use multiple times for
                            multiple recipients)
    --reply-to REPLY_TO   Specify where replies should be sent
    -m MAIL_SERVER, --mail-server MAIL_SERVER
                            Specify mail server for sending reports
    --subject-extra SUBJECT_EXTRA
                            Extra text to include in the subject line (useful for
                            marking test reports)
    --no-email-healthy    Do not email reports when the system is healthy

    Report control options:
    -k KEEP_DAYS, --keep-days KEEP_DAYS
                            Number of days to keep reports
    -r REPORT_DIR, --report-dir REPORT_DIR
                            Specify the directory in which to write the reports to
    -s, --short-report    Report non-healthy elements only

