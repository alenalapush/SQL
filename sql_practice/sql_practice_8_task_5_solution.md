select u.username,
    count(*) as submission_count
from users u
join codesubmit c
on u.id = c.user_id
where to_char(u.date_joined, 'YYYY') = '2021'
group by u.username
having count(*) > 200
order by username;