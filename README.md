//MainRegistry(StarWars)

package StarWars.main;

import net.minecraft.block.Block;
import net.minecraft.block.material.Material;
import net.minecraft.creativetab.CreativeTabs;
import net.minecraft.item.Item;
import net.minecraft.item.ItemStack;
import net.minecraft.world.WorldType;
import StarWars.Biomes.BiomeRegistry;
import StarWars.Biomes.WorldTypeIlum;
import StarWars.LightSabers.ItemProdigalSonSaber;
import StarWars.LightSabers.SaberDurability;
import StarWars.LightSabers.SaberEnums;
import StarWars.blocks.Blockilumice;
import StarWars.blocks.Blockilumsnow;
import StarWars.lib.STRINGS;
import cpw.mods.fml.common.Mod;
import cpw.mods.fml.common.Mod.EventHandler;
import cpw.mods.fml.common.Mod.Instance;
import cpw.mods.fml.common.SidedProxy;
import cpw.mods.fml.common.event.FMLInitializationEvent;
import cpw.mods.fml.common.event.FMLPostInitializationEvent;
import cpw.mods.fml.common.event.FMLPreInitializationEvent;
import cpw.mods.fml.common.registry.GameRegistry;



@Mod(modid = STRINGS.MODID, name = STRINGS.name, version = STRINGS.version)



public class StarWars {
@SidedProxy (clientSide = "StarWars.main.Client", serverSide = "StarWars.main.Common")
	
public static Common proxy;

	
@Instance("StarWars")
public static StarWars modInstance;


	//Creative Tabs
public static CreativeTabs LightSabers = new TabLightSabers(CreativeTabs.getNextID(), "LightSabers");
public static CreativeTabs JediClothes = new TabJediClothes(CreativeTabs.getNextID(), "JediClothes");
public static CreativeTabs SithClothes = new TabSithClothes(CreativeTabs.getNextID(), "SithClothes");
public static CreativeTabs SWBlocks = new TabSWBlocks(CreativeTabs.getNextID(), "SWBlocks");
	
	//Items
	

	//tools
	


	
	
	
	
	//blocks
	public static Block ilumice;
	public static Block ilumsnow;
	
	
	//lightsabers
	public static Item ProdigalSonSaber;

	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	{
	//Durabilities
		SaberDurability.ProdigalSon = 200;


	
		
			
		}
	

	
	@EventHandler
	public void preInit(FMLPreInitializationEvent event) {
		
		
		BiomeRegistry.StarWars();
		
		//proxies
				
				
				
				
				
				

				
		//LightSabers		
				
				
				
				
				
				
				
		//Item's
		ProdigalSonSaber = new ItemProdigalSonSaber(SaberEnums.ProdigalSonEnum).setUnlocalizedName("ProdigalSonSaber").setTextureName("SW:ProdigalSon").setCreativeTab(LightSabers);
		
		
		
		//tools
		
		
		
		
	
		
		
		
		//Block's
		ilumice = new Blockilumice(Material.rock).setBlockName("ilumice").setBlockTextureName("SW:ice").setCreativeTab(SWBlocks);
		ilumsnow = new Blockilumsnow(Material.rock).setBlockName("ilumsnow").setBlockTextureName("SW:snow").setCreativeTab(SWBlocks);
		
		
		
		//armor
		
		
		//Gameregistry-----------------------------------------------------------------------------------------------------------------------------
		
		//Armors
		
		
				
			
		
		
		
		//Items
		
	

		
		//tools

		
		//weapons
		
		
		
		//Blocks
		GameRegistry.registerBlock(ilumice, "ilumice");
		GameRegistry.registerBlock(ilumsnow, "ilumsnow");
		
		//LightSabers
		GameRegistry.registerItem(ProdigalSonSaber, "ProdigalSonSaber");
		
		
	
		
		
		
	
		
		
		
		
		
		//worldgen
		
		
		
		
		
		
		
		
		
		
		
		
		
	}
	@EventHandler
	public void Init(FMLInitializationEvent event){
		//Crafting-------------------------------------------------------------------------------------------------------------------------------------------
		
		//blocks
		GameRegistry.addRecipe(new ItemStack(ilumice, 3), new Object [] { "XXX", "XXX", "XXX", 'X',new ItemStack(ilumsnow)});
		
		
		//Tools
		
			
		//weapons
		
		
		
		
		
		
		
		
		//smelting--------------------------------------------------------------------------------------------------------------------------------------------
		
		//items
	
		
		//Registers
		
		
		
	
		
		
		
		
		
	}
	
	
	@EventHandler
	public void postInit(FMLPostInitializationEvent event){
		
		
		WorldType ILUM = new WorldTypeIlum(3, "Ilum");
		
	
	
	
	}

}




