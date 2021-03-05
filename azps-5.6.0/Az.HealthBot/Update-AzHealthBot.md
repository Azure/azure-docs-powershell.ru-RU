---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/update-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
ms.openlocfilehash: a0dc204bb6dc1a91031a87fd113c525f282f090e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013208"
---
# <span data-ttu-id="400cd-101">Update-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="400cd-101">Update-AzHealthBot</span></span>

## <span data-ttu-id="400cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="400cd-102">SYNOPSIS</span></span>
<span data-ttu-id="400cd-103">Исправление healthBot.</span><span class="sxs-lookup"><span data-stu-id="400cd-103">Patch a HealthBot.</span></span>

## <span data-ttu-id="400cd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="400cd-104">SYNTAX</span></span>

### <span data-ttu-id="400cd-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="400cd-105">UpdateExpanded (Default)</span></span>
```
Update-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Sku <SkuName>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="400cd-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="400cd-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzHealthBot -InputObject <IHealthBotIdentity> [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="400cd-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="400cd-107">DESCRIPTION</span></span>
<span data-ttu-id="400cd-108">Исправление healthBot.</span><span class="sxs-lookup"><span data-stu-id="400cd-108">Patch a HealthBot.</span></span>

## <span data-ttu-id="400cd-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="400cd-109">EXAMPLES</span></span>

### <span data-ttu-id="400cd-110">Пример 1. Обновление HealthBot по именам и именам групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="400cd-110">Example 1: update HealthBot by Resourcegroupname and Name</span></span>
```powershell
PS C:\> update-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot -Sku S1

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="400cd-111">Update HealthBot by Resourcegroupname and Name</span><span class="sxs-lookup"><span data-stu-id="400cd-111">update HealthBot by Resourcegroupname and Name</span></span>

### <span data-ttu-id="400cd-112">Пример 2. Обновление HealthBot с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="400cd-112">Example 2: update HealthBot by InputObject</span></span>
```powershell
PS C:\> $getHealth = Get-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot
Update-AzHealthBot -InputObject $getHealth -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="400cd-113">Update HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="400cd-113">update HealthBot by InputObject</span></span>

## <span data-ttu-id="400cd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="400cd-114">PARAMETERS</span></span>

### <span data-ttu-id="400cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="400cd-115">-DefaultProfile</span></span>
<span data-ttu-id="400cd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="400cd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400cd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="400cd-117">-InputObject</span></span>
<span data-ttu-id="400cd-118">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="400cd-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="400cd-119">-Name</span><span class="sxs-lookup"><span data-stu-id="400cd-119">-Name</span></span>
<span data-ttu-id="400cd-120">Имя ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="400cd-120">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400cd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="400cd-121">-ResourceGroupName</span></span>
<span data-ttu-id="400cd-122">Имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="400cd-122">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400cd-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="400cd-123">-Sku</span></span>
<span data-ttu-id="400cd-124">Имя SKU HealthBot</span><span class="sxs-lookup"><span data-stu-id="400cd-124">The name of the HealthBot SKU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400cd-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="400cd-125">-SubscriptionId</span></span>
<span data-ttu-id="400cd-126">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="400cd-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400cd-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="400cd-127">-Tag</span></span>
<span data-ttu-id="400cd-128">Теги для бота HealthBot.</span><span class="sxs-lookup"><span data-stu-id="400cd-128">Tags for a HealthBot.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400cd-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="400cd-129">-Confirm</span></span>
<span data-ttu-id="400cd-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="400cd-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400cd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="400cd-131">-WhatIf</span></span>
<span data-ttu-id="400cd-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="400cd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="400cd-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="400cd-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="400cd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="400cd-134">CommonParameters</span></span>
<span data-ttu-id="400cd-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="400cd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="400cd-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="400cd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="400cd-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="400cd-137">INPUTS</span></span>

### <span data-ttu-id="400cd-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="400cd-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="400cd-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="400cd-139">OUTPUTS</span></span>

### <span data-ttu-id="400cd-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="400cd-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="400cd-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="400cd-141">NOTES</span></span>

<span data-ttu-id="400cd-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="400cd-142">ALIASES</span></span>

<span data-ttu-id="400cd-143">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="400cd-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="400cd-144">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="400cd-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="400cd-145">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="400cd-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="400cd-146">INPUTOBJECT <IHealthBotIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="400cd-146">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="400cd-147">`[BotName <String>]`: Название ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="400cd-147">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="400cd-148">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="400cd-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="400cd-149">`[ResourceGroupName <String>]`: имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="400cd-149">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="400cd-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="400cd-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="400cd-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="400cd-151">RELATED LINKS</span></span>

