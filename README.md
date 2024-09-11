# README

This is part of the Forms Project in The Odin Project’s Ruby on Rails Curriculum. Find it at https://www.theodinproject.com

<form action="/users" method="post" accept-charset="UTF-8">
    <input type="hidden" name="authenticity_token" value="<%= form_authenticity_token %>"/>
    <div class="">
        <label for="username">Enter Username: </label>
        <input type="text" name="user[username]" id="username" required />
    </div>
    <div class="">
        <label for="password">Enter Password: </label>
        <input type="password" name="user[password]" id="password" required />
    </div>
    <div class="">
        <label for="email">Enter your email: </label>
        <input type="email" name="user[email]" id="email" required />
    </div>
    <div class="">
        <input type="submit" value="Create" />
    </div>
</form>

<%= form_tag(users_path, :method => "post") do %>
<div>
<%= label_tag(:username, "username: ")%>
<%= text_field_tag "user[username]"%>
</div>
<div>
<%= label_tag(:password, "password: ")%>
<%= password_field_tag "user[password]" %>
</div>
<div>
<%= label_tag(:email, "email: ")%>
<%= email_field_tag "user[email]" %>
</div>
<div>
<%= submit_tag "Create"%>
</div>
<%end%>
