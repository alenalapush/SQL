select count(distinct u.id) as cnt_users
from users u
join coderun c
on u.id = c.user_id
left join codesubmit csm
on u.id = csm.user_id
where csm.user_id is null;
