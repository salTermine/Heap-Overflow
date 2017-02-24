# Heap Overflow Exploit

	Note that the heap overflow vulnerability resides within heap delete function 
	in my malloc.c. This function is called within my malloc as well as my free. 
	In theory, one could exploit it from either place. However, the heap bocks have 
	to be arranged in a certain way in order for this work. So, you may need to use 
	the u, p and l commands a few times to make sure that heap blocks are ordered 
	in just the right way for your attack to work.
    

	Exercise a heap overflow in my malloc to overwrite the pointer to bcopy in the 
	global offset table (GOT) so that it instead points to ownme.

	Exercise a heap overflow in my free to overwrite the pointer to bcopy in the 
	global offset table (GOT) so that it instead points to ownme.

	Repeat one of the above, but overwrite the return address on the stack instead of 
	a GOT address. Your exploit should result in your injected code exploit to be 
	triggered when main returns. (As before, the exploit can simply call owmne().