//ItemClass


package StarWars.LightSabers;

import java.util.List;

import cpw.mods.fml.relauncher.Side;
import cpw.mods.fml.relauncher.SideOnly;
import net.minecraft.entity.player.EntityPlayer;
import net.minecraft.item.ItemStack;
import net.minecraft.item.ItemSword;

public class ItemProdigalSonSaber extends ItemSword{

	public ItemProdigalSonSaber(ToolMaterial ProdigalSonEnum) {
		super(ProdigalSonEnum);
		this.setFull3D();
	}
	
	
	  
	  
	  public void addInformation(ItemStack par1ItemStack, EntityPlayer par2EntityPlayer, List par2List, boolean par4)
	  {
	    par2List.add("Green Crystal, Tier 2 Light Saber");
	  }

}




//Model







package StarWars.LightSabers.Models;

import net.minecraft.client.model.ModelBase;
import net.minecraft.client.model.ModelRenderer;
import net.minecraft.entity.Entity;

public class ProdigalSonModel extends ModelBase
{
  //fields
    ModelRenderer MainBody;
    ModelRenderer Pomel2;
    ModelRenderer Pomel1;
    ModelRenderer Clip;
    ModelRenderer Middle_body;
    ModelRenderer Disc1;
    ModelRenderer Disc2;
    ModelRenderer Disc3;
    ModelRenderer Disc4;
    ModelRenderer Disc5;
    ModelRenderer Disc6;
    ModelRenderer Disc7;
    ModelRenderer Disc8;
    ModelRenderer Disc9;
    ModelRenderer Emmiter_Disc;
    ModelRenderer Emmiter1;
    ModelRenderer Emmiter2;
    ModelRenderer Emmiter3;
    ModelRenderer Emmiter4;
    ModelRenderer Emmiter5;
    ModelRenderer Emmiter6;
    ModelRenderer Emmiter7;
    ModelRenderer Emmiter8;
    ModelRenderer Emmiter9;
    ModelRenderer Emmiter10;
    ModelRenderer Emmiter11;
    ModelRenderer Emmiter12;
    ModelRenderer Emmiter_Rod;
    ModelRenderer Emmiter;
    ModelRenderer BladeEmiiter;
    ModelRenderer Blade;
  
