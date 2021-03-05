---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/update-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
ms.openlocfilehash: 330aca1a9d4cc9438bdf360d5aee4af914df6c7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007288"
---
# <span data-ttu-id="eb9c5-101">Update-AzBotService</span><span class="sxs-lookup"><span data-stu-id="eb9c5-101">Update-AzBotService</span></span>

## <span data-ttu-id="eb9c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb9c5-102">SYNOPSIS</span></span>
<span data-ttu-id="eb9c5-103">Обновление службы ботов</span><span class="sxs-lookup"><span data-stu-id="eb9c5-103">Updates a Bot Service</span></span>

## <span data-ttu-id="eb9c5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eb9c5-104">SYNTAX</span></span>

### <span data-ttu-id="eb9c5-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eb9c5-105">UpdateExpanded (Default)</span></span>
```
Update-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eb9c5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="eb9c5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBotService -InputObject <IBotServiceIdentity> [-Description <String>]
 [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eb9c5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb9c5-107">DESCRIPTION</span></span>
<span data-ttu-id="eb9c5-108">Обновление службы ботов</span><span class="sxs-lookup"><span data-stu-id="eb9c5-108">Updates a Bot Service</span></span>

## <span data-ttu-id="eb9c5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eb9c5-109">EXAMPLES</span></span>

### <span data-ttu-id="eb9c5-110">Пример 1. Обновление бота по имени и ресурсу ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb9c5-110">Example 1: Update the Bot by Name and ResourceGroupName</span></span>
```powershell
PS C:\> Update-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest' -kind Bot

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"0700e71b-0000-1800-0000-5fd73ed80000" Bot  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="eb9c5-111">Обновление бота по имени и ресурсуGroupName</span><span class="sxs-lookup"><span data-stu-id="eb9c5-111">Update the Bot by Name and ResourceGroupName</span></span>

### <span data-ttu-id="eb9c5-112">Пример 2. Обновление бота с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="eb9c5-112">Example 2: Update the Bot by InputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest'
Update-AzBotService -InputObject $getAzbot -kind sdk

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"07008b1c-0000-1800-0000-5fd73f9e0000" sdk  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="eb9c5-113">Обновление бота с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="eb9c5-113">Update the Bot by InputObject</span></span>

## <span data-ttu-id="eb9c5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb9c5-114">PARAMETERS</span></span>

