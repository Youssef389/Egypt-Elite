$(document).ready(function(){

  $('.service')[0].click();

  setServiceHeight();
    
  // open menu in mobile mode
  var menu_check = false;
  $('.menu-toggle').click(function(){
    if (!menu_check) {
      showMenu();
      menu_check = true;
    }else{
      hideMenu();
      menu_check = false;
    }
  })

  function showMenu(){
    $('.menu-toggle').addClass('active');
    $('.menu ul').css('visibility', 'visible');
    $('.menu ul').css('opacity', '1');
    $('.menu ul').css('margin-top', '0px');
  }

  function hideMenu() {
    $('.menu-toggle').removeClass('active');
    $('.menu ul').css('visibility', 'hidden');
    $('.menu ul').css('opacity', '0');
    $('.menu ul').css('margin-top', '50px');
  }

  $(window).resize(function() {
    if($(window).width() > 1100){
      showMenu();
      menu_check = true;
    }else{
      hideMenu();
      menu_check = false;
    }

    setServiceHeight();
  });


  $('.service').click(function(){
    var ul_count = $('ul', this);
    var ul_height = 0;
    for (let i = 0; i < ul_count.length; i++) {
      ul_height += ($(ul_count[i]).height() + 10);
    }      
    var service_height = $('h1', this).height() + ul_height + 50;
    setServiceHeight();
    $(this).css('max-height', service_height + 'px');
  })

  function setServiceHeight(){
    var titles = $('.service .service-title h1');
    var title_height = 0;
    for (let i = 0; i < titles.length; i++) {
      title_height = $(titles[i]).height() + 40;
      $(titles[i]).parent().parent().css('max-height', title_height + "px");
    }
  }

  var hashTagActive = "";
  $("a.scroll").click(function (event) {
    event.preventDefault();
    //calculate destination place
    var dest = 0;
    if ($(this.hash).offset().top > $(document).height() - $(window).height()) {
        dest = $(document).height() - $(window).height();
    } else {
        dest = $(this.hash).offset().top;
    }
    //go to destination
    $('html,body').animate({
        scrollTop: dest
    }, 800, 'swing');
    hashTagActive = this.hash;
  });
})