output_name = force_regs.random.ucli

$(output_name): force_regs.ucli
	awk 'BEGIN{srand();}{if ($$1 != "") { print $$1,$$2,$$3,int(rand()*2)}}' $< > $@

foo.txt:
	touch foo.txt
	make $(output_name)
clean:
	rm -f $(output_name)
