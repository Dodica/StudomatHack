
jQuery(document).ready(function($) {

    $(document).on('submit','form.formaOdjavaIspit',function(e){
        e.preventDefault();
        $(e.currentTarget).find("button").attr("disabled", true);
        var forma = $(e.currentTarget).closest("form");

    });

    $('button.daOdjava').click(function () {
        $(this).attr("disabled", true);
        var waitText=$(this).data('waittext');
        $(this).html('<i class="fa fa-spinner fa-spin spinButton"></i>' + waitText);
        var formId=$(this).data('formid');
        $.ajax({
            "data": $('#'+formId).serialize(),
            "method": "POST",
            "url": $('#'+formId).attr("action")
        }).done(function (data) {
            location.href = data;
        });
    });

    $('div[id^=odjava]').on('hide.bs.modal', function (e) {
        $("button.isp").attr("disabled", false)
    })
});