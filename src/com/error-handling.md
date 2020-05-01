Errors and error handling
=========================

This extension will throw instances of the class <span
class="classname">com\_exception</span> whenever there is a potentially
fatal error reported by COM. All COM exceptions have a well-defined
*code* property that corresponds to the HRESULT return value from the
various COM operations. You may use this code to make programmatic
decisions on how to handle the exception.