  public ProdigalSonModel()
  {
    textureWidth = 64;
    textureHeight = 32;
    
      MainBody = new ModelRenderer(this, 0, 0);
      MainBody.addBox(0F, 0F, 0F, 2, 2, 4);
      MainBody.setRotationPoint(0F, 0F, 0F);
      MainBody.setTextureSize(64, 32);
      MainBody.mirror = true;
      setRotation(MainBody, 0F, 0F, 0F);
      Pomel2 = new ModelRenderer(this, 0, 12);
      Pomel2.addBox(0.5F, 0.5F, -1F, 1, 1, 1);
      Pomel2.setRotationPoint(0F, 0F, 0F);
      Pomel2.setTextureSize(64, 32);
      Pomel2.mirror = true;
      setRotation(Pomel2, 0F, 0F, 0F);
      Pomel1 = new ModelRenderer(this, 6, 11);
      Pomel1.addBox(0F, 0F, -2F, 2, 2, 1);
      Pomel1.setRotationPoint(0F, 0F, 0F);
      Pomel1.setTextureSize(64, 32);
      Pomel1.mirror = true;
      setRotation(Pomel1, 0F, 0F, 0F);
      Clip = new ModelRenderer(this, 0, 15);
      Clip.addBox(-0.05F, 0F, -1.8F, 0, 2, 2);
      Clip.setRotationPoint(0F, 0F, 0F);
      Clip.setTextureSize(64, 32);
      Clip.mirror = true;
      setRotation(Clip, 0F, 0F, 0F);
      Middle_body = new ModelRenderer(this, 0, 21);
      Middle_body.addBox(0.5F, 0.5F, 4F, 1, 1, 3);
      Middle_body.setRotationPoint(0F, 0F, 0F);
      Middle_body.setTextureSize(64, 32);
      Middle_body.mirror = true;
      setRotation(Middle_body, 0F, 0F, 0F);
      Disc1 = new ModelRenderer(this, 0, 0);
      Disc1.addBox(0F, 0F, 4.2F, 2, 2, 0);
      Disc1.setRotationPoint(0F, 0F, 0F);
      Disc1.setTextureSize(64, 32);
      Disc1.mirror = true;
      setRotation(Disc1, 0F, 0F, 0F);
      Disc2 = new ModelRenderer(this, 0, 0);
      Disc2.addBox(0F, 0F, 4.4F, 2, 2, 0);
      Disc2.setRotationPoint(0F, 0F, 0F);
      Disc2.setTextureSize(64, 32);
      Disc2.mirror = true;
      setRotation(Disc2, 0F, 0F, 0F);
      Disc3 = new ModelRenderer(this, 0, 0);
      Disc3.addBox(0F, 0F, 4.6F, 2, 2, 0);
      Disc3.setRotationPoint(0F, 0F, 0F);
      Disc3.setTextureSize(64, 32);
      Disc3.mirror = true;
      setRotation(Disc3, 0F, 0F, 0F);
      Disc4 = new ModelRenderer(this, 0, 0);
      Disc4.addBox(0F, 0F, 4.8F, 2, 2, 0);
      Disc4.setRotationPoint(0F, 0F, 0F);
      Disc4.setTextureSize(64, 32);
      Disc4.mirror = true;
      setRotation(Disc4, 0F, 0F, 0F);
      Disc5 = new ModelRenderer(this, 0, 0);
      Disc5.addBox(0F, 0F, 5F, 2, 2, 0);
      Disc5.setRotationPoint(0F, 0F, 0F);
      Disc5.setTextureSize(64, 32);
      Disc5.mirror = true;
      setRotation(Disc5, 0F, 0F, 0F);
      Disc6 = new ModelRenderer(this, 0, 0);
      Disc6.addBox(0F, 0F, 5.2F, 2, 2, 0);
      Disc6.setRotationPoint(0F, 0F, 0F);
      Disc6.setTextureSize(64, 32);
      Disc6.mirror = true;
      setRotation(Disc6, 0F, 0F, 0F);
      Disc7 = new ModelRenderer(this, 0, 0);
      Disc7.addBox(0F, 0F, 5.4F, 2, 2, 0);
      Disc7.setRotationPoint(0F, 0F, 0F);
      Disc7.setTextureSize(64, 32);
      Disc7.mirror = true;
      setRotation(Disc7, 0F, 0F, 0F);
      Disc8 = new ModelRenderer(this, 0, 0);
      Disc8.addBox(0F, 0F, 5.6F, 2, 2, 0);
      Disc8.setRotationPoint(0F, 0F, 0F);
      Disc8.setTextureSize(64, 32);
      Disc8.mirror = true;
      setRotation(Disc8, 0F, 0F, 0F);
      Disc9 = new ModelRenderer(this, 0, 0);
      Disc9.addBox(0F, 0F, 5.8F, 2, 2, 0);
      Disc9.setRotationPoint(0F, 0F, 0F);
      Disc9.setTextureSize(64, 32);
      Disc9.mirror = true;
      setRotation(Disc9, 0F, 0F, 0F);
      Emmiter_Disc = new ModelRenderer(this, 0, 0);
      Emmiter_Disc.addBox(0F, 0F, 7F, 2, 2, 0);
      Emmiter_Disc.setRotationPoint(0F, 0F, 0F);
      Emmiter_Disc.setTextureSize(64, 32);
      Emmiter_Disc.mirror = true;
      setRotation(Emmiter_Disc, 0F, 0F, 0F);
      Emmiter1 = new ModelRenderer(this, 26, 0);
      Emmiter1.addBox(0.8F, 0.2F, 7F, 1, 0, 1);
      Emmiter1.setRotationPoint(0F, 0F, 0F);
      Emmiter1.setTextureSize(64, 32);
      Emmiter1.mirror = true;
      setRotation(Emmiter1, 0F, 0F, 0F);
      Emmiter2 = new ModelRenderer(this, 26, 0);
      Emmiter2.addBox(0.2F, 0.2F, 7F, 1, 0, 1);
      Emmiter2.setRotationPoint(0F, 0F, 0F);
      Emmiter2.setTextureSize(64, 32);
      Emmiter2.mirror = true;
      setRotation(Emmiter2, 0F, 0F, 0F);
      Emmiter3 = new ModelRenderer(this, 26, 0);
      Emmiter3.addBox(0.2F, 1.8F, 7F, 1, 0, 1);
      Emmiter3.setRotationPoint(0F, 0F, 0F);
      Emmiter3.setTextureSize(64, 32);
      Emmiter3.mirror = true;
      setRotation(Emmiter3, 0F, 0F, 0F);
      Emmiter4 = new ModelRenderer(this, 26, 0);
      Emmiter4.addBox(0.8F, 1.8F, 7F, 1, 0, 1);
      Emmiter4.setRotationPoint(0F, 0F, 0F);
      Emmiter4.setTextureSize(64, 32);
      Emmiter4.mirror = true;
      setRotation(Emmiter4, 0F, 0F, 0F);
      Emmiter5 = new ModelRenderer(this, 18, 0);
      Emmiter5.addBox(0.2F, 0.8F, 7F, 0, 1, 1);
      Emmiter5.setRotationPoint(0F, 0F, 0F);
      Emmiter5.setTextureSize(64, 32);
      Emmiter5.mirror = true;
      setRotation(Emmiter5, 0F, 0F, 0F);
      Emmiter6 = new ModelRenderer(this, 18, 0);
      Emmiter6.addBox(0.2F, 0.2F, 7F, 0, 1, 1);
      Emmiter6.setRotationPoint(0F, 0F, 0F);
      Emmiter6.setTextureSize(64, 32);
      Emmiter6.mirror = true;
      setRotation(Emmiter6, 0F, 0F, 0F);
      Emmiter7 = new ModelRenderer(this, 18, 0);
      Emmiter7.addBox(1.8F, 0.8F, 7F, 0, 1, 1);
      Emmiter7.setRotationPoint(0F, 0F, 0F);
      Emmiter7.setTextureSize(64, 32);
      Emmiter7.mirror = true;
      setRotation(Emmiter7, 0F, 0F, 0F);
      Emmiter8 = new ModelRenderer(this, 18, 0);
      Emmiter8.addBox(1.8F, 0.2F, 7F, 0, 1, 1);
      Emmiter8.setRotationPoint(0F, 0F, 0F);
      Emmiter8.setTextureSize(64, 32);
      Emmiter8.mirror = true;
      setRotation(Emmiter8, 0F, 0F, 0F);
      Emmiter9 = new ModelRenderer(this, 0, 27);
      Emmiter9.addBox(0.2F, 0.2F, 7.5F, 1, 1, 0);
      Emmiter9.setRotationPoint(0F, 0F, 0F);
      Emmiter9.setTextureSize(64, 32);
      Emmiter9.mirror = true;
      setRotation(Emmiter9, 0F, 0F, 0F);
      Emmiter10 = new ModelRenderer(this, 0, 27);
      Emmiter10.addBox(0.2F, 0.8F, 7.5F, 1, 1, 0);
      Emmiter10.setRotationPoint(0F, 0F, 0F);
      Emmiter10.setTextureSize(64, 32);
      Emmiter10.mirror = true;
      setRotation(Emmiter10, 0F, 0F, 0F);
      Emmiter11 = new ModelRenderer(this, 0, 27);
      Emmiter11.addBox(0.8F, 0.2F, 7.5F, 1, 1, 0);
      Emmiter11.setRotationPoint(0F, 0F, 0F);
      Emmiter11.setTextureSize(64, 32);
      Emmiter11.mirror = true;
      setRotation(Emmiter11, 0F, 0F, 0F);
      Emmiter12 = new ModelRenderer(this, 0, 27);
      Emmiter12.addBox(0.8F, 0.8F, 7.5F, 1, 1, 0);
      Emmiter12.setRotationPoint(0F, 0F, 0F);
      Emmiter12.setTextureSize(64, 32);
      Emmiter12.mirror = true;
      setRotation(Emmiter12, 0F, 0F, 0F);
      Emmiter_Rod = new ModelRenderer(this, 0, 7);
      Emmiter_Rod.addBox(0.5F, 0.5F, 7.5F, 1, 1, 1);
      Emmiter_Rod.setRotationPoint(0F, 0F, 0F);
      Emmiter_Rod.setTextureSize(64, 32);
      Emmiter_Rod.mirror = true;
      setRotation(Emmiter_Rod, 0F, 0F, 0F);
      Emmiter = new ModelRenderer(this, 15, 11);
      Emmiter.addBox(0F, 0F, 8.5F, 2, 2, 1);
      Emmiter.setRotationPoint(0F, 0F, 0F);
      Emmiter.setTextureSize(64, 32);
      Emmiter.mirror = true;
      setRotation(Emmiter, 0F, 0F, 0F);
      BladeEmiiter = new ModelRenderer(this, 4, 7);
      BladeEmiiter.addBox(0.5F, 0.5F, 8.7F, 1, 1, 1);
      BladeEmiiter.setRotationPoint(0F, 0F, 0F);
      BladeEmiiter.setTextureSize(64, 32);
      BladeEmiiter.mirror = true;
      setRotation(BladeEmiiter, 0F, 0F, 0F);
      Blade = new ModelRenderer(this, 34, 17);
      Blade.addBox(0.5F, 0.5F, 9.7F, 1, 1, 14);
      Blade.setRotationPoint(0F, 0F, 0F);
      Blade.setTextureSize(64, 32);
      Blade.mirror = true;
      setRotation(Blade, 0F, 0F, 0F);
  }
  
