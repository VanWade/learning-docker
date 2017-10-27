#### mount an overlay fs
* prepare
mkdir dir1 dir2 dir3 work
mkdir dir1/fruit
mkdir dir2/fruit
mkdir dir2/dairy
echo apple1 > dir1/fruit/apple
echo grape1 > dir1/fruit/grape
echo spoon1 > dir1/spoon
echo apple2 > dir2/fruit/apple
echo milk > dir2/dairy/milk
echo spoon2 > dir2/spoon
* mount
mount -t overlay -o lowerdir=./dir1,upperdir=./dir2,workdir=./work overlay ./dir3
