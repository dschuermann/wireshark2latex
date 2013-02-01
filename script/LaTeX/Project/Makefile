all:
.ifdef project
.if !exists(${project})
	@echo "Creating new project subdir:" ${project}
	@mkdir ${project}
	@cp sip-call/Makefile ${project}
	@cat sip-call/call.cfg | sed -e s/^/#comment#/ > ${project}/example.cfg
	@echo `pwd`/${project} is created
.else
	@echo ${project} "- the project already exists"
.endif
.else
	@echo "Usage :  make project=sub-dir-name"
.endif

