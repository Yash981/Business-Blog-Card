# Business-Blog-Card
(echo "use repositories"; echo "db.repo_data.aggregate([ { \$match: { topics: '3d' } }, { \$group: { _id: null, maxStars: { \$max: '\$stars' } } } ]).forEach(function(doc) { var owner = db.repo_data.findOne({ stars: doc.maxStars }).owner; print('max_rating: { owner: \"' + owner + '\", stars: ' + doc.maxStars + ' }'); });") | mongo > max_stars.txt
