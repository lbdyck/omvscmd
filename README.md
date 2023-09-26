# OMVSCMD

OMVSCMD is an ISPF dialog that execute any OMVS command, or commands
if separated by &&, and display the results in Browse or Edit.

Installation is to copy the OMVSCMD exec from this PDS into a library in
your SYSPROC or SYSEXEC allocations.

## Description
 Name:      OMVSCMD

 Function:  Issue a OMVS command for the passed option or prompt for a
            command.  Then display the results in ISPF Edit or Browse.

            If no command is provided then a popup panel appears to
            prompt for the OMVS command.

 Syntax:    %OMVSCMD cmd
            or
            %OMVSCMD -E cmd   (to edit the results of the cmd)

            cmd is optional and if provided that will be used,
            otherwise the user will be prompted for a OMVS command.

 Usage:     Best used when added to the site ISPF command table:

            Verb:   ocmd
            T:      0
            Action: select cmd(%OMVSCMD &zparm)

            Then the user can enter:  ocmd xxx
                                 or:  ocmd  (to be prompted)

