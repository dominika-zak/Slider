# Slider
 <script>
    	$(document).ready(function() {
    		wysokosc=$('.banef').height();
    		$('.blenda').height(wysokosc);
    		$('.col-md-4').height(wysokosc);
    		$('.buttom').css('top',wysokosc/2-$('.buttom').height()/2);
    		szerokosc=$('.banef').width();
    		$('.col-md-3').width(szerokosc/4);
    		$('.buttom').css('left',szerokosc/2-$('.buttom').width()/2);
    		setInterval(function(){ 
    		$('.active').next('.picture').addClass('active'); 
    					
    					if($('.active').next('.picture').children().length==0){
    					$('.picture').first('.picture').addClass('active');
    					$( ".active" ).last().removeClass('active');
    					}
    					else{
    				$( ".active" ).first().removeClass('active');
    				}
    				$('.active1').removeClass('active1');
    				zmienna=$('.active').children().attr('src');
    			$('.miniature').children().children().each(function(){
    				if($(this).attr('src')==zmienna){
    					$(this).addClass('active1');
    				}
    			})
    			 }, 5000);	
    		$('.miniature').children().children().click(function(){
    			$('.active').removeClass('active');

    			zmienna1=$(this).attr('src');
    			$('.picture').each(function(){
    				if($(this).children().attr('src')==zmienna1){
    					//$('.active').removeClass('active');

    					$(this).addClass('active');
    				}
    			})
    		})
    		$('.strzalka-right').click(function(){
    			$('.active').next('.picture').addClass('active'); 
    					
    					if($('.active').next('.picture').children().length==0){
    					$('.picture').first('.picture').addClass('active');
    					$( ".active" ).last().removeClass('active');
    					}
    					else{
    				$( ".active" ).first().removeClass('active');
    				}
    				$('.active1').removeClass('active1');
    				zmienna=$('.active').children().attr('src');
    			$('.miniature').children().children().each(function(){
    				if($(this).attr('src')==zmienna){
    					$(this).addClass('active1');
    				}
    			})
    		})
    		$('.strzalka-left').click(function(){
    			$('.active').prev('.picture').addClass('active'); 
    					
    					if($('.active').prev('.picture').children().length==0){
    					$('.picture').last('.picture').addClass('active');
    					$( ".active" ).first().removeClass('active');
    					}
    					else{
    				$( ".active" ).last().removeClass('active');
    				}
    				$('.active1').removeClass('active1');
    				zmienna=$('.active').children().attr('src');
    			$('.miniature').children().children().each(function(){
    				if($(this).attr('src')==zmienna){
    					$(this).addClass('active1');
    				}
    			})
    		})
    		
    		
    		
    		})
    		
    		
    		
    		
    		
    </script>
