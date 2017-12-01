# Map/Reduce - Advanced Join

# Map/Reduce - Advanced Join
[make_join2data.py]and [make_data_join2.txt] can be used to make the 6 input files used for this exercise. The join2_gennum*.txt files contain tv show names and viewer counts (show, viewer_count) and the join2_genchan*.txt files contain tv show names and the channel on which the show airs (show, channel). The objective is to return the number of viewers for shows on ABC.

   - The mapper emits (show, viewer_count) as the (key, value) for join2_gennum.txt files and emits (show, channel) as the (key, value) for join2_genchan.txt files when the channel is ABC.
   - The reducer receives the shuffled (key, value) pairs, aggregates the viewer_count values for all the same keys, and emits (show, viewer_total) for shows that have a (key, value) pair with ABC as the value.

Running [join2_mapper.py] on the join2_gennum.txt and join2_genchan.txt files results in the [total_viewer_counts_output.txt]
