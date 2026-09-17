select count(distinct u.id) as cnt_users
from users u
join codesubmit csm
on u.id = csm.user_id
join coderun c
on u.id = c.user_id;
