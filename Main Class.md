package me.massonrage66.plugin;

import org.bukkit.Bukkit;
import org.bukkit.ChatColor;
import org.bukkit.Material;
import org.bukkit.command.Command;
import org.bukkit.command.CommandSender;
import org.bukkit.enchantments.Enchantment;
import org.bukkit.entity.Player;
import org.bukkit.inventory.ItemStack;
import org.bukkit.inventory.meta.ItemMeta;
import org.bukkit.plugin.java.JavaPlugin;
 
public class youtube extends JavaPlugin {
 
        public void onEnable() {
                Bukkit.getServer().getLogger().info("Test Plugin Enabled!");
        }
       
        public void onDisable() {
                Bukkit.getServer().getLogger().info("Test Plugin Disabled!");
        }
       
        public boolean onCommand(CommandSender sender, Command cmd, String commandLabel, String[] args) {
               
                if (!(sender instanceof Player)) {
                        sender.sendMessage(ChatColor.AQUA + "The console ran the test command! Good job!");
                        return true;
                }
               
                Player player = (Player) sender;
                if (cmd.getName().equalsIgnoreCase("Cody")) {
                	player.sendMessage(ChatColor.RED + "OY! YOU WANNA 1v1 ME MATE!");
                	
                }
                if (cmd.getName().equalsIgnoreCase("GitGud")) {
                	ItemStack paper = new ItemStack(Material.PAPER, 1);
                	paper.addEnchantment(Enchantment.KNOCKBACK, 2);
                	ItemMeta papermeta = paper.getItemMeta();
                	papermeta.setDisplayName(ChatColor.GREEN + "Skills");
                }
                if (cmd.getName().equalsIgnoreCase("Monkey")) {
                	player.sendMessage(ChatColor.AQUA + "Reviewing");
                	player.sendMessage(ChatColor.AQUA + "25% Complete");
                	ItemStack mhead = new ItemStack(Material.LEATHER_HELMET, 1);
                	player.sendMessage(ChatColor.AQUA + "50% Complete");
                	ItemStack mchest = new ItemStack(Material.LEATHER_CHESTPLATE, 1);
                	player.sendMessage(ChatColor.AQUA + "65% Complete");
                	ItemStack mlegs = new ItemStack(Material.LEATHER_LEGGINGS, 1);
                	player.sendMessage(ChatColor.AQUA + "85% Complete");
                	ItemStack mboot = new ItemStack(Material.LEATHER_BOOTS, 1);
                	player.sendMessage(ChatColor.AQUA + "95% Complete");
                	ItemStack stick = new ItemStack(Material.STICK, 1);
                	player.sendMessage(ChatColor.AQUA + "100% Complete");
                	stick.addEnchantment(Enchantment.KNOCKBACK, 100);
                	mhead.addEnchantment(Enchantment.PROTECTION_ENVIRONMENTAL, 2);
                	mchest.addEnchantment(Enchantment.PROTECTION_ENVIRONMENTAL, 2);
                	mlegs.addEnchantment(Enchantment.PROTECTION_ENVIRONMENTAL, 2);
                	mboot.addEnchantment(Enchantment.PROTECTION_ENVIRONMENTAL, 2);
                	ItemMeta mheadmeta = mhead.getItemMeta();
                	mheadmeta.setDisplayName(ChatColor.GOLD + "Monkey Head");
                	ItemMeta mchestmeta = mchest.getItemMeta();
                	mchestmeta.setDisplayName(ChatColor.GOLD + "Monkey Torso");
                	ItemMeta mlegsmeta = mlegs.getItemMeta();
                	mlegsmeta.setDisplayName(ChatColor.GOLD + "Monkey Legs");
                	ItemMeta mbootmeta = mboot.getItemMeta();
                	mbootmeta.setDisplayName(ChatColor.GOLD + "Monkey Feet");
                	ItemMeta stickmeta = stick.getItemMeta();
                	stickmeta.setDisplayName(ChatColor.RED + "Beating Stick");
                	player.sendMessage(ChatColor.AQUA + "Complete! Enjoy");
                	
                			
                }
                

                return true;
        }
}