  public void render(Entity entity, float f, float f1, float f2, float f3, float f4, float f5)
  {
    super.render(entity, f, f1, f2, f3, f4, f5);
    setRotationAngles(f, f1, f2, f3, f4, f5, entity);
    MainBody.render(f5);
    Pomel2.render(f5);
    Pomel1.render(f5);
    Clip.render(f5);
    Middle_body.render(f5);
    Disc1.render(f5);
    Disc2.render(f5);
    Disc3.render(f5);
    Disc4.render(f5);
    Disc5.render(f5);
    Disc6.render(f5);
    Disc7.render(f5);
    Disc8.render(f5);
    Disc9.render(f5);
    Emmiter_Disc.render(f5);
    Emmiter1.render(f5);
    Emmiter2.render(f5);
    Emmiter3.render(f5);
    Emmiter4.render(f5);
    Emmiter5.render(f5);
    Emmiter6.render(f5);
    Emmiter7.render(f5);
    Emmiter8.render(f5);
    Emmiter9.render(f5);
    Emmiter10.render(f5);
    Emmiter11.render(f5);
    Emmiter12.render(f5);
    Emmiter_Rod.render(f5);
    Emmiter.render(f5);
    BladeEmiiter.render(f5);
    Blade.render(f5);
  }
  
  private void setRotation(ModelRenderer model, float x, float y, float z)
  {
    model.rotateAngleX = x;
    model.rotateAngleY = y;
    model.rotateAngleZ = z;
  }
  
