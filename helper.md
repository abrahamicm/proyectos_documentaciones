```php
# admin_helper.php
app_admin_head() : mixed
app_admin_footer() : null
init_head([bool $aside = true ]) : mixed
init_tail() : mixed
admin_url([mixed $url = '' ]) : string
staff_can(string $capability[, string $feature = null ][, mixed $staff_id = '' ]) : bool
has_role_permission(mixed $role_id, string $capability, string $feature) : bool
has_permission(string $permission[, mixed $staffid = '' ][, mixed $can = '' ]) : bool
load_admin_language([string $staff_id = '' ]) : string
get_admin_uri() : string
is_admin([mixed $staffid = '' ]) : bool
admin_body_class([mixed $class = '' ]) : mixed
get_admin_body_class([mixed $class = '' ]) : mixed
render_admin_js_variables() : void
_maybe_system_setup_warnings() : mixed

# app_email_helper.php
valid_email(string $address) : bool
name_email_format(mixed $name, mixed $email) : mixed

# assets_helper.php
init_admin_assets() : mixed
init_customers_area_assets() : mixed
init_admin_auth_assets() : mixed
_init_admin_assets() : mixed
add_calendar_assets([mixed $group = 'admin' ]) : mixed
add_moment_js_assets([mixed $group = 'admin' ]) : mixed
add_favicon_link_asset([mixed $group = 'admin' ]) : mixed
add_jquery_validation_js_assets([mixed $group = 'admin' ]) : mixed
add_bootstrap_select_js_assets([mixed $group = 'admin' ]) : mixed
add_dropbox_js_assets([mixed $group = 'admin' ]) : mixed
add_google_api_js_assets([mixed $group = 'admin' ]) : mixed
add_admin_tickets_js_assets() : mixed
add_datatables_js_assets([mixed $group = 'admin' ]) : mixed
app_compile_css([mixed $group = 'admin' ]) : mixed
app_compile_scripts([mixed $group = 'admin' ]) : mixed
is_contact_email_verified([mixed $id = null ]) : bool
is_email_verification_enabled() : bool
is_client_id_used(mixed $id) : bool
customer_has_subscriptions(mixed $id) : bool
get_client([mixed $id = null ]) : mixed
get_customer_profile_tabs() : array<string|int, mixed>
filter_client_visible_tabs(array<string|int, mixed> $tabs[, int $id = '' ]) : array<string|int, mixed>
app_init_customer_profile_tabs() : null
get_client_id_by_lead_id(mixed $id) : mixed
is_primary_contact([string $contact_id = '' ]) : bool
is_client_using_multiple_currencies([mixed $clientid = '' ][, mixed $table = null ]) : booelan
is_empty_customer_company(mixed $id) : bool
get_customer_profile_file_sharing([array<string|int, mixed> $where = [] ]) : array<string|int, mixed>
get_user_id_by_contact_id(mixed $id) : mixed
get_primary_contact_user_id(mixed $userid) : mixed
get_contact_full_name([string $contact_id = '' ]) : string
contact_profile_image_url(mixed $contact_id[, string $type = 'small' ]) : string
get_company_name(mixed $userid[, mixed $prevent_empty_company = false ]) : mixed
get_client_default_language([mixed $clientid = '' ]) : mixed
is_customer_admin(mixed $id[, staff_id $staff_id = '' ]) : bool
have_assigned_customers([mixed $staff_id = '' ]) : bool
has_contact_permission(string $permission[, string $contact_id = '' ]) : bool
load_client_language([string $customer_id = '' ]) : string
client_have_transactions(mixed $id) : bool
get_contact_permissions() : array<string|int, mixed>
get_contact_permission(mixed $name) : mixed
can_contact_view_email_notifications_options() : bool
login_as_client(mixed $id) : mixed
send_customer_registered_email_to_administrators(mixed $client_id) : mixed
contact_consent_url(mixed $contact_id) : string
get_all_customer_attachments(mixed $id) : array<string|int, mixed>
_check_vault_entries_visibility(array<string|int, mixed> $entries) : array<string|int, mixed>
get_sql_select_client_company([string $as = 'company' ]) : string
can_loggged_in_user_manage_contacts() : bool
is_individual_client() : bool
set_contact_language(mixed $lang[, mixed $duration = 60 * 60 * 24 * 31 * 3 ]) : void
get_contact_language() : string
is_automatic_calling_codes_enabled() : bool

# contracts_helper.php
get_contract_shortlink(object $contract) : string
check_contract_restrictions(int $id, string $hash) : void
get_contract_templates() : array<string|int, mixed>
send_contract_signed_notification_to_staff(int $contract_id) : void
count_recently_created_contracts([int $days = 7 ][, int|null $staffId = null ]) : int
count_active_contracts([int|null $staffId = null ]) : int
count_expired_contracts([int|null $staffId = null ]) : int
count_trash_contracts([int|null $staffId = null ]) : int

# core_hooks_helper.php
_maybe_set_identification_key() : mixed
core_merge_fields(array<string|int, mixed> $fields) : array<string|int, mixed>
_maybe_add_estimate_request_link_in_customers_area() : mixed

# countries_helper.php
get_all_countries() : array<string|int, mixed>
get_country(mixed $id) : object
get_country_short_name(mixed $id) : mixed
get_country_name(mixed $id) : mixed

# credit_notes_helper.php
total_credits_applied_to_invoice(mixed $id) : mixed
credit_note_status_color_pdf(mixed $status_id) : string
invoices_statuses_available_for_credits() : array<string|int, mixed>
credits_can_be_applied_to_invoice(mixed $status_id) : bool
is_last_credit_note(mixed $id) : bool
format_credit_note_number(mixed $id) : string
format_credit_note_status(mixed $status[, bool $text = false ]) : string
get_credit_note_item_taxes(mixed $itemid) : array<string|int, mixed>

# custom_fields_helper.php
render_custom_fields(string $belongs_to[, mixed $rel_id = false ][, array<string|int, mixed> $where = [] ][, array<string|int, mixed> $items_cf_params = [] ]) : mixed
get_custom_fields(string $field_to[, array<string|int, mixed> $where = [] ][, bool $exclude_only_admin = false ]) : array<string|int, mixed>
_maybe_translate_custom_field_name(mixed $name, mixed $slug) : mixed
get_table_custom_fields(string $field_to) : array<string|int, mixed>
get_custom_field_value(mixed $rel_id, mixed $field_id_or_slug, string $field_to[, string $format = true ]) : string
handle_custom_fields_post(mixed $rel_id, array<string|int, mixed> $custom_fields[, mixed $is_cf_items = false ]) : bool
get_items_custom_fields_for_table_html(mixed $rel_id, string $rel_type) : array<string|int, mixed>
render_custom_fields_items_table_add_edit_preview() : string
render_custom_fields_items_table_in(array<string|int, mixed> $item, mixed $part_item_name) : string
get_company_custom_fields() : array<string|int, mixed>
is_cf_date(array<string|int, mixed> $field) : bool
is_custom_fields_for_customers_portal() : mixed
get_custom_fields_hyperlink_js_function() : stirng
is_custom_fields_smart_transfer_enabled() : mixed

# database_helper.php
is_reference_in_table(string $field, string $table, int $id) : bool
add_views_tracking(string $rel_type, mixed $rel_id) : mixed
get_views_tracking(string $rel_type, mixed $rel_id) : array<string|int, mixed>
log_activity(string $description[, int $staffid = null ]) : mixed
get_last_system_activity_id() : mixed
add_notification(array<string|int, mixed> $values) : mixed
total_rows(string $table[, array<string|int, mixed> $where = [] ]) : mixed
sum_from_table(string $table[, array<string|int, mixed> $attr = [] ]) : mixed
prefixed_table_fields_wildcard(string $table, string $alias, string $field) : string
prefixed_table_fields_array(string $table[, bool $string = false ][, array<string|int, mixed> $exclude = [] ]) : array<string|int, mixed>|string
prefixed_table_fields_string(string $table[, array<string|int, mixed> $exclude = [] ]) : string
get_department_email(mixed $id) : mixed
add_foreign_key(string $table, string $foreign_key, string $references[, string $on_delete = 'RESTRICT' ][, string $on_update = 'RESTRICT' ]) : string
drop_foreign_key(string $table, string $foreign_key) : string
add_trigger(string $trigger_name, string $table, string $statement[, string $time = 'BEFORE' ][, string $event = 'INSERT' ][, string $type = 'FOR EACH ROW' ]) : string
drop_trigger(string $trigger_name) : string
table_exists(string $table) : bool
data_tables_init(array<string|int, mixed> $aColumns, mixed $sIndexColumn, string $sTable[, array<string|int, mixed> $join = [] ][, array<string|int, mixed> $where = [] ][, array<string|int, mixed> $additionalSelect = [] ][, string $sGroupBy = '' ][, mixed $searchAs = [] ]) : array<string|int, mixed>
get_null_columns_that_should_be_sorted_as_last() : array<string|int, mixed>
render_datatable([array<string|int, mixed> $headings = [] ][, string $class = '' ][, array<string|int, mixed> $additional_classes = [''] ][, array<string|int, mixed> $table_attributes = [] ]) : string
get_datatables_language_array() : array<string|int, mixed>
prepare_dt_filter(array<string|int, mixed> $filter) : string
get_table_last_order(string $tableID) : string

# deprecated_helper.php
_deprecated_function(string $function, string $version[, string $replacement = null ]) : mixed
_deprecated_hook(mixed $hook, mixed $version[, mixed $replacement = null ][, mixed $message = null ]) : mixed
_has_deprecated_errors_admin_body_class() : void
_add_has_deprecated_errors_admin_body_class(mixed $classes) : array<string|int, mixed>
_startsWith(mixed $haystack, mixed $needle) : mixed
get_table_items_html_and_taxes(mixed $items, mixed $type[, mixed $admin_preview = false ]) : mixed
get_table_items_pdf_and_taxes(mixed $items, mixed $type) : mixed
get_project_label(mixed $id[, mixed $replace_default_by_muted = false ]) : mixed
project_status_color_class(mixed $id[, mixed $replace_default_by_muted = false ]) : mixed
get_task_priority_class(mixed $id) : string
project_status_by_id(mixed $id) : mixed
format_seconds(mixed $seconds) : mixed
can_logged_in_contact_change_language() : mixed
add_encryption_key_old() : mixed
app_admin_ajax_search_function() : mixed
number_unformat(mixed $number[, mixed $force_number = true ]) : mixed
app_select_plugin_js([string $locale = 'en' ]) : mixed
app_jquery_validation_plugin_js([string $locale = 'en' ]) : mixed
get_email_template_for_sending(string $template_slug, string $email) : object
_parse_email_template_merge_fields(object $template, array<string|int, mixed> $merge_fields) : object
get_client_email_templates_slugs() : array<string|int, mixed>
get_staff_email_templates_slugs() : array<string|int, mixed>
get_email_template_language(string $template_slug, string $email) : string
default_aside_menu_active() : string
add_main_menu_item([mixed $options = [] ][, mixed $parent = '' ]) : string
add_setup_menu_item([mixed $options = [] ][, mixed $parent = '' ]) : string
default_setup_menu_active() : string
get_table_items_and_taxes(array<string|int, mixed> $items, string $type[, bool $admin_preview = false ]) : array<string|int, mixed>
_format_number(mixed $total[, bool $foce_check_zero_decimals = false ]) : mixed
mutiple_taxes_found_for_item(array<string|int, mixed> $taxes) : bool
template_assets_url() : string
template_assets_path() : string
render_custom_styles(mixed $type) : mixed
format_money(mixed $total[, string $symbol = '' ]) : string
app_stylesheet(string $path, string $filename) : string
app_script(string $path, string $filename) : string
add_projects_assets([mixed $group = 'admin' ]) : mixed
check_missing_language_strings(string $language) : void
logActivity(string $description[, int $staffid = null ]) : mixed
get_permission_conditions() : array<string|int, mixed>
handle_google_drive_links_in_text(string $text) : string
_check_deprecated_calendar_view_name_option(mixed $value, mixed $name) : mixed
_check_removed_number_padding_option_name(mixed $value, mixed $name) : mixed
get_task_array_gantt_data(array<string|int, mixed> $task[, mixed $dep_id = null ][, mixed $defaultEnd = null ]) : array<string|int, mixed>

# email_templates_helper.php
prepare_mail_preview_data(string $template, mixed $customer_id_or_email[, mixed $mailClassParams = [] ]) : array<string|int, mixed>
parse_email_template(mixed $template[, array<string|int, mixed> $merge_fields = [] ]) : object
parse_email_template_merge_fields(object $template, array<string|int, mixed> $merge_fields) : object
send_mail_template() : mixed
mail_template(string $class) : mixed
get_mail_template_path(mixed $class, mixed &$params) : mixed
create_email_template(string $subject, string $message, string $type, string $name, string $slug[, int $active = 1 ]) : mixed
is_email_template_active(string $slug) : bool

# emails_tracking_helper.php
email_tracking_inject_in_body(mixed $template) : mixed
add_email_tracking(mixed $data) : mixed
get_tracked_emails(mixed $rel_id, mixed $rel_type) : mixed
delete_tracked_emails(mixed $rel_id, mixed $rel_type) : mixed
get_available_tracking_templates_slugs() : mixed

# estimates_helper.php
get_estimate_shortlink(object $estimate) : string
check_estimate_restrictions(mixed $id, string $hash) : mixed
is_estimates_email_expiry_reminder_enabled() : bool
is_estimates_expiry_reminders_enabled() : bool
estimate_status_color_pdf(mixed $status_id) : string
format_estimate_status(int $status[, string $classes = '' ][, bool $label = true ]) : mixed
estimate_status_by_id(mixed $id) : string
estimate_status_color_class(mixed $id[, bool $replace_default_by_muted = false ]) : string
is_last_estimate(mixed $id) : bool
format_estimate_number(mixed $id) : string
get_estimate_item_taxes(mixed $itemid) : array<string|int, mixed>
get_estimates_percent_by_status(mixed $status[, mixed $project_id = null ]) : array<string|int, mixed>
get_estimates_where_sql_for_staff(mixed $staff_id) : mixed
staff_has_assigned_estimates([mixed $staff_id = '' ]) : bool
user_can_view_estimate(mixed $id[, mixed $staff_id = false ]) : bool

# files_helper.php
render_yes_no_option(string $option_value, string $label[, string $tooltip = '' ][, mixed $replace_yes_text = '' ][, mixed $replace_no_text = '' ][, mixed $replace_1 = '' ][, mixed $replace_0 = '' ]) : mixed
render_input(string $name[, string $label = '' ][, string $value = '' ][, string $type = 'text' ][, array<string|int, mixed> $input_attrs = [] ][, array<string|int, mixed> $form_group_attr = [] ][, string $form_group_class = '' ][, string $input_class = '' ]) : string
render_color_picker(string $name[, string $label = '' ][, string $value = '' ][, array<string|int, mixed> $input_attrs = [] ]) : string
render_date_input(mixed $name[, string $label = '' ][, string $value = '' ][, array<string|int, mixed> $input_attrs = [] ][, array<string|int, mixed> $form_group_attr = [] ][, string $form_group_class = '' ][, string $input_class = '' ]) : string
render_datetime_input(mixed $name[, string $label = '' ][, string $value = '' ][, array<string|int, mixed> $input_attrs = [] ][, array<string|int, mixed> $form_group_attr = [] ][, string $form_group_class = '' ][, string $input_class = '' ]) : string
render_textarea(mixed $name[, string $label = '' ][, string $value = '' ][, array<string|int, mixed> $textarea_attrs = [] ][, array<string|int, mixed> $form_group_attr = [] ][, string $form_group_class = '' ][, string $textarea_class = '' ]) : string
render_select(string $name, array<string|int, mixed> $options[, array<string|int, mixed> $option_attrs = [] ][, string $label = '' ][, string $selected = '' ][, array<string|int, mixed> $select_attrs = [] ][, array<string|int, mixed> $form_group_attr = [] ][, string $form_group_class = '' ][, string $select_class = '' ][, bool $include_blank = true ]) : string
render_select_with_input_group(mixed $name, mixed $options[, mixed $option_attrs = [] ][, mixed $label = '' ][, mixed $selected = '' ][, mixed $input_group_contents = '' ][, mixed $select_attrs = [] ][, mixed $form_group_attr = [] ][, mixed $form_group_class = '' ][, mixed $select_class = '' ][, mixed $include_blank = true ]) : mixed
render_form_builder_field(object $field) : mixed
format_external_form_custom_fields(array<string|int, mixed> $custom_fields) : array<string|int, mixed>
render_estimate_request_status_select(mixed $statuses[, mixed $selected = '' ][, mixed $lang_key = '' ][, mixed $name = 'status' ][, mixed $select_attrs = [] ]) : mixed
access_control_media(mixed $attr, mixed $path, mixed $data, mixed $volume, mixed $isDir, mixed $relpath) : mixed
xcopy(string $source, string $dest[, int $permissions = 0755 ]) : bool
delete_dir(string $dirPath) : bool
is_image(string $path) : bool
get_html5_video_extensions() : array<string|int, mixed>
is_html5_video(string $path) : bool
get_file_extension(string $file_name) : mixed
unique_filename(string $dir, string $filename) : string
sanitize_file_name(string $filename) : mixed
get_mime_class(string $mime) : string
bytesToSize(string $path[, string $filesize = '' ]) : mixed
list_folders(stirng $path) : array<string|int, mixed>
list_files(string $dir) : array<string|int, mixed>
file_upload_max_size() : mixed
replace_in_file(string $path, string $find, string $replace) : bool
parse_upload_size(mixed $size) : int
protected_file_url_by_path(string $path[, bool $preview = false ]) : string
project_file_url(array<string|int, mixed> $file[, bool $preview = false ]) : string
is_markdown_file(string $path) : bool
markdown_parse_preview(string $path) : mixed
get_dir_contents(string $dir[, array<string|int, mixed> &$results = [] ]) : array<string|int, mixed>
app_temp_dir() : string
app_maybe_delete_old_temporary_files() : void
_delete_temporary_files_older_then() : int
validate_file(string $file[, array<string|int, mixed> $allowed_files = [] ]) : int
startsWith(string $haystack, string $needle) : bool
endsWith(string $haystack, string $needle) : bool
is_html(mixed $string) : mixed
strafter(string $string, substring $substring) : string
strbefore(string $string, substring $substring) : string
is_connected([string $domain = 'www.google.com' ]) : bool
str_lreplace(string $search, string $replace, string $subject) : string
get_string_between(string $string, string $start, string $end) : string
time_ago_specific(mixed $date[, string $from = 'now' ]) : mixed
sec2qty(mixed $sec) : int
seconds_to_time_format([int $seconds = 0 ][, bool $include_seconds = false ]) : string
hours_to_seconds_format(mixed $hours) : int
ip_in_range(string $ip, string $range) : bool
array_merge_recursive_distinct(array<string|int, mixed> &$array1, array<string|int, mixed> &$array2) : array<string|int, mixed>
array_to_object(array<string|int, mixed> $array) : object
array_flatten(array<string|int, mixed> $array) : array<string|int, mixed>
value_exists_in_array_by_key(array<string|int, mixed> $array, string $key, mixed $val) : bool
in_array_multidimensional(array<string|int, mixed> $array, mixed $key, mixed $val) : bool
in_object_multidimensional(object $object, mixed $key, mixed $val) : bool
array_pluck( $array,  $key) : plucked
adjust_color_brightness(string $hex, mixed $steps) : string
hex2rgb(string $color) : string
check_for_links(string $ret) : string
time_ago(datetime $date) : mixed
slug_it(string $str[, array<string|int, mixed> $options = [] ]) : mixed
similarity(string $str1, string $str2) : float
app_sort_by_position(array<string|int, mixed> $array[, bool $keepIndex = false ]) : array<string|int, mixed>
app_fill_empty_common_attributes(array<string|int, mixed> $array) : array<string|int, mixed>
strip_html_tags(string $str[, string $allowed = '' ]) : string
adjust_hex_brightness(mixed $hex, mixed $percent) : mixed
app_unserialize(mixed $data) : mixed

# send_gdpr_email_template
send_gdpr_email_template(mixed $template, mixed $user_id) : mixed
is_gdpr() : mixed
load_custom_lang_file(string $language) : void

# general_helper.php
app_generate_short_link(array<string|int, mixed> $data) : mixed
app_archive_short_link(string $link) : bool
get_total_days_overdue(object $duedate) : int
is_rtl([bool $client_area = false ]) : bool
is_data_for_customer() : bool
generate_encryption_key() : stirng
get_app_version() : string
redirect_after_login_to_current_url() : mixed
maybe_redirect_to_previous_url() : null
do_recaptcha_validation([string $str = '' ]) : bool
get_current_date_format([mixed $php = false ]) : string
is_logged_in() : bool
is_client_logged_in() : bool
is_staff_logged_in() : bool
get_staff_user_id() : mixed
get_client_user_id() : mixed
get_contact_user_id() : mixed
get_timezones_list() : array<string|int, mixed>
is_mobile() : bool
set_alert(string $type, string $message) : mixed
blank_page([string $message = '' ][, string $alert = 'danger' ]) : mixed
access_denied([string $permission = '' ]) : mixed
ajax_access_denied() : mixed
set_debug_alert(string $message) : mixed
set_system_popup(string $message) : mixed
get_available_date_formats() : array<string|int, mixed>
get_weekdays() : array<string|int, mixed>
get_weekdays_original() : array<string|int, mixed>
_l(string $line[, mixed $label = '' ][, mixed $log_errors = true ]) : string
_d(date $date) : date
_dt(datetime $date[, mixed $is_timesheet = false ]) : datetime
to_sql_date(string $date[, mixed $datetime = false ]) : mixed
_simplify_date_fix(string $date, string $from_format) : string
is_date(string $date) : bool
get_locales() : array<string|int, mixed>
get_locale_key([string $language = 'english' ]) : string
current_full_url() : string
pusher_trigger_notification([array<string|int, mixed> $users = [] ]) : null
app_generate_hash() : string
get_csrf_for_ajax() : array<string|int, mixed>
csrf_jquery_token() : mixed
app_happy_text(string $text) : string
get_temp_dir() : string
app_hasher() : object
app_hash_password(string $password) : string
get_last_upgrade_copy_data() : mixed
collect(array<string|int, mixed> $items) : Collection

# invoices_helper.php
get_invoice_shortlink(object $invoice) : string
get_invoice_total_left_to_pay(mixed $id[, mixed $invoice_total = null ]) : mixed
is_invoices_email_overdue_notice_enabled() : bool
is_invoices_email_due_notice_enabled() : bool
is_invoices_overdue_reminders_enabled() : bool
is_invoices_due_reminders_enabled() : bool
check_invoice_restrictions(mixed $id, string $hash) : mixed
format_invoice_status(int $status[, string $classes = '' ][, bool $label = true ]) : mixed
get_invoice_status_label(mixed $status) : string
is_invoice_overdue(object|array<string|int, mixed> $invoice) : bool
invoice_status_color_pdf(mixed $status_id) : string
update_invoice_status(mixed $id[, mixed $force_update = false ][, mixed $prevent_logging = false ]) : mixed
is_last_invoice(mixed $id) : bool
format_invoice_number(mixed $id) : string
get_invoice_item_taxes(mixed $itemid) : array<string|int, mixed>
is_payment_mode_allowed_for_invoice(mixed $id, mixed $invoiceid) : bool
found_invoice_mode(array<string|int, mixed> $modes, mixed $invoiceid[, bool $offline = true ][, mixed $show_on_pdf = false ]) : bool
get_invoices_percent_by_status(mixed $status) : array<string|int, mixed>
staff_has_assigned_invoices([mixed $staff_id = '' ]) : bool
load_invoices_total_template() : string
get_invoices_where_sql_for_staff(mixed $staff_id) : mixed
user_can_view_invoice(mixed $id[, mixed $staff_id = false ]) : bool

# leads_helper.php
leads_app_admin_head_data() : mixed
is_lead_creator(mixed $lead_id[, mixed $staff_id = '' ]) : bool
lead_consent_url(mixed $id) : string
leads_public_url(mixed $id) : string
get_lead_hash(mixed $id) : string
get_leads_summary() : array<string|int, mixed>
render_leads_status_select(array<string|int, mixed> $statuses[, string $selected = '' ][, string $lang_key = '' ][, string $name = 'status' ][, array<string|int, mixed> $select_attrs = [] ][, bool $exclude_default = false ]) : string
render_leads_source_select(array<string|int, mixed> $sources[, string $selected = '' ][, string $lang_key = '' ][, string $name = 'source' ][, array<string|int, mixed> $select_attrs = [] ]) : string
load_lead_language(string $lead_id) : string

# menu_helper.php
app_init_admin_sidebar_menu_items() : mixed

# misc_helper.php
show_recaptcha() : bool
get_media_locale() : string
get_tinymce_language(string $locale) : string
get_system_favourite_colors() : array<string|int, mixed>
process_digital_signature_image(mixed $partBase64, mixed $path) : mixed
get_acceptance_info_array([bool $empty = false ]) : array<string|int, mixed>
get_form_accepted_mimes() : string
close_setup_menu() : null
maybe_add_http(string $url) : string
get_alert_class() : string
generate_two_factor_auth_key() : string
optimize_dropbox_thumbnail(string $url[, string $bounding_box = '800' ]) : string
split_weeks_chart_label(array<string|int, mixed> $weeks, mixed $week) : string
get_weekdays_between_dates(object $start_time, objetc $end_time) : array<string|int, mixed>
is_knowledge_base_viewable([bool $excludeStaff = false ]) : bool
_prepare_attachments_array_for_export(mixed $attachments) : mixed
_prepare_items_array_for_export(mixed $items, mixed $type) : mixed
get_all_knowledge_base_articles_grouped([bool $only_customers = true ][, array<string|int, mixed> $where = [] ][, mixed $q = null ]) : array<string|int, mixed>
get_kb_groups() : array<string|int, mixed>
get_announcements_for_user([bool $staff = true ]) : array<string|int, mixed>
app_set_update_message_info(int $version) : mixed
get_scheduled_email_default_date() : string
app_set_pipe_php_permissions() : mixed
app_check_imap_open_function([string $redirectOnError = null ]) : mixed
_maybe_user_is_trying_to_login_into_the_clients_area_as_staff(array<string|int, mixed> $data) : mixed
_maybe_mistaken_login_area_check_performed() : mixed
_maybe_show_just_updated_message() : mixed
show_pdf_unable_to_get_image_size_error() : mixed

# modules_helper.php
register_activation_hook(string $module, mixed $function) : void
register_deactivation_hook(string $module, mixed $function) : void
register_uninstall_hook(string $module, mixed $function) : void
register_merge_fields(mixed $for) : void
add_module_support(string $module_name, string $feature) : void
module_supports(string $module_name, string $feature) : bool
register_cron_task(mixed $function) : void
register_staff_capabilities(string $feature_id, array<string|int, mixed> $config[, string $name = null ]) : void
modules_list_url() : string
register_payment_gateway(string $id, string $module) : void
register_theme_assets_hook(string $function) : bool
module_views_path(string $module[, string $concat = '' ]) : string
module_libs_path(string $module[, string $concat = '' ]) : string
module_dir_path(string $module[, string $concat = '' ]) : string
module_dir_url(string $module[, string $segment = '' ]) : string
register_language_files(string $module[, array<string|int, mixed> $languages = [] ]) : void
uninstallable_modules() : array<string|int, mixed>
do_action_deprecated(string $tag, array<string|int, mixed> $args, string $version[, string $replacement = false ][, string $message = null ]) : mixed
apply_filters_deprecated(string $tag, array<string|int, mixed> $args, string $version[, string $replacement = false ][, string $message = null ]) : mixed

# payment_gateways_helper.php
payment_gateway_logo() : string
payment_gateway_logo_url() : mixed
payment_gateway_head([string $title = 'Payment for Invoice' ]) : mixed
payment_gateway_scripts() : html
payment_gateway_footer() : html

# pdf_helper.php
load_pdf_language(mixed $clientLanguage) : null
pdf_logo_url() : string
get_pdf_fonts_list() : mixed
set_mailing_constant() : mixed
get_pdf_format(string $option_name) : array<string|int, mixed>
invoice_pdf(object $invoice[, string $tag = '' ]) : mixed
credit_note_pdf(object $credit_note[, string $tag = '' ]) : mixed
estimate_pdf(object $estimate[, string $tag = '' ]) : mixed
proposal_pdf(object $proposal[, string $tag = '' ]) : object
contract_pdf(object $contract) : mixed
payment_pdf(mixed $payment[, string $tag = '' ]) : object
statement_pdf(object $statement) : mixed
app_pdf(string $type, mixed $path, mixed ...$params) : object
_bulk_pdf_export_maybe_tag(string $tag, object &$pdf) : null
pdf_multi_row(string $left, string $right, object $pdf[, int $left_width = 40 ]) : null

# pre_query_data_formatters_helper.php
_format_data_sales_feature(array<string|int, mixed> $data) : array<string|int, mixed>
_format_data_client(mixed $data[, mixed $id = null ]) : mixed
_get_sales_feature_unused_names() : array<string|int, mixed>
_get_client_unused_names() : mixed

# projects_helper.php
_maybe_init_admin_project_assets() : mixed
get_project_tabs_admin() : array<string|int, mixed>
app_init_project_tabs() : null
filter_project_visible_tabs(array<string|int, mixed> $tabs, array<string|int, mixed> $applied_settings) : array<string|int, mixed>
get_project([mixed $id = null ]) : mixed
get_project_status_by_id(mixed $id) : array<string|int, mixed>
get_user_pinned_projects() : array<string|int, mixed>
get_project_name_by_id(mixed $id) : string
get_project_milestones(mixed $project_id) : array<string|int, mixed>
get_client_id_by_project_id(mixed $id) : mixed
customer_has_projects(mixed $customer_id) : bool
get_project_billing_type(mixed $project_id) : mixed
get_project_deadline(mixed $project_id) : mixed
get_project_discussions_language_array() : array<string|int, mixed>
project_has_recurring_tasks(mixed $id) : bool
total_project_tasks_by_milestone(mixed $milestone_id, mixed $project_id) : mixed
total_project_finished_tasks_by_milestone(mixed $milestone_id, mixed $project_id) : mixed

# proposals_helper.php
get_proposal_shortlink(object $proposal) : string
check_proposal_restrictions(mixed $id, string $hash) : void
is_proposals_email_expiry_reminder_enabled() : bool
is_proposals_expiry_reminders_enabled() : bool
proposal_status_color_class(mixed $id[, bool $replace_default_by_muted = false ]) : string
format_proposal_status(mixed $status[, string $classes = '' ][, bool $label = true ]) : string
format_proposal_number(mixed $id) : string
get_proposal_item_taxes(mixed $itemid) : array<string|int, mixed>
get_proposals_percent_by_status(mixed $status[, mixed $total_proposals = '' ]) : array<string|int, mixed>
get_proposal_templates() : array<string|int, mixed>
user_can_view_proposal(mixed $id[, mixed $staff_id = false ]) : bool
parse_proposal_content_merge_fields(mixed $proposal) : mixed
staff_has_assigned_proposals([mixed $staff_id = '' ]) : bool
get_proposals_sql_where_staff(mixed $staff_id) : mixed

# relation_helper.php
get_relation_data(string $type[, string $rel_id = '' ][, array<string|int, mixed> $extra = [] ]) : mixed
get_relation_values(mixed $relation, string $type) : mixed
init_relation_options(mixed $data, string $type[, string $rel_id = '' ]) : string

# sales_helper.php
is_using_multiple_currencies([string $table = null ]) : bool
app_format_number(mixed $total[, bool $foce_check_zero_decimals = false ]) : mixed
app_format_money(mixed $amount, mixed $currency[, bool $excludeSymbol = false ]) : string
is_decimal(mixed $val) : bool
multiple_taxes_found_for_item(array<string|int, mixed> $taxes) : bool
ajax_on_total_items() : int
get_tax_by_id(int $id) : object
get_tax_by_name(string $name) : object
_maybe_remove_first_and_last_br_tag(string $text) : string
_info_format_replace(string $mergeCode, mixed $val, string $txt) : string
_info_format_custom_field(mixed $id, string $label, mixed $value, string $txt) : string
_info_format_custom_fields_check(array<string|int, mixed> $custom_fields, string $txt) : string
format_customer_info(object $data, string $for, string $type[, bool $companyLink = false ]) : string
format_proposal_info(object $proposal[, string $for = '' ]) : string
format_organization_info() : string
get_decimal_places() : mixed
get_items_by_type(string $type, mixed $id) : array<string|int, mixed>
update_sales_total_tax_column(mixed $id, mixed $type, mixed $table) : void
_maybe_insert_post_item_tax(mixed $item_id, array<string|int, mixed> $post_item, mixed $rel_id, string $rel_type) : mixed
add_new_sales_item_post(array<string|int, mixed> $item, mixed $rel_id, string $rel_type) : mixed
update_sales_item_post(mixed $item_id, array<string|int, mixed> $data[, string $field = '' ]) : bool
handle_removed_sales_item_post(mixed $id, string $rel_type) : boolena
delete_taxes_from_item(mixed $item_id, string $rel_type) : bool
is_sale_discount_applied(mixed $data) : mixed
is_sale_discount(mixed $data, mixed $is) : mixed
get_items_table_data(object $transaction, string $type[, string $for = 'html' ][, bool $admin_preview = false ]) : object
sales_number_format(mixed $number, mixed $format, mixed $applied_prefix, mixed $date) : mixed
get_currency(mixed $id_or_name) : object
get_base_currency() : object

# settings_helper
add_option(string $name[, string $value = '' ][, int $autoload = 1 ]) : mixed
get_option(string $name) : mixed
update_option(string $name, string $value[, mixed $autoload = null ]) : bool
delete_option(mixed $name) : bool
option_exists(string $name) : bool
app_init_settings_tabs() : mixed

# sms_helper.php
maybe_test_sms_gateway() : mixed
_maybe_sms_gateways_settings_group(mixed $groups) : mixed
app_init_sms_gateways() : mixed
is_sms_trigger_active([mixed $trigger = '' ]) : mixed
can_send_sms_based_on_creation_date(mixed $data_date_created) : mixed

# staff_helper.php
get_available_staff_permissions([array<string|int, mixed> $data = [] ]) : array<string|int, mixed>
get_staff([mixed $id = null ]) : mixed
staff_profile_image_url(mixed $staff_id[, string $type = 'small' ]) : string
staff_profile_image(bool $id[, array<string|int, mixed> $classes = ['staff-profile-image'] ][, string $type = 'small' ][, array<string|int, mixed> $img_attrs = [] ]) : string
get_staff_full_name([string $userid = '' ]) : string
get_staff_default_language([mixed $staffid = '' ]) : mixed
get_staff_recent_search_history([mixed $staff_id = null ]) : mixed
update_staff_recent_search_history(mixed $history[, mixed $staff_id = null ]) : mixed
is_staff_member([string $staff_id = '' ]) : bool

# subscriptions_helper.php
create_subscription_invoice_data(mixed $subscription, mixed $invoice) : mixed
subscription_invoice_preview_data(mixed $subscription[, mixed $upcomingInvoice = null ][, mixed $stripeSubscription = null ]) : mixed
get_subscriptions_statuses() : mixed
subscriptions_summary() : mixed
send_email_customer_subscribed_to_subscription_to_staff(mixed $subscription) : mixed
can_logged_in_contact_view_subscriptions() : mixed
can_logged_in_contact_update_credit_card() : mixed
customer_can_delete_credit_card([mixed $client_id = null ]) : mixed
is_future_subscription_date(mixed $date) : mixed
redirect_to_stripe_checkout(mixed $session_id) : mixed
check_stripe_subscription_environment(mixed $subscription) : mixed

# tags_helper.php
handle_tags_save(string $tags, mixed $rel_id, string $rel_type) : bool
get_tag_by_name(string $name) : object
get_tags() : array<string|int, mixed>
get_tags_clean() : array<string|int, mixed>
get_tags_ids() : array<string|int, mixed>
get_tags_in(string $rel_id, string $rel_type) : array<string|int, mixed>
_call_tags_method(string $method, mixed ...$params) : mixed
prep_tags_input(array<string|int, mixed> $tag_names) : string
render_tags(string $tags) : string

# tasks_helper.php
format_task_status(mixed $status[, bool $text = false ][, bool $clean = false ]) : string
get_tasks_priorities() : array<string|int, mixed>
get_task_subject_by_id(mixed $id) : string
get_task_status_by_id(mixed $id) : array<string|int, mixed>
task_priority(mixed $id) : string
task_priority_color(mixed $id) : string
format_members_by_ids_and_names(string $ids, string $names[, mixed $hidden_export_table = true ][, mixed $image_class = 'staff-profile-image-small' ]) : string
task_rel_name(string $rel_name, mixed $rel_id, string $rel_type) : string
task_rel_link(mixed $rel_id, string $rel_type) : string
tasks_rel_name_select_query() : string
init_relation_tasks_table([array<string|int, mixed> $table_attributes = [] ]) : string
tasks_summary_data([mixed $rel_id = null ][, mixed $rel_type = null ]) : array<string|int, mixed>
get_sql_calc_task_logged_time(mixed $task_id) : mixed
get_sql_select_task_assignees_ids() : mixed
get_sql_select_task_asignees_full_names() : mixed
get_sql_select_task_total_checklist_items() : mixed
get_sql_select_task_total_finished_checklist_items() : mixed
get_tasks_where_string([mixed $table = true ]) : string
get_task_timer_round_off_options() : array<string|int, mixed>
get_task_timer_round_off_times() : array<string|int, mixed>
task_timer_round(int $seconds) : int
is_task_created_by_staff(null|int|string $taskId[, null|int|string $staffId = null ]) : bool

# template_helper.php
html_purify(string $content) : string
clear_textarea_breaks(string $text[, string $replace = '' ]) : string
nl2br_save_html(string $string) : string
app_js_alerts() : null
app_external_form_footer(mixed $form) : mixed
app_external_form_header(mixed $form) : mixed
get_company_logo([string $uri = '' ][, string $href_class = '' ][, string $type = '' ]) : mixed
get_dark_company_logo([string $uri = '' ][, string $href_class = '' ]) : string
_strip_tags(string $html) : string
_inject_no_index() : mixed
icon_btn([string $url = '' ][, string $icon = '' ][, string $class = 'btn-default' ][, array<string|int, mixed> $attributes = [] ]) : string
remove_emojis(mixed $string) : mixed

# themes_helper.php
add_theme_menu_item(mixed $slug, mixed $item) : mixed
no_index_customers_area() : mixed
add_default_theme_menu_items() : mixed
compile_theme_css() : mixed
compile_theme_scripts() : mixed
theme_head_view() : mixed
theme_footer_view() : mixed
theme_template_view() : mixed
app_customers_footer() : mixed
app_customers_head([string $language = null ]) : null
theme_assets_url() : string
theme_assets_path() : string
terms_url() : string
privacy_policy_url() : string
show_recaptcha_in_customers_area() : bool
get_template_part(string $name[, array<string|int, mixed> $data = [] ][, mixed $return = false ]) : mixed
get_all_client_themes() : array<string|int, mixed>
active_clients_theme() : mixed
app_theme_head_hook() : null
_do_clients_area_deprecated_js_vars(mixed $date_format, mixed $locale, mixed $maxUploadSize, mixed $isRTL) : mixed

# tickets_helper.php
AdminTicketsTableStructure([string $name = '' ][, bool $bulk_action = false ]) : mixed
ticket_status_translate(mixed $id) : string
ticket_priority_translate(mixed $id) : string
set_ticket_open(int $current, int $id[, bool $admin = true ]) : mixed
show_ticket_submitter_on_clients_area_table() : bool
can_logged_in_contact_view_all_tickets() : bool
get_clients_area_tickets_summary(array<string|int, mixed> $statuses) : array<string|int, mixed>
can_change_ticket_status_in_clients_area([mixed $status = null ]) : bool
get_ticket_form_accepted_mimes() : string
ticket_message_save_as_predefined_reply_javascript() : mixed
get_ticket_public_url(mixed $ticket) : mixed
ticket_public_form_customers_footer() : mixed

# upload_helper.php
handle_estimate_request_attachments(mixed $estimateRequestId[, mixed $index_name = 'file' ]) : bool
_perfex_upload_error(mixed $error) : mixed
handle_newsfeed_post_attachments(mixed $postid) : array<string|int, mixed>
handle_project_file_uploads(mixed $project_id) : bool
handle_contract_attachment(mixed $id) : bool
handle_lead_attachments(mixed $leadid[, mixed $index_name = 'file' ][, mixed $form_activity = false ]) : bool
handle_task_attachments_array(mixed $taskid[, string $index_name = 'attachments' ]) : mixed
handle_sales_attachments(mixed $rel_id, mixed $rel_type) : array<string|int, mixed>
handle_client_attachments_upload(mixed $id[, mixed $customer_upload = false ]) : array<string|int, mixed>
handle_expense_attachments(mixed $id) : void
handle_ticket_attachments(mixed $ticketid[, mixed $index_name = 'attachments' ]) : mixed
handle_company_logo_upload() : bool
handle_company_signature_upload() : bool
handle_favicon_upload() : bool
handle_staff_profile_image_upload([string $staff_id = '' ]) : bool
handle_contact_profile_image_upload([string $contact_id = '' ]) : bool
handle_project_discussion_comment_attachments(mixed $discussion_id, mixed $post_data, array<string|int, mixed> $insert_data) : arrray
create_img_thumb(string $path, string $filename[, int $width = 300 ][, int $height = 300 ]) : null
_upload_extension_allowed(string $filename) : bool
_file_attachments_index_fix(string $index_name) : null
_maybe_create_upload_path(string $path) : null
get_upload_path_by_type(string $type) : string

# user_meta_helper.php
add_staff_meta(mixed $user_id, mixed $meta_key[, mixed $meta_value = '' ]) : mixed
update_staff_meta(mixed $user_id, mixed $meta_key, mixed $meta_value) : mixed
get_staff_meta(mixed $user_id[, mixed $meta_key = '' ]) : mixed
delete_staff_meta(mixed $user_id, mixed $meta_key) : mixed
add_contact_meta(mixed $user_id, mixed $meta_key[, mixed $meta_value = '' ]) : mixed
update_contact_meta(mixed $user_id, mixed $meta_key, mixed $meta_value) : mixed
get_contact_meta(mixed $user_id[, mixed $meta_key = '' ]) : mixed
delete_contact_meta(mixed $user_id, mixed $meta_key) : mixed
add_customer_meta(mixed $user_id, mixed $meta_key[, mixed $meta_value = '' ]) : mixed
update_customer_meta(mixed $user_id, mixed $meta_key, mixed $meta_value) : mixed
get_customer_meta(mixed $user_id[, mixed $meta_key = '' ]) : mixed
delete_customer_meta(mixed $user_id, mixed $meta_key) : mixed
add_meta(mixed $for, mixed $user_id, mixed $meta_key[, mixed $meta_value = '' ]) : mixed
update_meta(mixed $for, mixed $user_id, mixed $meta_key, mixed $meta_value) : mixed
meta_key_exists(mixed $for, mixed $user_id, mixed $meta_key) : mixed
delete_meta(mixed $for, mixed $user_id, mixed $meta_key) : mixed
get_meta(mixed $for, mixed $user_id[, mixed $meta_key = '' ]) : mixed
_get_meta_key_query_column_for(mixed $for) : mixed

# widgets_helper.php
get_dashboard_widgets() : array<string|int, mixed>
render_dashboard_widgets(string $container) : mixed
create_widget_id([string|null $id = null ]) : string