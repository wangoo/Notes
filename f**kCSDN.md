(function() {
    'use strict';
 
    //优化登陆后复制
    $('code').css({'user-select':'unset'})
    $('#content_views pre').css({'user-select':'unset'})
 
 
    //移除“登陆后复制”按钮
     $('.hljs-button').remove();
    //移除readmore按钮，并显示全文
    $('.hide-article-box').remove();
    $('.article_content').css({'height':'initial'})
 
 
    //去除复制后的copyright小尾巴

    document.querySelectorAll('*').forEach(item=>{
    item.oncopy = function(e) {
        e.stopPropagation();
    }
})
 
 
})();
