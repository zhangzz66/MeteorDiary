{{SELECT * FROM blocks WHERE (id in (select parent_id from blocks where content like '%.action{.title}%' and type !='l' ) and type='i') or (id in (select parent_id from blocks where content like '%.action{.title}%' ) and type='h') and root_id !='.action{.id}' order by created DESC}}