### <span data-ttu-id="eb9c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb9c5-115">-DefaultProfile</span></span>
<span data-ttu-id="eb9c5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb9c5-117">-Description</span><span class="sxs-lookup"><span data-stu-id="eb9c5-117">-Description</span></span>
<span data-ttu-id="eb9c5-118">Описание бота</span><span class="sxs-lookup"><span data-stu-id="eb9c5-118">The description of the bot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9c5-119">-DeveloperAppInsightKey</span><span class="sxs-lookup"><span data-stu-id="eb9c5-119">-DeveloperAppInsightKey</span></span>
<span data-ttu-id="eb9c5-120">Ключ "Application Insights"</span><span class="sxs-lookup"><span data-stu-id="eb9c5-120">The Application Insights key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9c5-121">-DeveloperAppInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="eb9c5-121">-DeveloperAppInsightsApiKey</span></span>
<span data-ttu-id="eb9c5-122">Ключ API Application Insights</span><span class="sxs-lookup"><span data-stu-id="eb9c5-122">The Application Insights Api Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9c5-123">-DeveloperAppInsightsApplicationId</span><span class="sxs-lookup"><span data-stu-id="eb9c5-123">-DeveloperAppInsightsApplicationId</span></span>
<span data-ttu-id="eb9c5-124">ИД приложения Application Insights</span><span class="sxs-lookup"><span data-stu-id="eb9c5-124">The Application Insights App Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9c5-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="eb9c5-125">-DisplayName</span></span>
<span data-ttu-id="eb9c5-126">Имя бота</span><span class="sxs-lookup"><span data-stu-id="eb9c5-126">The Name of the bot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9c5-127">-Конечная точка</span><span class="sxs-lookup"><span data-stu-id="eb9c5-127">-Endpoint</span></span>
<span data-ttu-id="eb9c5-128">Конечная точка бота</span><span class="sxs-lookup"><span data-stu-id="eb9c5-128">The bot's endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9c5-129">-Etag</span><span class="sxs-lookup"><span data-stu-id="eb9c5-129">-Etag</span></span>
<span data-ttu-id="eb9c5-130">Тег сущности</span><span class="sxs-lookup"><span data-stu-id="eb9c5-130">Entity Tag</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9c5-131">-IconUrl</span><span class="sxs-lookup"><span data-stu-id="eb9c5-131">-IconUrl</span></span>
<span data-ttu-id="eb9c5-132">Url-адрес значка бота</span><span class="sxs-lookup"><span data-stu-id="eb9c5-132">The Icon Url of the bot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9c5-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb9c5-133">-InputObject</span></span>
<span data-ttu-id="eb9c5-134">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9c5-135">-Kind</span><span class="sxs-lookup"><span data-stu-id="eb9c5-135">-Kind</span></span>
<span data-ttu-id="eb9c5-136">Обязательно.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-136">Required.</span></span>
<span data-ttu-id="eb9c5-137">Возвращает или задает тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-137">Gets or sets the Kind of the resource.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.Kind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9c5-138">-Location</span><span class="sxs-lookup"><span data-stu-id="eb9c5-138">-Location</span></span>
<span data-ttu-id="eb9c5-139">Определяет расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-139">Specifies the location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9c5-140">-LuisAppId</span><span class="sxs-lookup"><span data-stu-id="eb9c5-140">-LuisAppId</span></span>
<span data-ttu-id="eb9c5-141">Коллекция ИД приложения ДОИ3</span><span class="sxs-lookup"><span data-stu-id="eb9c5-141">Collection of LUIS App Ids</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9c5-142">-НояркиКомассия</span><span class="sxs-lookup"><span data-stu-id="eb9c5-142">-LuisKey</span></span>
<span data-ttu-id="eb9c5-143">Ключ ОТ ДОИ2</span><span class="sxs-lookup"><span data-stu-id="eb9c5-143">The LUIS Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9c5-144">-MsaAppId</span><span class="sxs-lookup"><span data-stu-id="eb9c5-144">-MsaAppId</span></span>
<span data-ttu-id="eb9c5-145">Microsoft App Id for the bot</span><span class="sxs-lookup"><span data-stu-id="eb9c5-145">Microsoft App Id for the bot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9c5-146">-Name</span><span class="sxs-lookup"><span data-stu-id="eb9c5-146">-Name</span></span>
<span data-ttu-id="eb9c5-147">Имя ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-147">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="eb9c5-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb9c5-148">-ResourceGroupName</span></span>
<span data-ttu-id="eb9c5-149">Имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-149">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="eb9c5-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="eb9c5-150">-SkuName</span></span>
<span data-ttu-id="eb9c5-151">Имя SKU</span><span class="sxs-lookup"><span data-stu-id="eb9c5-151">The sku name</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9c5-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eb9c5-152">-SubscriptionId</span></span>
<span data-ttu-id="eb9c5-153">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-153">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="eb9c5-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="eb9c5-154">-Tag</span></span>
<span data-ttu-id="eb9c5-155">Содержит теги ресурсов, определенные как пары ключей и значений.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-155">Contains resource tags defined as key/value pairs.</span></span>

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

### <span data-ttu-id="eb9c5-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb9c5-156">-Confirm</span></span>
<span data-ttu-id="eb9c5-157">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb9c5-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb9c5-158">-WhatIf</span></span>
<span data-ttu-id="eb9c5-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb9c5-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb9c5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb9c5-161">CommonParameters</span></span>
<span data-ttu-id="eb9c5-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb9c5-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb9c5-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb9c5-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb9c5-164">INPUTS</span></span>

### <span data-ttu-id="eb9c5-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="eb9c5-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="eb9c5-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eb9c5-166">OUTPUTS</span></span>

### <span data-ttu-id="eb9c5-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="eb9c5-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="eb9c5-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eb9c5-168">NOTES</span></span>

<span data-ttu-id="eb9c5-169">ALIASES</span><span class="sxs-lookup"><span data-stu-id="eb9c5-169">ALIASES</span></span>

<span data-ttu-id="eb9c5-170">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="eb9c5-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eb9c5-171">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eb9c5-172">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eb9c5-173">INPUTOBJECT <IBotServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="eb9c5-173">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eb9c5-174">`[ChannelName <ChannelName?>]`: Название ресурса канала.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-174">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="eb9c5-175">`[ConnectionName <String>]`: имя ресурса Параметра подключения к службе-роботу</span><span class="sxs-lookup"><span data-stu-id="eb9c5-175">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="eb9c5-176">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="eb9c5-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eb9c5-177">`[ResourceGroupName <String>]`: имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-177">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="eb9c5-178">`[ResourceName <String>]`: название бота.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-178">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="eb9c5-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="eb9c5-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="eb9c5-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb9c5-180">RELATED LINKS</span></span>

