#
# Linux Makefile for GCC for Jedi Academy SDK
#


# === Variables ===

# Compiler - GCC
CC = gcc

# Compiler Flags
# -D<name> ( Used to make a define like #define mydefine )
# -w ( disable warnings )
# -I<include path>  used to include headers
# -fPIC ( this flag is necessary to build shared libraries )
CFLAGS = -I../qcommon -I../server -I../icarus -I../ghoul2 -fPIC -DFINAL_BUILD -DMISSION_PACK -DQAGAME -D_JK2 -D__linux__ -D__GCC__ -w

# Target file
TARGET = ../../baseAAA/jampgamei386.so

# Object Files
OFILES = 	ai_main.o ai_util.o ai_wpnav.o AnimalNPC.o bg_lib.o bg_g2_utils.o bg_misc.o bg_panimate.o \
		bg_pmove.o bg_saber.o bg_saberLoad.o bg_saga.o bg_slidemove.o bg_vehicleLoad.o bg_weapons.o \
		FighterNPC.o g_active.o g_arenas.o g_bot.o g_client.o g_cmds.o g_combat.o g_exphysics.o \
		g_ICARUScb.o g_items.o g_log.o g_main.o g_mem.o g_misc.o g_missile.o g_mover.o g_nav.o g_navnew.o \
		g_object.o g_saga.o g_session.o g_spawn.o g_strap.o g_svcmds.o g_target.o g_team.o g_timer.o g_trigger.o \
		g_turret.o g_turret_G2.o g_utils.o g_vehicles.o g_vehicleTurret.o g_weapon.o NPC.o NPC_AI_Atst.o \
		NPC_AI_Default.o NPC_AI_Droid.o NPC_AI_GalakMech.o NPC_AI_Grenadier.o NPC_AI_Howler.o NPC_AI_ImperialProbe.o \
		NPC_AI_Interrogator.o NPC_AI_Jedi.o NPC_AI_Mark1.o NPC_AI_Mark2.o NPC_AI_MineMonster.o NPC_AI_Rancor.o \
		NPC_AI_Remote.o NPC_AI_Seeker.o NPC_AI_Sentry.o NPC_AI_Sniper.o NPC_AI_Stormtrooper.o NPC_AI_Utils.o \
		NPC_AI_Wampa.o NPC_behavior.o NPC_combat.o NPC_goal.o NPC_misc.o NPC_move.o NPC_reactions.o NPC_senses.o \
		NPC_sounds.o NPC_spawn.o NPC_stats.o NPC_utils.o q_math.o q_shared.o SpeederNPC.o tri_coll_test.o \
		WalkerNPC.o w_force.o w_saber.o g_syscalls.o



# === Arguments for the Makefile ===
#  typing just "make" invokes the first target ( which in this case is $(TARGET) )

$(TARGET): 	$(OFILES)
		$(CC) -shared -o $(TARGET) $(OFILES) -lm
.c.o:
	$(CC) $(CFLAGS) -c $*.c -o $*.o

# "make clean"
clean:
	rm -f $(OFILES)
	rm -f $(TARGET)
