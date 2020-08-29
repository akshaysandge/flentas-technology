# flentas-technology



class   Test 
{ 
	

	static long minimumCost(long price[], int n) 
	{ 
	
		
		Arrays.sort(price); 
		
		long totalCost = 0; 
	

		for (int i = n - 1; i > 1; i -= 2) 
		{ 
			if (i == 2) 
			{ 
				totalCost += price[2] + price[0]; 
			} 
			else
			{ 
	
			
				long price_first = price[i] + price[0] + 2 * price[1]; 
				long price_second = price[i] + price[i - 1] + 2 * price[0]; 
				totalCost += Math.min(price_first, price_second); 
			} 
		} 
	
	 
		if (n == 1) 
		{ 
			totalCost += price[0]; 
		} 
		else
		{ 
			totalCost += price[1]; 
		} 
	
		return totalCost; 
	} 
	
	
	public static void main (String[] args) 
	{ 
		long price[] = { 1321,2450 }; 
		int n = price.length; 
	
		System.out.println(minimumCost(price, n)); 
	} 
} 










