#### APIs
##### Cal_Distribution_Pdf_Cdf
Cals the distribution PDF and CDF

`int  Cal_Distribution_Pdf_Cdf(
			int distributionType,
			double min,
			double max,
			double mode,
			double mean,
			double variance,
			std::size_t length,
			double* pdfX,
			double* pdfY,
			double* cdfX,
			double* cdfY);`
- (in)distributionType: Type of the distribution. 0-normal,1-log normal,2-union,3-triangle
- (in)min: The minimum.
- (in)max: The maximum.
- (in)mode: The mode.
- (in)mean: The mean.
- (in)variance: The variance.
- (in)length: The length.
- (out)pdfX: The PDF x.
- (out)pdfY: The PDF y.
- (out)cdfX: The CDF x.
- (out)cdfY: The CDF y.
- return: 0-success,1-check error

##### Cal_Distribution_inv
Cals the distribution inv.

`int  Cal_Distribution_inv(
			int distributionType,
			double min,
			double max,
			double mode,
			double mean,
			double variance,
			std::size_t length,
			double* arrayInv,
			double* arrayRnd,
			double& u);`
- (in)distributionType: Type of the distribution. 0-normal,1-log normal,2-union,3-triangle
- (in)min: The minimum.
- (in)max: The maximum.
- (in)mode: The mode.
- (in)mean: The mean.
- (in)variance: The variance.
- (in)length: The length.
- (out) arrayInv: result set of 
- (out) arrayRnd: random sequence
- (out) u: mean value
- return: return value 0-success,1-check error

##### Cal_CumFrequency
probability distribution of geological reserves

`int Cal_CumFrequency(double* arratOOIP, int ooipNumber, double * arrayX, double * arrayY, int length)`
- (in)arratOOIP: geological reserves
- (in)ooipNumber: number
- (out)arrayX: geological reserves
- (out)arrayY: probability 
- (in)length: size
- return: return value,0-success,1-check error


      
