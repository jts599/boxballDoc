# Boxball Schemas
This document contains the schemas for the boxball database.

Columns with a &#128273; next to the name represent the primary keys of the table, and will always be listed first in a given table.
## retrosheet
<details>
 <summary> <b>code_event</b></summary>

  #### &#128273; code: smallint
  #### description: varchar(30)
</details><br>
<details>
 <summary> <b>code_field_park</b></summary>

  #### &#128273; code: smallint
  #### description: varchar(30)
</details><br>
<details>
 <summary> <b>code_method_record</b></summary>

  #### &#128273; code: smallint
  #### description: varchar(30)
</details><br>
<details>
 <summary> <b>code_pitches_record</b></summary>

  #### &#128273; code: smallint
  #### description: varchar(30)
</details><br>
<details>
 <summary> <b>code_precip_park</b></summary>

  #### &#128273; code: smallint
  #### description: varchar(30)
</details><br>
<details>
 <summary> <b>code_sky_park</b></summary>

  #### &#128273; code: smallint
  #### description: varchar(30)
</details><br>
<details>
 <summary> <b>code_wind_direction_park</b></summary>

  #### &#128273; code: smallint
  #### description: varchar(30)
</details><br>
<details>
 <summary> <b>comment</b></summary>

  #### &#128273; dummy_id: integer
  #### game_id: char(12)
   >Game ID (home team ID + YYYYMMDD + doubleheader flag
  #### event_id: smallint
   >Commented event number
  #### comment: varchar(1638)
   >Comment text
  #### ejected_person_id: varchar(256)
   >ID of ejected person
  #### ejected_person_role_cd: varchar(256)
  #### eject_umpire_id: varchar(256)
   >ID of umpire who ejected person
  #### eject_reason: varchar(1639)
  #### umpchange_inning: varchar(256)
  #### umpchange_position: varchar(256)
  #### umpchange_person_id: varchar(256)
   >ID of new umpire
</details><br>
<details>
 <summary> <b>daily</b></summary>

  #### &#128273; dummy_id: integer
  #### game_id: char(12)
   >Game ID (home team ID + YYYYMMDD + doubleheader flag
  #### game_dt: date
   >Game date
  #### game_ct: smallint
   >Doubleheader flag (0 - only game of day, 1 - first game of doubleheader, 2 - second game of doubleheader
  #### appearance_dt: date
   >Player appearance date. Can be different from game date if the game was suspended and the player entered the game at the later date
  #### team_id: char(3)
   >Team ID of player
  #### player_id: char(8)
   >Player ID
  #### slot_ct: smallint
   >Player lineup position
  #### seq_ct: smallint
   >Player is nth person of game to play in that lineup slot
  #### home_fl: boolean
   >Player is playing at home
  #### opponent_id: char(3)
   >Team opponent ID
  #### park_id: char(5)
   >Park ID
  #### b_g: smallint
   >Games played
  #### b_pa: smallint
   >Plate appearances
  #### b_ab: smallint
   >At bats
  #### b_r: smallint
   >Runs scored
  #### b_h: smallint
   >Hits
  #### b_tb: smallint
   >Total bases
  #### b_2b: smallint
   >Doubles
  #### b_3b: smallint
   >Triples
  #### b_hr: smallint
   >Home runs
  #### b_hr4: smallint
   >Grand slams
  #### b_rbi: smallint
   >Runs batted in
  #### b_gw: smallint
   >Game winning RBI
  #### b_bb: smallint
   >Walks
  #### b_ibb: smallint
   >Intentional walks
  #### b_so: smallint
   >Strikeouts
  #### b_gdp: smallint
   >Grounded into double plays
  #### b_hp: smallint
   >Hit by pitches
  #### b_sh: smallint
   >Sacrifice hits
  #### b_sf: smallint
   >Sacrifice files
  #### b_sb: smallint
   >Stolen bases
  #### b_cs: smallint
   >Caught stealing
  #### b_xi: smallint
   >Reached on interference
  #### b_g_dh: smallint
   >Games as DH
  #### b_g_ph: smallint
   >Games as pinch hitter
  #### b_g_pr: smallint
   >Games as pinch runner
  #### p_g: smallint
   >Games pitched
  #### p_gs: smallint
   >Games as starting pitcher
  #### p_cg: smallint
   >Complete games
  #### p_sho: smallint
   >Shutouts
  #### p_gf: smallint
   >Games finished
  #### p_w: smallint
   >Wins
  #### p_l: smallint
   >Losses
  #### p_sv: smallint
   >Saves
  #### p_out: smallint
   >Outs recorded
  #### p_tbf: smallint
   >Total batters faced
  #### p_ab: smallint
   >At bats against
  #### p_r: smallint
   >Runs allowed
  #### p_er: smallint
   >Earned runs allowed
  #### p_h: smallint
   >Hits allowed
  #### p_tb: smallint
   >Total bases allowed
  #### p_2b: smallint
   >Doubles allowed
  #### p_3b: smallint
   >Triples allowed
  #### p_hr: smallint
   >Home runs allowed
  #### p_hr4: smallint
   >Grand slams allowed
  #### p_bb: smallint
   >Walks allowed
  #### p_ibb: smallint
   >Intentional walks allowed
  #### p_so: smallint
   >Strikeouts against
  #### p_gdp: smallint
   >Grounded into double plays against
  #### p_hp: smallint
   >Hit by pitches allowed
  #### p_sh: smallint
   >Sacrifice hits allowed
  #### p_sf: smallint
   >Sacrifice flies allowed
  #### p_xi: smallint
   >Reached on interference allowed
  #### p_wp: smallint
   >Wild pitches allowed
  #### p_bk: smallint
   >Balks allowed
  #### p_ir: smallint
   >Inherited runners
  #### p_irs: smallint
   >Inherited runners scored
  #### p_go: smallint
   >Groundouts recorded
  #### p_ao: smallint
   >Fly ball outs recorded
  #### p_pitch: smallint
   >Pitches thrown
  #### p_strike: smallint
   >Strikes thrown
  #### f_p_g: smallint
   >Appearances at pitcher
  #### f_p_gs: smallint
   >Starts at pitcher
  #### f_p_out: smallint
   >Outs played as pitcher
  #### f_p_tc: smallint
   >Total chances as pitcher
  #### f_p_po: smallint
   >Putouts as pitcher
  #### f_p_a: smallint
   >Assists as pitcher
  #### f_p_e: smallint
   >Errors as pitcher
  #### f_p_dp: smallint
   >Double plays turned as pitcher
  #### f_p_tp: smallint
   >Triple pays turned as pitcher
  #### f_c_g: smallint
   >Appearances at catcher
  #### f_c_gs: smallint
   >Starts at catcher
  #### f_c_out: smallint
   >Outs played as catcher
  #### f_c_tc: smallint
   >Total chances as catcher
  #### f_c_po: smallint
   >Putouts as catcher
  #### f_c_a: smallint
   >Assists as catcher
  #### f_c_e: smallint
   >Errors as catcher
  #### f_c_dp: smallint
   >Double plays turned as catcher
  #### f_c_tp: smallint
   >Triple pays turned as catcher
  #### f_c_pb: smallint
   >Passed balls
  #### f_c_xi: smallint
   >Catcher's interference
  #### f_1b_g: smallint
   >Appearances at first baseman
  #### f_1b_gs: smallint
   >Starts at first baseman
  #### f_1b_out: smallint
   >Outs played as first baseman
  #### f_1b_tc: smallint
   >Total chances as first baseman
  #### f_1b_po: smallint
   >Putouts as first baseman
  #### f_1b_a: smallint
   >Assists as first baseman
  #### f_1b_e: smallint
   >Errors as first baseman
  #### f_1b_dp: smallint
   >Double plays turned as first baseman
  #### f_1b_tp: smallint
   >Triple pays turned as first baseman
  #### f_2b_g: smallint
   >Appearances at second baseman
  #### f_2b_gs: smallint
   >Starts at second baseman
  #### f_2b_out: smallint
   >Outs played as second baseman
  #### f_2b_tc: smallint
   >Total chances as second baseman
  #### f_2b_po: smallint
   >Putouts as second baseman
  #### f_2b_a: smallint
   >Assists as second baseman
  #### f_2b_e: smallint
   >Errors as second baseman
  #### f_2b_dp: smallint
   >Double plays turned as second baseman
  #### f_2b_tp: smallint
   >Triple pays turned as second baseman
  #### f_3b_g: smallint
   >Appearances at third baseman
  #### f_3b_gs: smallint
   >Starts at third baseman
  #### f_3b_out: smallint
   >Outs played as third baseman
  #### f_3b_tc: smallint
   >Total chances as third baseman
  #### f_3b_po: smallint
   >Putouts as third baseman
  #### f_3b_a: smallint
   >Assists as third baseman
  #### f_3b_e: smallint
   >Errors as third baseman
  #### f_3b_dp: smallint
   >Double plays turned as third baseman
  #### f_3b_tp: smallint
   >Triple pays turned as third baseman
  #### f_ss_g: smallint
   >Appearances at shortstop
  #### f_ss_gs: smallint
   >Starts at shortstop
  #### f_ss_out: smallint
   >Outs played as shortstop
  #### f_ss_tc: smallint
   >Total chances as shortstop
  #### f_ss_po: smallint
   >Putouts as shortstop
  #### f_ss_a: smallint
   >Assists as shortstop
  #### f_ss_e: smallint
   >Errors as shortstop
  #### f_ss_dp: smallint
   >Double plays turned as shortstop
  #### f_ss_tp: smallint
   >Triple pays turned as shortstop
  #### f_lf_g: smallint
   >Appearances at left fielder
  #### f_lf_gs: smallint
   >Starts at left fielder
  #### f_lf_out: smallint
   >Outs played as left fielder
  #### f_lf_tc: smallint
   >Total chances as left fielder
  #### f_lf_po: smallint
   >Putouts as left fielder
  #### f_lf_a: smallint
   >Assists as left fielder
  #### f_lf_e: smallint
   >Errors as left fielder
  #### f_lf_dp: smallint
   >Double plays turned as left fielder
  #### f_lf_tp: smallint
   >Triple pays turned as left fielder
  #### f_cf_g: smallint
   >Appearances at center fielder
  #### f_cf_gs: smallint
   >Starts at center fielder
  #### f_cf_out: smallint
   >Outs played as center fielder
  #### f_cf_tc: smallint
   >Total chances as center fielder
  #### f_cf_po: smallint
   >Putouts as center fielder
  #### f_cf_a: smallint
   >Assists as center fielder
  #### f_cf_e: smallint
   >Errors as center fielder
  #### f_cf_dp: smallint
   >Double plays turned as center fielder
  #### f_cf_tp: smallint
   >Triple pays turned as center fielder
  #### f_rf_g: smallint
   >Appearances at right fielder
  #### f_rf_gs: smallint
   >Starts at right fielder
  #### f_rf_out: smallint
   >Outs played as right fielder
  #### f_rf_tc: smallint
   >Total chances as right fielder
  #### f_rf_po: smallint
   >Putouts as right fielder
  #### f_rf_a: smallint
   >Assists as right fielder
  #### f_rf_e: smallint
   >Errors as right fielder
  #### f_rf_dp: smallint
   >Double plays turned as right fielder
  #### f_rf_tp: smallint
   >Triple pays turned as right fielder
</details><br>
<details>
 <summary> <b>deduced_game</b></summary>

  #### &#128273; game_id: char(12)
   >Game ID (home team ID + YYYYMMDD + doubleheader flag
</details><br>
<details>
 <summary> <b>event</b></summary>

  #### &#128273; game_id: char(12)
   >Game ID (home team ID + YYYYMMDD + doubleheader flag
  #### &#128273; event_id: integer
   >Event number of game
  #### away_team_id: char(3)
   >Visiting Team
  #### inn_ct: smallint
   >Inning
  #### bat_home_id: boolean
   >Home team is batting
  #### outs_ct: smallint
   >Outs (0-2)
  #### balls_ct: smallint
   >Balls (0-3)
  #### strikes_ct: smallint
   >Strikes (0-2
  #### pitch_seq_tx: varchar(30)
   >Pitch sequence
  #### away_score_ct: smallint
   >Away score
  #### home_score_ct: smallint
   >Home score
  #### bat_id: char(8)
   >Batter ID
  #### bat_hand_cd: char(1)
   >Batter handedness
  #### resp_bat_id: char(8)
   >ID of batter charged with event
  #### resp_bat_hand_cd: char(1)
   >Handedness of batter charged with event
  #### pit_id: char(8)
   >Pitcher ID
  #### pit_hand_cd: char(1)
   >Pitcher handedness
  #### resp_pit_id: char(8)
   >ID of pitcher charged with event
  #### resp_pit_hand_cd: char(1)
   >Handedness of pitcher charged with event
  #### pos2_fld_id: char(8)
   >Catcher ID
  #### pos3_fld_id: char(8)
   >First baseman ID
  #### pos4_fld_id: char(8)
   >Second baseman ID
  #### pos5_fld_id: char(8)
   >Third baseman ID
  #### pos6_fld_id: char(8)
   >Shortstop ID
  #### pos7_fld_id: char(8)
   >Left fielder ID
  #### pos8_fld_id: char(8)
   >Center fielder ID
  #### pos9_fld_id: char(8)
   >Right fielder ID
  #### base1_run_id: char(8)
   >ID of runner on first
  #### base2_run_id: char(8)
   >ID of runner on second
  #### base3_run_id: char(8)
   >ID of runner on third
  #### event_tx: varchar(128)
   >Event text (in scoring shorthand
  #### leadoff_fl: boolean
   >Batter is leading off the inning
  #### ph_fl: boolean
   >Batter is pinch-hitting
  #### bat_fld_cd: smallint
   >Defensive position of batter (10 for DH, 11 for PH, 12 for PR
  #### bat_lineup_id: smallint
   >Lineup position (1-9)
  #### event_cd: smallint
   >Event code (join table `code_event` for descriptions
  #### bat_event_fl: boolean
   >Event is related to the batter
  #### ab_fl: boolean
   >Event is an at-bat
  #### h_fl: smallint
   >Event is a hit
  #### sh_fl: boolean
   >Event is a sacrifice hit
  #### sf_fl: boolean
   >Event is a sacrifice fly
  #### event_outs_ct: smallint
   >Outs recorded on event (0-3)
  #### dp_fl: boolean
   >Event is a double play
  #### tp_fl: boolean
   >Event is a triple play
  #### rbi_ct: smallint
   >Runs batted in on event
  #### wp_fl: boolean
   >Event is a wild pitch
  #### pb_fl: boolean
   >Event is a passed ball
  #### fld_cd: smallint
   >Position id of event fielder
  #### battedball_cd: char(1)
   >Batted ball code (P - pop-up, G - ground ball, F - fly ball, L - line drive
  #### bunt_fl: boolean
   >Event is a bunt
  #### foul_fl: boolean
   >Event is a foul ball
  #### battedball_loc_tx: varchar(5)
   >Hit location code (see https://www.retrosheet.org/location.htm)
  #### err_ct: smallint
   >Number of errors recorded during event
  #### err1_fld_cd: smallint
   >Position code of fielder committing first error during event
  #### err1_cd: char(1)
   >First error type (T - throwing, F - fielding)
  #### err2_fld_cd: smallint
   >Position code of fielder committing second error during event
  #### err2_cd: char(1)
   >Second error type (T - throwing, F - fielding)
  #### err3_fld_cd: smallint
   >Position code of fielder committing third error during event
  #### err3_cd: char(1)
   >Third error type (T - throwing, F - fielding)
  #### bat_dest_id: smallint
   >Destination of batter after event (0 - putout, 1-3 - bases, 4 - scored asearned run, 5 - scored as unearned, 6 - scored as unearned to team earned to pitcher)
  #### run1_dest_id: smallint
   >Destination of runner on first after event (0 - putout, 1-3 - bases, 4 - scored as earned run, 5 - scored as unearned, 6 - scored as unearned to team earned to pitcher)
  #### run2_dest_id: smallint
   >Destination of runner on second after event (0 - putout, 1-3 - bases, 4 - scored as earned run, 5 - scored as unearned, 6 - scored as unearned to team earned to pitcher)
  #### run3_dest_id: smallint
   >Destination of runner on third after event (0 - putout, 1-3 - bases, 4 - scored as earned run, 5 - scored as unearned, 6 - scored as unearned to team earned to pitcher)
  #### bat_play_tx: varchar(15)
   >Fielding play on batter
  #### run1_play_tx: varchar(15)
   >Fielding play on runner on first
  #### run2_play_tx: varchar(15)
   >Fielding play on runner on second
  #### run3_play_tx: varchar(15)
   >Fielding play on runner on third
  #### run1_sb_fl: boolean
   >Runner on first steals base
  #### run2_sb_fl: boolean
   >Runner on second steals base
  #### run3_sb_fl: boolean
   >Runner on third steals base
  #### run1_cs_fl: boolean
   >Runner on first caught stealing
  #### run2_cs_fl: boolean
   >Runner on second caught stealing
  #### run3_cs_fl: boolean
   >Runner on third caught stealing
  #### run1_pk_fl: boolean
   >Runner on first picked off
  #### run2_pk_fl: boolean
   >Runner on second picked off
  #### run3_pk_fl: boolean
   >Runner on third picked off
  #### run1_resp_pit_id: char(8)
   >ID of pitcher charged with runner on first
  #### run2_resp_pit_id: char(8)
   >ID of pitcher charged with runner on second
  #### run3_resp_pit_id: char(8)
   >ID of pitcher charged with runner on third
  #### game_new_fl: boolean
   >Start of game flag
  #### game_end_fl: boolean
   >End of game flag
  #### pr_run1_fl: boolean
   >Pinch-runner on first
  #### pr_run2_fl: boolean
   >Pinch-runner on second
  #### pr_run3_fl: boolean
   >Runner on third
  #### removed_for_pr_run1_id: char(8)
   >ID of former runner on first removed for pinch-runner
  #### removed_for_pr_run2_id: char(8)
   >ID of former runner on second removed for pinch-runner
  #### removed_for_pr_run3_id: char(8)
   >ID of former runner on third removed for pinch-runner
  #### removed_for_ph_bat_id: char(8)
   >ID of former batter removed for pinch-hitter
  #### removed_for_ph_bat_fld_cd: integer
   >Position code of batter removed for pinch-hitter
  #### po1_fld_cd: smallint
   >Position code of fielder with first putout
  #### po2_fld_cd: smallint
   >Position code of fielder with second putout
  #### po3_fld_cd: smallint
   >Position code of fielder with third putout
  #### ass1_fld_cd: smallint
   >Position code of fielder with first assist
  #### ass2_fld_cd: smallint
   >Position code of fielder with second assist
  #### ass3_fld_cd: smallint
   >Position code of fielder with third assist
  #### ass4_fld_cd: smallint
   >Position code of fielder with fourth assist
  #### ass5_fld_cd: smallint
   >Position code of fielder with fifth assist
  #### home_team_id: char(3)
   >Home team ID
  #### bat_team_id: char(3)
   >Batting team ID
  #### fld_team_id: char(3)
   >Fielding team ID
  #### bat_last_id: smallint
   >Half inning (differs from batting team if home team bats first)
  #### inn_new_fl: boolean
   >Start of half-inning flag
  #### inn_end_fl: boolean
   >End of half-inning flag
  #### start_bat_score_ct: smallint
   >Runs scored by batting team (prior to this event)
  #### start_fld_score_ct: smallint
   >Runs scored by fielding team
  #### inn_runs_ct: smallint
   >Runs scored in this half-inning (prior to this event)
  #### game_pa_ct: smallint
   >Batting team PA total (prior to this event)
  #### inn_pa_ct: smallint
   >Half-inning PA total (prior to this event)
  #### pa_new_fl: boolean
   >Event is the start of a plate appearance
  #### pa_trunc_fl: boolean
   >Event is a truncated plate appearance
  #### start_bases_cd: smallint
   >Base state at start of event (0-7, binary value is flags for runners on third, second, and first left-to-right)
  #### end_bases_cd: smallint
   >Base state end of event (0-7, binary value is flags for runners on third, second, and first left-to-right)
  #### bat_start_fl: boolean
   >Batter started game
  #### resp_bat_start_fl: boolean
   >Result-charged batter is a starter
  #### bat_on_deck_id: char(8)
   >ID of batter on deck
  #### bat_in_hold_id: char(8)
   >Id of batter in the hole
  #### pit_start_fl: boolean
   >Pitcher started game
  #### resp_pit_start_fl: boolean
   >Result-charged pitcher started game
  #### run1_fld_cd: smallint
   >Defensive position code of runner on first
  #### run1_lineup_cd: smallint
   >Lineup position of runner on first
  #### run1_origin_event_id: smallint
   >Event number on which runner on first reached base
  #### run2_fld_cd: smallint
   >Defensive position code of runner on second
  #### run2_lineup_cd: smallint
   >Lineup position of runner on second
  #### run2_origin_event_id: smallint
   >Event number on which runner on second reached base
  #### run3_fld_cd: smallint
   >Defensive position code of runner on third
  #### run3_lineup_cd: smallint
   >Lineup position of runner on third
  #### run3_origin_event_id: smallint
   >Event number on which runner on third reached base
  #### run1_resp_cat_id: char(8)
   >ID of responsible catcher for runner on first
  #### run2_resp_cat_id: char(8)
   >ID of responsible catcher for runner on second
  #### run3_resp_cat_id: char(8)
   >ID of responsible catcher for runner on third
  #### pa_ball_ct: smallint
   >Number of balls in plate appearance
  #### pa_called_ball_ct: smallint
   >Number of called balls in plate appearance
  #### pa_intent_ball_ct: smallint
   >Number of intentional balls in plate appearance
  #### pa_pitchout_ball_ct: smallint
   >Number of pitchouts in plate appearance
  #### pa_hitbatter_ball_ct: smallint
   >Number of pitches hitting batter in plate appearance
  #### pa_other_ball_ct: smallint
   >Number of other balls in plate appearance
  #### pa_strike_ct: smallint
   >Number of strikes in plate appearance
  #### pa_called_strike_ct: smallint
   >Number of called strikes in plate appearance
  #### pa_swingmiss_strike_ct: smallint
   >Number of swing-and-miss strikes in plate appearance
  #### pa_foul_strike_ct: smallint
   >Number of foul balls in plate appearance
  #### pa_inplay_strike_ct: smallint
   >Number of balls in play in plate appearance
  #### pa_other_strike_ct: smallint
   >Number of other strikes in plate appearance
  #### event_runs_ct: smallint
   >Number of runs on play
  #### fld_id: char(8)
   >ID of player fielding batted ball
  #### base2_force_fl: boolean
   >Event has force play at second
  #### base3_force_fl: boolean
   >Event has force play at third
  #### base4_force_fl: boolean
   >Event has force play at home
  #### bat_safe_err_fl: boolean
   >Event has batter safe on an error
  #### bat_fate_id: smallint
   >Ultimate fate of batter (see `dest_id` cols for code meaning
  #### run1_fate_id: smallint
   >Ultimate fate of runner on first (see `dest_id` cols for code meaning
  #### run2_fate_id: smallint
   >Ultimate fate of runner on second (see `dest_id` cols for code meaning
  #### run3_fate_id: smallint
   >Ultimate fate of runner on third (see `dest_id` cols for code meaning
  #### fate_runs_ct: smallint
   >Additional runs scored in half inning after this event
  #### ass6_fld_cd: smallint
   >Position code of fielder with sixth assist
  #### ass7_fld_cd: smallint
   >Position code of fielder with seventh assist
  #### ass8_fld_cd: smallint
   >Position code of fielder with eighth assist
  #### ass9_fld_cd: smallint
   >Position code of fielder with ninth assist
  #### ass10_fld_cd: smallint
   >Position code of fielder with tenth assist
  #### unknown_out_exc_fl: boolean
   >Unknown fielding credit flag
  #### uncertain_play_exc_fl: boolean
   >Uncertain play flag
</details><br>
<details>
 <summary> <b>game</b></summary>

  #### &#128273; game_id: char(12)
   >Game ID (home team ID + YYYYMMDD + doubleheader flag
  #### game_dt: date
   >Game date
  #### game_ct: smallint
   >Doubleheader flag (0 - only game of day, 1 - first game of doubleheader, 2 - second game of doubleheader
  #### game_dy: varchar(9)
   >Day of week
  #### start_game_tm: smallint
   >Game start time (12HMM coded as integer, eg 1015 for 10:15 PM)
  #### dh_fl: varchar(1)
   >DH used
  #### daynight_park_cd: varchar(1)
   >D - day game, N - night game
  #### away_team_id: char(3)
   >Away team ID
  #### home_team_id: char(3)
   >Home team ID
  #### park_id: varchar(5)
   >Park ID
  #### away_start_pit_id: char(8)
   >Away team starting pitcher ID
  #### home_start_pit_id: char(8)
   >Home team starting pitcher ID
  #### base4_ump_id: varchar(32)
   >Home plate umpire ID
  #### base1_ump_id: varchar(32)
   >First base umpire ID
  #### base2_ump_id: varchar(32)
   >Second base umpire ID
  #### base3_ump_id: varchar(32)
   >Third base umpire ID
  #### lf_ump_id: char(8)
   >Left field umpire ID
  #### rf_ump_id: char(8)
   >Right field umpire ID
  #### attend_park_ct: integer
   >Attendance
  #### scorer_record_id: varchar(50)
   >Scorekeeper
  #### translator_record_id: varchar(50)
   >Translator
  #### inputter_record_id: varchar(50)
   >Inputter
  #### input_record_ts: varchar(20)
   >Date and time of record input
  #### edit_record_ts: varchar(20)
   >Date and time of Most recent record edit
  #### method_record_cd: varchar(1)
   >How the game was scored (join `code_method_record` for details
  #### pitches_record_cd: varchar(1)
   >Highest detail of pitches recorded (join `code_pitches_record` for details). Note that many games with pitch detail do not have that info for all events, so pitch totals may not be accurate.
  #### temp_park_ct: smallint
   >Park temperature in degrees F (0 if unknown)
  #### wind_direction_park_cd: smallint
   >Wind direction park code (join `code_wind_direction_park` for details)
  #### wind_speed_park_ct: smallint
   >Wind speed in miles per hour (-1 if unknown)
  #### field_park_cd: smallint
   >Park field condition code (join `code_field_park` for details)
  #### precip_park_cd: smallint
   >Park precipitation code (join `code_precip_park` for details
  #### sky_park_cd: smallint
   >Park sky condition code (join `code_sky_park` for details
  #### minutes_game_ct: smallint
   >Length of game in minutes
  #### inn_ct: smallint
   >Length of game in innings
  #### away_score_ct: smallint
   >Away team final score
  #### home_score_ct: smallint
   >Home team final score
  #### away_hits_ct: smallint
   >Away team hits
  #### home_hits_ct: smallint
   >Home team hits
  #### away_err_ct: smallint
   >Away team errors
  #### home_err_ct: smallint
   >Home team errors
  #### away_lob_ct: smallint
   >Away team left on base
  #### home_lob_ct: smallint
   >Home team left on base
  #### win_pit_id: char(8)
   >ID of winning pitcher
  #### lose_pit_id: char(8)
   >ID of losing pitcher
  #### save_pit_id: char(8)
   >ID of saving pitcher
  #### gwrbi_bat_id: char(8)
   >ID of batter wit game-winning RBI
  #### away_lineup1_bat_id: char(8)
   >ID of away team starting batter in lineup position 1
  #### away_lineup1_fld_cd: smallint
   >Fielding position code of away team starting batter in lineup position 1
  #### away_lineup2_bat_id: char(8)
   >ID of away team starting batter in lineup position 2
  #### away_lineup2_fld_cd: smallint
   >Fielding position code of away team starting batter in lineup position 2
  #### away_lineup3_bat_id: char(8)
   >ID of away team starting batter in lineup position 3
  #### away_lineup3_fld_cd: smallint
   >Fielding position code of away team starting batter in lineup position 3
  #### away_lineup4_bat_id: char(8)
   >ID of away team starting batter in lineup position 4
  #### away_lineup4_fld_cd: smallint
   >Fielding position code of away team starting batter in lineup position 4
  #### away_lineup5_bat_id: char(8)
   >ID of away team starting batter in lineup position 5
  #### away_lineup5_fld_cd: smallint
   >Fielding position code of away team starting batter in lineup position 5
  #### away_lineup6_bat_id: char(8)
   >ID of away team starting batter in lineup position 6
  #### away_lineup6_fld_cd: smallint
   >Fielding position code of away team starting batter in lineup position 6
  #### away_lineup7_bat_id: char(8)
   >ID of away team starting batter in lineup position 7
  #### away_lineup7_fld_cd: smallint
   >Fielding position code of away team starting batter in lineup position 7
  #### away_lineup8_bat_id: char(8)
   >ID of away team starting batter in lineup position 8
  #### away_lineup8_fld_cd: smallint
   >Fielding position code of away team starting batter in lineup position 8
  #### away_lineup9_bat_id: char(8)
   >ID of away team starting batter in lineup position 9
  #### away_lineup9_fld_cd: smallint
   >Fielding position code of away team starting batter in lineup position 9
  #### home_lineup1_bat_id: char(8)
   >ID of home team starting batter in lineup position 1
  #### home_lineup1_fld_cd: smallint
   >Fielding position code of home team starting batter in lineup position 1
  #### home_lineup2_bat_id: char(8)
   >ID of home team starting batter in lineup position 2
  #### home_lineup2_fld_cd: smallint
   >Fielding position code of home team starting batter in lineup position 2
  #### home_lineup3_bat_id: char(8)
   >ID of home team starting batter in lineup position 3
  #### home_lineup3_fld_cd: smallint
   >Fielding position code of home team starting batter in lineup position 3
  #### home_lineup4_bat_id: char(8)
   >ID of home team starting batter in lineup position 4
  #### home_lineup4_fld_cd: smallint
   >Fielding position code of home team starting batter in lineup position 4
  #### home_lineup5_bat_id: char(8)
   >ID of home team starting batter in lineup position 5
  #### home_lineup5_fld_cd: smallint
   >Fielding position code of home team starting batter in lineup position 5
  #### home_lineup6_bat_id: char(8)
   >ID of home team starting batter in lineup position 6
  #### home_lineup6_fld_cd: smallint
   >Fielding position code of home team starting batter in lineup position 6
  #### home_lineup7_bat_id: char(8)
   >ID of home team starting batter in lineup position 7
  #### home_lineup7_fld_cd: smallint
   >Fielding position code of home team starting batter in lineup position 7
  #### home_lineup8_bat_id: char(8)
   >ID of home team starting batter in lineup position 8
  #### home_lineup8_fld_cd: smallint
   >Fielding position code of home team starting batter in lineup position 8
  #### home_lineup9_bat_id: char(8)
   >ID of home team starting batter in lineup position 9
  #### home_lineup9_fld_cd: smallint
   >Fielding position code of home team starting batter in lineup position 9
  #### away_finish_pit_id: char(8)
   >Away team finishing pitcher
  #### home_finish_pit_id: char(8)
   >Home team finishing pitcher
  #### away_team_league_id: char(1)
   >Away team league (1 char ID)
  #### home_team_league_id: char(1)
   >Home team league (1 char ID)
  #### away_team_game_ct: smallint
   >Away team game number
  #### home_team_game_ct: smallint
   >Home team game number
  #### outs_ct: smallint
   >Length of game in outs
  #### completion_tx: varchar(26)
   >Information on completion of game
  #### forfeit_tx: varchar(26)
   >Information on forfeit of game
  #### protest_tx: varchar(26)
   >Information on protest of game
  #### away_line_tx: varchar(26)
   >Away team linescore
  #### home_line_tx: varchar(26)
   >Home team linescore
  #### away_ab_ct: smallint
   >Away team at bats
  #### away_2b_ct: smallint
   >Away team doubles
  #### away_3b_ct: smallint
   >Away team triples
  #### away_hr_ct: smallint
   >Away team home runs
  #### away_bi_ct: smallint
   >Away team runs batted in
  #### away_sh_ct: smallint
   >Away team sacrifice hits
  #### away_sf_ct: smallint
   >Away team sacrifice flies
  #### away_hp_ct: smallint
   >Away team hit by pitches
  #### away_bb_ct: smallint
   >Away team walks
  #### away_ibb_ct: smallint
   >Away team intentional walks
  #### away_so_ct: smallint
   >Away team strikeouts
  #### away_sb_ct: smallint
   >Away team stolen bases
  #### away_cs_ct: smallint
   >Away team caught stealing
  #### away_gdp_ct: smallint
   >Away team grounded into double plays
  #### away_xi_ct: smallint
   >Away team reached on interference
  #### away_pitcher_ct: smallint
   >Away team number of pitchers used
  #### away_er_ct: smallint
   >Away team individual earned runs
  #### away_ter_ct: smallint
   >Away team team earned runs
  #### away_wp_ct: smallint
   >Away team wild pitches
  #### away_bk_ct: smallint
   >Away team balks
  #### away_po_ct: smallint
   >Away team putouts
  #### away_a_ct: smallint
   >Away team assists
  #### away_pb_ct: smallint
   >Away team passed balls
  #### away_dp_ct: smallint
   >Away team double plays turned
  #### away_tp_ct: smallint
   >Away team triple plays turned
  #### home_ab_ct: smallint
   >Home team at bats
  #### home_2b_ct: smallint
   >Home team doubles
  #### home_3b_ct: smallint
   >Home team triples
  #### home_hr_ct: smallint
   >Home team home runs
  #### home_bi_ct: smallint
   >Home team runs batted in
  #### home_sh_ct: smallint
   >Home team sacrifice hits
  #### home_sf_ct: smallint
   >Home team sacrifice flies
  #### home_hp_ct: smallint
   >Home team hit by pitches
  #### home_bb_ct: smallint
   >Home team walks
  #### home_ibb_ct: smallint
   >Home team intentional walks
  #### home_so_ct: smallint
   >Home team strikeouts
  #### home_sb_ct: smallint
   >Home team stolen bases
  #### home_cs_ct: smallint
   >Home team caught stealing
  #### home_gdp_ct: smallint
   >Home team grounded into double plays
  #### home_xi_ct: smallint
   >Home team reached on interference
  #### home_pitcher_ct: smallint
   >Home team number of pitchers used
  #### home_er_ct: smallint
   >Home team individual earned runs
  #### home_ter_ct: smallint
   >Home team team earned runs
  #### home_wp_ct: smallint
   >Home team wild pitches
  #### home_bk_ct: smallint
   >Home team balks
  #### home_po_ct: smallint
   >Home team putouts
  #### home_a_ct: smallint
   >Home team assists
  #### home_pb_ct: smallint
   >Home team passed balls
  #### home_dp_ct: smallint
   >Home team double plays turned
  #### home_tp_ct: smallint
   >Home team triple plays turned
  #### ump_home_name_tx: varchar(26)
   >Home plate umpire name
  #### ump_1b_name_tx: varchar(26)
   >First base umpire name
  #### ump_2b_name_tx: varchar(26)
   >Second base umpire name
  #### ump_3b_name_tx: varchar(26)
   >Third base umpire name
  #### ump_lf_name_tx: varchar(26)
   >Left field umpire name
  #### ump_rf_name_tx: varchar(26)
   >Right field umpire name
  #### away_manager_id: char(8)
   >Away manager ID
  #### away_manager_name_tx: varchar(26)
   >Away manager name
  #### home_manager_id: char(8)
   >Home manager ID
  #### home_manager_name_tx: varchar(26)
   >Home manager name
  #### win_pit_name_tx: varchar(26)
   >Wining pitcher name
  #### lose_pit_name_tx: varchar(26)
   >Losing pitcher name
  #### save_pit_name_tx: varchar(26)
   >Saving pitcher name
  #### goahead_rbi_id: char(8)
   >ID of batter with goahead RBI
  #### goahead_rbi_name_tx: varchar(26)
   >Name of batter with goahead RBI
  #### away_lineup1_bat_name_tx: varchar(26)
   >Name of away team batter in lineup position 1
  #### away_lineup2_bat_name_tx: varchar(26)
   >Name of away team batter in lineup position 2
  #### away_lineup3_bat_name_tx: varchar(26)
   >Name of away team batter in lineup position 3
  #### away_lineup4_bat_name_tx: varchar(26)
   >Name of away team batter in lineup position 4
  #### away_lineup5_bat_name_tx: varchar(26)
   >Name of away team batter in lineup position 5
  #### away_lineup6_bat_name_tx: varchar(26)
   >Name of away team batter in lineup position 6
  #### away_lineup7_bat_name_tx: varchar(26)
   >Name of away team batter in lineup position 7
  #### away_lineup8_bat_name_tx: varchar(26)
   >Name of away team batter in lineup position 8
  #### away_lineup9_bat_name_tx: varchar(26)
   >Name of home team batter in lineup position 9
  #### home_lineup1_bat_name_tx: varchar(26)
   >Name of home team batter in lineup position 1
  #### home_lineup2_bat_name_tx: varchar(26)
   >Name of home team batter in lineup position 2
  #### home_lineup3_bat_name_tx: varchar(26)
   >Name of home team batter in lineup position 3
  #### home_lineup4_bat_name_tx: varchar(26)
   >Name of home team batter in lineup position 4
  #### home_lineup5_bat_name_tx: varchar(26)
   >Name of home team batter in lineup position 5
  #### home_lineup6_bat_name_tx: varchar(26)
   >Name of home team batter in lineup position 6
  #### home_lineup7_bat_name_tx: varchar(26)
   >Name of home team batter in lineup position 7
  #### home_lineup8_bat_name_tx: varchar(26)
   >Name of home team batter in lineup position 8
  #### home_lineup9_bat_name_tx: varchar(26)
   >Name of home team batter in lineup position 9
  #### add_info_tx: varchar(26)
   >Additional information
  #### acq_info_tx: varchar(26)
   >Acquisition information
</details><br>
<details>
 <summary> <b>gamelog</b></summary>

  #### &#128273; date: date
   >Game date
  #### &#128273; double_header: char(1)
   >
        Number of game:
         "0" -- a single game
         "1" -- the first game of a double (or triple) header
                including separate admission doubleheaders
         "2" -- the second game of a double (or triple) header
                including separate admission doubleheaders
         "3" -- the third game of a triple-header
         "A" -- the first game of a double-header involving 3 teams
         "B" -- the second game of a double-header involving 3 teams
         
  #### &#128273; visiting_team: char(3)
   >Visiting team ID
  #### &#128273; home_team: char(3)
   >Home team ID
  #### day_of_week: char(3)
   >Day of week (3 char abbreviation)
  #### visiting_team_league: char(2)
   >Away team league ID
  #### visiting_team_game_number: smallint
   >Away team game number
  #### home_team_league: char(2)
   >Home team league ID
  #### home_team_game_number: smallint
   >Home team game number
  #### visitor_runs_scored: smallint
   >Away team runs scored
  #### home_runs_score: smallint
   >Home team runs scored
  #### length_in_outs: smallint
   >Game length in outs
  #### day_night: char(1)
   >D - day game, N - night game
  #### completion_info: varchar(23)
   >
        Completion information.  If the game was completed at a
        later date (either due to a suspension or an upheld protest)
        this field will include:
            "yyyymmdd,park,vs,hs,len" Where
        yyyymmdd -- the date the game was completed
        park -- the park ID where the game was completed
        vs -- the visitor score at the time of interruption
        hs -- the home score at the time of interruption
        len -- the length of the game in outs at time of interruption
        All the rest of the information in the record refers to the
        entire game.
        
  #### forfeit_info: varchar(3)
   >V - forfeited to away team, H - forfeited to home team, T - ruled a no-decision
  #### protest_info: varchar(3)
   >P - protested by unidentified team, V - disallowed protest by away team, H - disallowed protest by home team, X - upheld protest by away team, Y - upheld protest by home team
  #### park_id: char(5)
   >Park ID
  #### attendance: integer
   >Attendance
  #### duration: smallint
   >Time of game in minutes
  #### vistor_line_score: varchar(26)
   >Away team line score, e.g. 010000(10)0x
  #### home_line_score: varchar(26)
   >Home team line score, e.g. 010000(10)0x
  #### visitor_ab: smallint
   >Away team at bats
  #### visitor_h: smallint
   >Away team hits
  #### visitor_d: smallint
   >Away team doubles
  #### visitor_t: smallint
   >Away team triples
  #### visitor_hr: smallint
   >Away team home runs
  #### visitor_rbi: smallint
   >Away team runs batted in
  #### visitor_sh: smallint
   >Away team sacrifice hits (may include sac flies before 1954)
  #### visitor_sf: smallint
   >Away team sacrifice flies (since 1954)
  #### visitor_hbp: smallint
   >Away team hit by pitches
  #### visitor_bb: smallint
   >Away team walks
  #### visitor_ibb: smallint
   >Away team intentional walks
  #### visitor_k: smallint
   >Away team strikeouts
  #### visitor_sb: smallint
   >Away team stolen bases
  #### visitor_cs: smallint
   >Away team caught stealing
  #### visitor_gdp: smallint
   >Away team grounded into double plays
  #### visitor_ci: smallint
   >Away team reached on interference
  #### visitor_lob: smallint
   >Away team left on base
  #### visitor_pitchers: smallint
   >Away team pitchers used
  #### visitor_er: smallint
   >Away team individual earned runs allowed
  #### visitor_ter: smallint
   >Away team team earned runs allowed
  #### visitor_wp: smallint
   >Away team wild pitches allowed
  #### visitor_balks: smallint
   >Away team balks allowed
  #### visitor_po: smallint
   >Away team putouts
  #### visitor_a: smallint
   >Away team assists
  #### visitor_e: smallint
   >Away team errors
  #### visitor_passed: smallint
   >Away team passed balls
  #### visitor_db: smallint
   >Away team double plays turned
  #### visitor_tp: smallint
   >Away team triple plays turned
  #### home_ab: smallint
   >Home team at bats
  #### home_h: smallint
   >Home team hits
  #### home_d: smallint
   >Home team doubles
  #### home_t: smallint
   >Home team triples
  #### home_hr: smallint
   >Home team home runs
  #### home_rbi: smallint
   >Home team runs batted in
  #### home_sh: smallint
   >Home team sacrifice hits (may include sac flies before 1954)
  #### home_sf: smallint
   >Home team sacrifice flies (since 1954)
  #### home_hbp: smallint
   >Home team hit by pitches
  #### home_bb: smallint
   >Home team walks
  #### home_ibb: smallint
   >Home team intentional walks
  #### home_k: smallint
   >Home team strikeouts
  #### home_sb: smallint
   >Home team stolen bases
  #### home_cs: smallint
   >Home team caught stealing
  #### home_gdp: smallint
   >Home team grounded into double plays
  #### home_ci: smallint
   >Home team reached on interference
  #### home_lob: smallint
   >Home team left on base
  #### home_pitchers: smallint
   >Home team pitchers used
  #### home_er: smallint
   >Home team individual earned runs allowed
  #### home_ter: smallint
   >Home team team earned runs allowed
  #### home_wp: smallint
   >Home team wild pitches allowed
  #### home_balks: smallint
   >Home team balks allowed
  #### home_po: smallint
   >Home team putouts
  #### home_a: smallint
   >Home team assists
  #### home_e: smallint
   >Home team errors
  #### home_passed: smallint
   >Home team passed balls
  #### home_db: smallint
   >Home team double plays turned
  #### home_tp: smallint
   >Home team triple plays turned
  #### umpire_h_id: char(8)
   >Home plate umpire ID
  #### umpire_h_name: varchar(32)
   >Home plate umpire name
  #### umpire_1b_id: char(8)
   >First base umpire ID
  #### umpire_1b_name: varchar(32)
   >First base umpire name
  #### umpire_2b_id: char(8)
   >Second base umpire ID
  #### umpire_2b_name: varchar(32)
   >Second base umpire name
  #### umpire_3b_id: char(8)
   >Third base umpire ID
  #### umpire_3b_name: varchar(32)
   >Third base umpire name
  #### umpire_lf_id: char(8)
   >Left field umpire ID
  #### umpire_lf_name: varchar(32)
   >Left field umpire name
  #### umpire_rf_id: char(8)
   >Right field umpire ID
  #### umpire_rf_name: varchar(32)
   >Right field umpire name
  #### visitor_manager_id: char(8)
   >Away team manager ID
  #### visitor_manager_name: varchar(32)
   >Away team manager name
  #### home_manager_id: char(8)
   >Home team manager ID
  #### home_manager_name: varchar(32)
   >Home team manager name
  #### winning_pitcher_id: char(8)
   >Winning pitcher ID
  #### winning_pitcher_name: varchar(32)
   >Winning pitcher name
  #### losing_pitcher_id: char(8)
   >Losing pitcher ID
  #### losing_pitcher_name: varchar(32)
   >Losing pitcher name
  #### saving_pitcher_id: char(8)
   >Saving pitcher ID
  #### saving_pitcher_name: varchar(32)
   >Saving pitcher name
  #### game_winning_rbi_id: char(8)
   >Game-winning RBI ID
  #### game_winning_rbi_name: varchar(32)
   >Game-winning RBI name
  #### visitor_starting_pitcher_id: char(8)
   >Away team starting pitcher ID
  #### visitor_starting_pitcher_name: varchar(32)
   >Away team starting pitcher name
  #### home_starting_pitcher_id: char(8)
   >Home team starting pitcher ID
  #### home_starting_pitcher_name: varchar(32)
   >Home team starting pitcher name
  #### visitor_batting_1_player_id: char(8)
   >Away team lineup slot 1 starting player ID
  #### visitor_batting_1_name: varchar(32)
   >Away team lineup slot 1 starting player name
  #### visitor_batting_1_position: smallint
   >Away team lineup slot 1 starting player fielding position
  #### visitor_batting_2_player_id: char(8)
   >Away team lineup slot 2 starting player ID
  #### visitor_batting_2_name: varchar(32)
   >Away team lineup slot 2 starting player name
  #### visitor_batting_2_position: smallint
   >Away team lineup slot 2 starting player fielding position
  #### visitor_batting_3_player_id: char(8)
   >Away team lineup slot 3 starting player ID
  #### visitor_batting_3_name: varchar(32)
   >Away team lineup slot 3 starting player name
  #### visitor_batting_3_position: smallint
   >Away team lineup slot 3 starting player fielding position
  #### visitor_batting_4_player_id: char(8)
   >Away team lineup slot 4 starting player ID
  #### visitor_batting_4_name: varchar(32)
   >Away team lineup slot 4 starting player name
  #### visitor_batting_4_position: smallint
   >Away team lineup slot 4 starting player fielding position
  #### visitor_batting_5_player_id: char(8)
   >Away team lineup slot 5 starting player ID
  #### visitor_batting_5_name: varchar(32)
   >Away team lineup slot 5 starting player name
  #### visitor_batting_5_position: smallint
   >Away team lineup slot 5 starting player fielding position
  #### visitor_batting_6_player_id: char(8)
   >Away team lineup slot 6 starting player ID
  #### visitor_batting_6_name: varchar(32)
   >Away team lineup slot 6 starting player name
  #### visitor_batting_6_position: smallint
   >Away team lineup slot 6 starting player fielding position
  #### visitor_batting_7_player_id: char(8)
   >Away team lineup slot 7 starting player ID
  #### visitor_batting_7_name: varchar(32)
   >Away team lineup slot 7 starting player name
  #### visitor_batting_7_position: smallint
   >Away team lineup slot 7 starting player fielding position
  #### visitor_batting_8_player_id: char(8)
   >Away team lineup slot 8 starting player ID
  #### visitor_batting_8_name: varchar(32)
   >Away team lineup slot 8 starting player name
  #### visitor_batting_8_position: smallint
   >Away team lineup slot 8 starting player fielding position
  #### visitor_batting_9_player_id: char(8)
   >Away team lineup slot 9 starting player ID
  #### visitor_batting_9_name: varchar(32)
   >Away team lineup slot 9 starting player name
  #### visitor_batting_9_position: smallint
   >Away team lineup slot 9 starting player fielding position
  #### home_batting_1_player_id: char(8)
   >Home team lineup slot 1 starting player ID
  #### home_batting_1_name: varchar(32)
   >Home team lineup slot 1 starting player name
  #### home_batting_1_position: smallint
   >Home team lineup slot 1 starting player fielding position
  #### home_batting_2_player_id: char(8)
   >Home team lineup slot 2 starting player ID
  #### home_batting_2_name: varchar(32)
   >Home team lineup slot 2 starting player name
  #### home_batting_2_position: smallint
   >Home team lineup slot 2 starting player fielding position
  #### home_batting_3_player_id: char(8)
   >Home team lineup slot 3 starting player ID
  #### home_batting_3_name: varchar(32)
   >Home team lineup slot 3 starting player name
  #### home_batting_3_position: smallint
   >Home team lineup slot 3 starting player fielding position
  #### home_batting_4_player_id: char(8)
   >Home team lineup slot 4 starting player ID
  #### home_batting_4_name: varchar(32)
   >Home team lineup slot 4 starting player name
  #### home_batting_4_position: smallint
   >Home team lineup slot 4 starting player fielding position
  #### home_batting_5_player_id: char(8)
   >Home team lineup slot 5 starting player ID
  #### home_batting_5_name: varchar(32)
   >Home team lineup slot 5 starting player name
  #### home_batting_5_position: smallint
   >Home team lineup slot 5 starting player fielding position
  #### home_batting_6_player_id: char(8)
   >Home team lineup slot 6 starting player ID
  #### home_batting_6_name: varchar(32)
   >Home team lineup slot 6 starting player name
  #### home_batting_6_position: smallint
   >Home team lineup slot 6 starting player fielding position
  #### home_batting_7_player_id: char(8)
   >Home team lineup slot 7 starting player ID
  #### home_batting_7_name: varchar(32)
   >Home team lineup slot 7 starting player name
  #### home_batting_7_position: smallint
   >Home team lineup slot 7 starting player fielding position
  #### home_batting_8_player_id: char(8)
   >Home team lineup slot 8 starting player ID
  #### home_batting_8_name: varchar(32)
   >Home team lineup slot 8 starting player name
  #### home_batting_8_position: smallint
   >Home team lineup slot 8 starting player fielding position
  #### home_batting_9_player_id: char(8)
   >Home team lineup slot 9 starting player ID
  #### home_batting_9_name: varchar(32)
   >Home team lineup slot 9 starting player name
  #### home_batting_9_position: smallint
   >Home team lineup slot 9 starting player fielding position
  #### additional_info: varchar(128)
   >
        Additional information.  This is a grab-bag of informational
              items that might not warrant a field on their own.  The field
              is alpha-numeric. Some items are represented by tokens such as:
                 "HTBF" -- home team batted first.
                 Note: if "HTBF" is specified it would be possible to see
                 something like "01002000x" in the visitor's line score.
              Changes in umpire positions during a game will also appear in
              this field.  These will be in the form:
                 umpchange,inning,umpPosition,umpid with the latter three
                 repeated for each umpire.
              These changes occur with umpire injuries, late arrival of
              umpires or changes from completion of suspended games. Details
              of suspended games are in field `completion_information`.
        
  #### acquisition_info: char(1)
   >Y - complete game information, N - no game information, D - game derived from box score and game story, P - portions of game information
</details><br>
<details>
 <summary> <b>park</b></summary>

  #### &#128273; park_id: char(5)
   >Park ID
  #### name: varchar(41)
   >Park name
  #### aka: varchar(55)
   >Common park alias
  #### city: varchar(17)
   >City
  #### state: varchar(9)
   >State
  #### start_date: varchar(10)
   >First game
  #### end_date: varchar(10)
   >Last game
  #### league: char(2)
   >League ID
  #### notes: varchar(54)
   >Misc. notes
</details><br>
<details>
 <summary> <b>roster</b></summary>

  #### &#128273; year: integer
   >Year of roster
  #### &#128273; player_id: char(8)
   >Player ID
  #### &#128273; team_id: char(3)
   >Team ID
  #### &#128273; position: varchar(2)
   >Primary fielding position
  #### last_name: varchar(32)
   >Player last name
  #### first_name: varchar(32)
   >Player first name
  #### bats: char(1)
   >Bat handedness
  #### throws: char(1)
   >Throw handedness
</details><br>
<details>
 <summary> <b>schedule</b></summary>

  #### &#128273; date: date
   >Scheduled game date
  #### &#128273; home_team: char(3)
   >Home team ID
  #### &#128273; home_team_game_number: integer
   >Home team game number
  #### double_header: smallint
   >Doubleheader flag (0 - only game of day, 1 - first game of doubleheader, 2 - second game of doubleheader
  #### day_of_week: char(3)
   >Day of week (3 letter abbreviation
  #### visiting_team: char(3)
   >Away team ID
  #### visiting_team_league: char(2)
   >Away team league ID
  #### visiting_team_game_number: smallint
   >Away team game number
  #### home_team_league: char(2)
   >Home team league ID
  #### day_night: char(1)
   >D - day, N - night
  #### postponement_indicator: varchar(120)
   >
        This field will contain one or more phrases related to the game if it was
        not played as scheduled. If there is more than one phrase, they are separated
        by a semi-colon (";"). There are three possible outcomes for games not played
        on the originally scheduled date:
        -- The game was played on another date
        -- The game was played on the original date but at another site
        -- The game was not played
        
  #### makeup_dates: varchar(120)
   >
        This field will contain a makeup date if the postponed game was played at
        another time or place. If an attempt was known to have been made on a date but
        postponed again, that date will be listed. In that case, there will be a second
        date for the date when the game was actually played, in this form: "20150428;
        20150528" For the note about a team folding, the team code is one of the
        standard Retrosheet team IDs. The same is true for the team played as note.
        Often, the two of these are combined in one field.
        
</details><br>
<details>
 <summary> <b>sub</b></summary>

  #### &#128273; dummy_id: integer
  #### game_id: char(12)
   >Game ID (home team ID + YYYYMMDD + doubleheader flag
  #### inn_ct: smallint
   >Inning of substitution
  #### bat_home_id: smallint
   >Is home team batting (-1 for N/A)
  #### sub_id: char(8)
   >Player ID of substitute
  #### sub_home_id: boolean
   >Is the home team making the substitution
  #### sub_lineup_id: smallint
   >Lineup position of substitution
  #### sub_fld_cd: smallint
   >Fielding position of substitution
  #### removed_id: char(8)
   >ID of removed player
  #### removed_fld_cd: smallint
   >Fielding position of removed player
  #### event_id: smallint
   >Event number in which substitution occurred
</details><br>


## baseballdatabank
<details>
 <summary> <b>allstar_full</b></summary>

  #### &#128273; dummy_id: integer
  #### player_id: varchar(9)
  #### year_id: smallint
  #### game_num: smallint
  #### game_id: varchar(12)
  #### team_id: varchar(3)
  #### lg_id: varchar(2)
  #### gp: smallint
  #### starting_pos: smallint
</details><br>
<details>
 <summary> <b>appearances</b></summary>

  #### &#128273; year_id: smallint
  #### &#128273; team_id: varchar(3)
  #### &#128273; player_id: varchar(9)
  #### lg_id: varchar(2)
  #### g_all: smallint
  #### gs: smallint
  #### g_batting: smallint
  #### g_defense: smallint
  #### g_p: smallint
  #### g_c: smallint
  #### g_1b: smallint
  #### g_2b: smallint
  #### g_3b: smallint
  #### g_ss: smallint
  #### g_lf: smallint
  #### g_cf: smallint
  #### g_rf: smallint
  #### g_of: smallint
  #### g_dh: smallint
  #### g_ph: smallint
  #### g_pr: smallint
</details><br>
<details>
 <summary> <b>awards_managers</b></summary>

  #### &#128273; dummy_id: integer
  #### player_id: varchar(10)
  #### award_id: varchar(75)
  #### year_id: smallint
  #### lg_id: varchar(2)
  #### tie: varchar(1)
  #### notes: varchar(100)
</details><br>
<details>
 <summary> <b>awards_players</b></summary>

  #### &#128273; dummy_id: integer
  #### player_id: varchar(9)
  #### award_id: varchar(255)
  #### year_id: smallint
  #### lg_id: varchar(2)
  #### tie: varchar(1)
  #### notes: varchar(100)
</details><br>
<details>
 <summary> <b>awards_share_managers</b></summary>

  #### &#128273; award_id: varchar(25)
  #### &#128273; year_id: integer
  #### &#128273; player_id: varchar(10)
  #### lg_id: varchar(2)
  #### points_won: integer
  #### points_max: integer
  #### votes_first: integer
</details><br>
<details>
 <summary> <b>awards_share_players</b></summary>

  #### &#128273; award_id: varchar(25)
  #### &#128273; year_id: smallint
  #### &#128273; player_id: varchar(9)
  #### lg_id: varchar(2)
  #### points_won: float
  #### points_max: integer
  #### votes_first: float
</details><br>
<details>
 <summary> <b>batting</b></summary>

  #### &#128273; player_id: varchar(9)
  #### &#128273; year_id: smallint
  #### &#128273; stint: smallint
  #### team_id: varchar(3)
  #### lg_id: varchar(2)
  #### g: smallint
  #### ab: smallint
  #### r: smallint
  #### h: smallint
  #### _2b: smallint
  #### _3b: smallint
  #### hr: smallint
  #### rbi: smallint
  #### sb: smallint
  #### cs: smallint
  #### bb: smallint
  #### so: smallint
  #### ibb: smallint
  #### hbp: smallint
  #### sh: smallint
  #### sf: smallint
  #### gidp: smallint
</details><br>
<details>
 <summary> <b>batting_post</b></summary>

  #### &#128273; year_id: smallint
  #### &#128273; round: varchar(10)
  #### &#128273; player_id: varchar(9)
  #### team_id: varchar(3)
  #### lg_id: varchar(2)
  #### g: smallint
  #### ab: smallint
  #### r: smallint
  #### h: smallint
  #### _2b: smallint
  #### _3b: smallint
  #### hr: smallint
  #### rbi: smallint
  #### sb: smallint
  #### cs: smallint
  #### bb: smallint
  #### so: smallint
  #### ibb: smallint
  #### hbp: smallint
  #### sh: smallint
  #### sf: smallint
  #### gidp: smallint
</details><br>
<details>
 <summary> <b>college_playing</b></summary>

  #### &#128273; player_id: varchar(9)
  #### &#128273; school_id: varchar(15)
  #### &#128273; year_id: smallint
</details><br>
<details>
 <summary> <b>fielding</b></summary>

  #### &#128273; player_id: varchar(9)
  #### &#128273; year_id: smallint
  #### &#128273; stint: smallint
  #### &#128273; pos: varchar(2)
  #### team_id: varchar(3)
  #### lg_id: varchar(2)
  #### g: smallint
  #### gs: smallint
  #### inn_outs: smallint
  #### po: smallint
  #### a: smallint
  #### e: smallint
  #### dp: smallint
  #### pb: smallint
  #### wp: smallint
  #### sb: smallint
  #### cs: smallint
  #### zr: float
</details><br>
<details>
 <summary> <b>fielding_of</b></summary>

  #### &#128273; player_id: varchar(9)
  #### &#128273; year_id: smallint
  #### &#128273; stint: smallint
  #### g_lf: smallint
  #### g_cf: smallint
  #### g_rf: smallint
</details><br>
<details>
 <summary> <b>fielding_of_split</b></summary>

  #### &#128273; player_id: varchar(9)
  #### &#128273; year_id: smallint
  #### &#128273; stint: smallint
  #### &#128273; pos: varchar(2)
  #### team_id: varchar(3)
  #### lg_id: varchar(2)
  #### g: smallint
  #### gs: smallint
  #### inn_outs: smallint
  #### po: smallint
  #### a: smallint
  #### e: smallint
  #### dp: smallint
  #### pb: smallint
  #### wp: smallint
  #### sb: smallint
  #### cs: smallint
  #### zr: float
</details><br>
<details>
 <summary> <b>fielding_post</b></summary>

  #### &#128273; player_id: varchar(9)
  #### &#128273; year_id: smallint
  #### &#128273; round: varchar(10)
  #### &#128273; pos: varchar(2)
  #### team_id: varchar(3)
  #### lg_id: varchar(2)
  #### g: smallint
  #### gs: smallint
  #### inn_outs: smallint
  #### po: smallint
  #### a: smallint
  #### e: smallint
  #### dp: smallint
  #### tp: smallint
  #### pb: smallint
  #### sb: smallint
  #### cs: smallint
</details><br>
<details>
 <summary> <b>hall_of_fame</b></summary>

  #### &#128273; player_id: varchar(10)
  #### &#128273; year_id: smallint
  #### &#128273; voted_by: varchar(64)
  #### ballots: varchar(64)
  #### needed: varchar(64)
  #### votes: varchar(64)
  #### inducted: varchar(1)
  #### category: varchar(20)
  #### needed_note: varchar(25)
</details><br>
<details>
 <summary> <b>home_games</b></summary>

  #### &#128273; year_id: smallint
  #### &#128273; lg_id: varchar(2)
  #### &#128273; team_id: varchar(3)
  #### &#128273; park_id: varchar(5)
  #### first_game: date
  #### last_game: date
  #### games: smallint
  #### openings: smallint
  #### attendance: integer
</details><br>
<details>
 <summary> <b>managers</b></summary>

  #### &#128273; year_id: smallint
  #### &#128273; team_id: varchar(3)
  #### &#128273; inseason: smallint
  #### player_id: varchar(10)
  #### lg_id: varchar(2)
  #### g: smallint
  #### w: smallint
  #### l: smallint
  #### rank: smallint
  #### plyr_mgr: varchar(1)
</details><br>
<details>
 <summary> <b>managers_half</b></summary>

  #### &#128273; player_id: varchar(10)
  #### &#128273; year_id: smallint
  #### &#128273; team_id: varchar(3)
  #### &#128273; half: smallint
  #### lg_id: varchar(2)
  #### inseason: smallint
  #### g: smallint
  #### w: smallint
  #### l: smallint
  #### rank: smallint
</details><br>
<details>
 <summary> <b>parks</b></summary>

  #### &#128273; park_id: varchar(5)
  #### park_name: varchar(40)
  #### park_alias: varchar(55)
  #### city: varchar(25)
  #### state: varchar(16)
  #### country: varchar(2)
</details><br>
<details>
 <summary> <b>people</b></summary>

  #### &#128273; player_id: varchar(10)
  #### birth_year: smallint
  #### birth_month: smallint
  #### birth_day: smallint
  #### birth_country: varchar(50)
  #### birth_state: varchar(50)
  #### birth_city: varchar(50)
  #### death_year: smallint
  #### death_month: smallint
  #### death_day: smallint
  #### death_country: varchar(50)
  #### death_state: varchar(50)
  #### death_city: varchar(50)
  #### name_first: varchar(50)
  #### name_last: varchar(50)
  #### name_given: varchar(255)
  #### weight: smallint
  #### height: float
  #### bats: varchar(1)
  #### throws: varchar(1)
  #### debut: date
  #### final_game: date
  #### retro_id: varchar(9)
  #### bbref_id: varchar(9)
</details><br>
<details>
 <summary> <b>pitching</b></summary>

  #### &#128273; player_id: varchar(9)
  #### &#128273; year_id: smallint
  #### &#128273; stint: smallint
  #### team_id: varchar(3)
  #### lg_id: varchar(2)
  #### w: smallint
  #### l: smallint
  #### g: smallint
  #### gs: smallint
  #### cg: smallint
  #### sho: smallint
  #### sv: smallint
  #### ip_outs: smallint
  #### h: smallint
  #### er: smallint
  #### hr: smallint
  #### bb: smallint
  #### so: smallint
  #### ba_opp: float
  #### era: float
  #### ibb: smallint
  #### wp: smallint
  #### hbp: smallint
  #### bk: smallint
  #### bfp: smallint
  #### gf: smallint
  #### r: smallint
  #### sh: smallint
  #### sf: smallint
  #### gidp: smallint
</details><br>
<details>
 <summary> <b>pitching_post</b></summary>

  #### &#128273; player_id: varchar(9)
  #### &#128273; year_id: smallint
  #### &#128273; round: varchar(10)
  #### team_id: varchar(3)
  #### lg_id: varchar(2)
  #### w: smallint
  #### l: smallint
  #### g: smallint
  #### gs: smallint
  #### cg: smallint
  #### sho: smallint
  #### sv: smallint
  #### ip_outs: smallint
  #### h: smallint
  #### er: smallint
  #### hr: smallint
  #### bb: smallint
  #### so: smallint
  #### ba_opp: float
  #### era: float
  #### ibb: smallint
  #### wp: smallint
  #### hbp: smallint
  #### bk: smallint
  #### bfp: smallint
  #### gf: smallint
  #### r: smallint
  #### sh: smallint
  #### sf: smallint
  #### gidp: smallint
</details><br>
<details>
 <summary> <b>salaries</b></summary>

  #### &#128273; year_id: smallint
  #### &#128273; team_id: varchar(3)
  #### &#128273; lg_id: varchar(2)
  #### &#128273; player_id: varchar(9)
  #### salary: float
</details><br>
<details>
 <summary> <b>schools</b></summary>

  #### &#128273; school_id: varchar(15)
  #### name_full: varchar(255)
  #### city: varchar(55)
  #### state: varchar(55)
  #### country: varchar(55)
</details><br>
<details>
 <summary> <b>series_post</b></summary>

  #### &#128273; year_id: smallint
  #### &#128273; round: varchar(5)
  #### team_id_winner: varchar(3)
  #### lg_id_winner: varchar(2)
  #### team_id_loser: varchar(3)
  #### lg_id_loser: varchar(2)
  #### wins: smallint
  #### losses: smallint
  #### ties: smallint
</details><br>
<details>
 <summary> <b>teams</b></summary>

  #### &#128273; year_id: smallint
  #### &#128273; lg_id: varchar(2)
  #### &#128273; team_id: varchar(3)
  #### franch_id: varchar(3)
  #### div_id: varchar(1)
  #### rank: integer
  #### g: integer
  #### g_home: integer
  #### w: integer
  #### l: integer
  #### div_win: varchar(1)
  #### wc_win: varchar(1)
  #### lg_win: varchar(1)
  #### ws_win: varchar(1)
  #### r: integer
  #### ab: integer
  #### h: integer
  #### _2b: integer
  #### _3b: integer
  #### hr: integer
  #### bb: integer
  #### so: integer
  #### sb: integer
  #### cs: integer
  #### hbp: integer
  #### sf: integer
  #### ra: integer
  #### er: integer
  #### era: float
  #### cg: integer
  #### sho: integer
  #### sv: integer
  #### ip_outs: integer
  #### h_a: integer
  #### hr_a: integer
  #### bb_a: integer
  #### so_a: integer
  #### e: integer
  #### dp: integer
  #### fp: float
  #### name: varchar(50)
  #### park: varchar(255)
  #### attendance: integer
  #### bpf: integer
  #### ppf: integer
  #### team_id_br: varchar(3)
  #### team_id_lahman45: varchar(3)
  #### team_id_retro: varchar(3)
</details><br>
<details>
 <summary> <b>teams_franchises</b></summary>

  #### &#128273; franch_id: varchar(3)
  #### franch_name: varchar(50)
  #### active: varchar(2)
  #### na_assoc: varchar(3)
</details><br>
<details>
 <summary> <b>teams_half</b></summary>

  #### &#128273; year_id: integer
  #### &#128273; lg_id: varchar(2)
  #### &#128273; team_id: varchar(3)
  #### &#128273; half: varchar(1)
  #### div_id: varchar(1)
  #### div_win: varchar(1)
  #### rank: integer
  #### g: integer
  #### w: integer
  #### l: integer
</details><br>