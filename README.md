Biquad Filter Implementation
============================

* Original code by Nigel Redmon (http://www.earlevel.com/main/2012/11/26/biquad-c-source-code/)

This is an implementation of a Biquad filter implemented as an Arduino library.

Supported filter types:

* Low Pass
* High Pass
* Band Pass
* Notch
* Peaking
* Low Shelf
* High Shelf

----

Methods:

* Constructors

    Biquad();
    Biquad(int type, double Fc, double Q, double peakGainDB);

* Destructor

    ~Biquad();

* Configure the filter

    void setBiquad(int type, double Fc, double Q, double peakGain);

* Same as above but broken into separate parts

    void setType(int type);
    void setQ(double Q);
    void setFc(double Fc);
    void setPeakGain(double peakGainDB);

* Process a sample and return the filtered result

    float process(float in);
    