  public void setRotationAngles(float f, float f1, float f2, float f3, float f4, float f5, Entity ent)
  {
    super.setRotationAngles(f, f1, f2, f3, f4, f5, ent);
  }

}


//Renderer

package StarWars.LightSabers.Renders;

import org.lwjgl.opengl.GL11;

import StarWars.LightSabers.Models.ProdigalSonModel;
import StarWars.lib.STRINGS;
import net.minecraft.client.Minecraft;
import net.minecraft.entity.Entity;
import net.minecraft.item.ItemStack;
import net.minecraft.util.ResourceLocation;
import net.minecraftforge.client.IItemRenderer;

public class ProdigalSonRenderer implements IItemRenderer {
	
	protected ProdigalSonModel model;
	
	public ProdigalSonRenderer() {
		model = new ProdigalSonModel();
		
	}
@Override
	public boolean handleRenderType(ItemStack item, ItemRenderType type) {
		switch(type){
		case EQUIPPED:
		case EQUIPPED_FIRST_PERSON:
			return true;
		default: return false;
		}
	}

	@Override
	public boolean shouldUseRenderHelper(ItemRenderType type, ItemStack item, ItemRendererHelper helper) {
		return false;
	}

	@Override
	public void renderItem(ItemRenderType type, ItemStack item, Object... data) {
		
		switch(type){
		case EQUIPPED:
		case EQUIPPED_FIRST_PERSON:
			GL11.glPushMatrix();
			
			Minecraft.getMinecraft().renderEngine.bindTexture(new ResourceLocation(STRINGS.MODID, "textures/models/Items/prodigalson_on.png"));
			
			GL11.glRotatef(90.0F, 0.0F, 0.0F, 1.0F);
			GL11.glRotatef(180.0F, 1.0F, 0.0F, 0.0F);
			GL11.glRotatef(-45.0F, 0.0F, 0.0F, 1.0F);

			
			GL11.glTranslatef(-0.6F, 0.5F, 0.0F);

			
			model.render((Entity)data[1], 0.0F, 0.0F, 0.0F, 0.0F, 0.0F, 0.0625F);

			
			GL11.glPopMatrix();
		default:
			break;
		}
	}
}
