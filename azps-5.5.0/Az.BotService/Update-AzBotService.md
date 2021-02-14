---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/update-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
ms.openlocfilehash: f7dd02a214fa32223e052c1999329699f1c653e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234908"
---
# <span data-ttu-id="edf7f-101">Update-AzBotService</span><span class="sxs-lookup"><span data-stu-id="edf7f-101">Update-AzBotService</span></span>

## <span data-ttu-id="edf7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edf7f-102">SYNOPSIS</span></span>
<span data-ttu-id="edf7f-103">Обновление службы ботов</span><span class="sxs-lookup"><span data-stu-id="edf7f-103">Updates a Bot Service</span></span>

## <span data-ttu-id="edf7f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="edf7f-104">SYNTAX</span></span>

### <span data-ttu-id="edf7f-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="edf7f-105">UpdateExpanded (Default)</span></span>
```
Update-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="edf7f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="edf7f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBotService -InputObject <IBotServiceIdentity> [-Description <String>]
 [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="edf7f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="edf7f-107">DESCRIPTION</span></span>
<span data-ttu-id="edf7f-108">Обновление службы ботов</span><span class="sxs-lookup"><span data-stu-id="edf7f-108">Updates a Bot Service</span></span>

## <span data-ttu-id="edf7f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="edf7f-109">EXAMPLES</span></span>

### <span data-ttu-id="edf7f-110">Пример 1. Обновление бота по имени и ресурсу ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edf7f-110">Example 1: Update the Bot by Name and ResourceGroupName</span></span>
```powershell
PS C:\> Update-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest' -kind Bot

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"0700e71b-0000-1800-0000-5fd73ed80000" Bot  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="edf7f-111">Обновление бота по имени и ресурсу ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edf7f-111">Update the Bot by Name and ResourceGroupName</span></span>

### <span data-ttu-id="edf7f-112">Пример 2. Обновление бота с помощью inputObject</span><span class="sxs-lookup"><span data-stu-id="edf7f-112">Example 2: Update the Bot by InputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest'
Update-AzBotService -InputObject $getAzbot -kind sdk

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"07008b1c-0000-1800-0000-5fd73f9e0000" sdk  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="edf7f-113">Обновление бота с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="edf7f-113">Update the Bot by InputObject</span></span>

## <span data-ttu-id="edf7f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edf7f-114">PARAMETERS</span></span>

### <span data-ttu-id="edf7f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edf7f-115">-DefaultProfile</span></span>
<span data-ttu-id="edf7f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="edf7f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edf7f-117">-Description</span><span class="sxs-lookup"><span data-stu-id="edf7f-117">-Description</span></span>
<span data-ttu-id="edf7f-118">Описание бота</span><span class="sxs-lookup"><span data-stu-id="edf7f-118">The description of the bot</span></span>

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

### <span data-ttu-id="edf7f-119">-DeveloperAppInsightKey</span><span class="sxs-lookup"><span data-stu-id="edf7f-119">-DeveloperAppInsightKey</span></span>
<span data-ttu-id="edf7f-120">Ключ "Application Insights"</span><span class="sxs-lookup"><span data-stu-id="edf7f-120">The Application Insights key</span></span>

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

### <span data-ttu-id="edf7f-121">-DeveloperAppInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="edf7f-121">-DeveloperAppInsightsApiKey</span></span>
<span data-ttu-id="edf7f-122">Ключ API Application Insights</span><span class="sxs-lookup"><span data-stu-id="edf7f-122">The Application Insights Api Key</span></span>

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

### <span data-ttu-id="edf7f-123">-DeveloperAppInsightsApplicationId</span><span class="sxs-lookup"><span data-stu-id="edf7f-123">-DeveloperAppInsightsApplicationId</span></span>
<span data-ttu-id="edf7f-124">ИД приложения Application Insights</span><span class="sxs-lookup"><span data-stu-id="edf7f-124">The Application Insights App Id</span></span>

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

### <span data-ttu-id="edf7f-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="edf7f-125">-DisplayName</span></span>
<span data-ttu-id="edf7f-126">Имя бота</span><span class="sxs-lookup"><span data-stu-id="edf7f-126">The Name of the bot</span></span>

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

### <span data-ttu-id="edf7f-127">-Конечная точка</span><span class="sxs-lookup"><span data-stu-id="edf7f-127">-Endpoint</span></span>
<span data-ttu-id="edf7f-128">Конечная точка бота</span><span class="sxs-lookup"><span data-stu-id="edf7f-128">The bot's endpoint</span></span>

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

### <span data-ttu-id="edf7f-129">-Etag</span><span class="sxs-lookup"><span data-stu-id="edf7f-129">-Etag</span></span>
<span data-ttu-id="edf7f-130">Тег сущности</span><span class="sxs-lookup"><span data-stu-id="edf7f-130">Entity Tag</span></span>

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

### <span data-ttu-id="edf7f-131">-IconUrl</span><span class="sxs-lookup"><span data-stu-id="edf7f-131">-IconUrl</span></span>
<span data-ttu-id="edf7f-132">Url-адрес значка бота</span><span class="sxs-lookup"><span data-stu-id="edf7f-132">The Icon Url of the bot</span></span>

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

### <span data-ttu-id="edf7f-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edf7f-133">-InputObject</span></span>
<span data-ttu-id="edf7f-134">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="edf7f-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="edf7f-135">-Kind</span><span class="sxs-lookup"><span data-stu-id="edf7f-135">-Kind</span></span>
<span data-ttu-id="edf7f-136">Обязательно.</span><span class="sxs-lookup"><span data-stu-id="edf7f-136">Required.</span></span>
<span data-ttu-id="edf7f-137">Возвращает или задает тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="edf7f-137">Gets or sets the Kind of the resource.</span></span>

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

### <span data-ttu-id="edf7f-138">-Location</span><span class="sxs-lookup"><span data-stu-id="edf7f-138">-Location</span></span>
<span data-ttu-id="edf7f-139">Определяет расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="edf7f-139">Specifies the location of the resource.</span></span>

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

### <span data-ttu-id="edf7f-140">-LuisAppId</span><span class="sxs-lookup"><span data-stu-id="edf7f-140">-LuisAppId</span></span>
<span data-ttu-id="edf7f-141">Коллекция ИД приложения ДОИ3</span><span class="sxs-lookup"><span data-stu-id="edf7f-141">Collection of LUIS App Ids</span></span>

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

### <span data-ttu-id="edf7f-142">-НояркиКомассия</span><span class="sxs-lookup"><span data-stu-id="edf7f-142">-LuisKey</span></span>
<span data-ttu-id="edf7f-143">Ключ ДОИ2</span><span class="sxs-lookup"><span data-stu-id="edf7f-143">The LUIS Key</span></span>

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

### <span data-ttu-id="edf7f-144">-MsaAppId</span><span class="sxs-lookup"><span data-stu-id="edf7f-144">-MsaAppId</span></span>
<span data-ttu-id="edf7f-145">Microsoft App Id for the bot</span><span class="sxs-lookup"><span data-stu-id="edf7f-145">Microsoft App Id for the bot</span></span>

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

### <span data-ttu-id="edf7f-146">-Name</span><span class="sxs-lookup"><span data-stu-id="edf7f-146">-Name</span></span>
<span data-ttu-id="edf7f-147">Имя ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="edf7f-147">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="edf7f-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edf7f-148">-ResourceGroupName</span></span>
<span data-ttu-id="edf7f-149">Имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="edf7f-149">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="edf7f-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="edf7f-150">-SkuName</span></span>
<span data-ttu-id="edf7f-151">Имя SKU</span><span class="sxs-lookup"><span data-stu-id="edf7f-151">The sku name</span></span>

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

### <span data-ttu-id="edf7f-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="edf7f-152">-SubscriptionId</span></span>
<span data-ttu-id="edf7f-153">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="edf7f-153">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="edf7f-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="edf7f-154">-Tag</span></span>
<span data-ttu-id="edf7f-155">Содержит теги ресурсов, определенные как пары ключей и значений.</span><span class="sxs-lookup"><span data-stu-id="edf7f-155">Contains resource tags defined as key/value pairs.</span></span>

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

### <span data-ttu-id="edf7f-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edf7f-156">-Confirm</span></span>
<span data-ttu-id="edf7f-157">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edf7f-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edf7f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edf7f-158">-WhatIf</span></span>
<span data-ttu-id="edf7f-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edf7f-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edf7f-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="edf7f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edf7f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf7f-161">CommonParameters</span></span>
<span data-ttu-id="edf7f-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edf7f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf7f-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edf7f-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf7f-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="edf7f-164">INPUTS</span></span>

### <span data-ttu-id="edf7f-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="edf7f-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="edf7f-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="edf7f-166">OUTPUTS</span></span>

### <span data-ttu-id="edf7f-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="edf7f-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="edf7f-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="edf7f-168">NOTES</span></span>

<span data-ttu-id="edf7f-169">ALIASES</span><span class="sxs-lookup"><span data-stu-id="edf7f-169">ALIASES</span></span>

<span data-ttu-id="edf7f-170">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="edf7f-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="edf7f-171">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="edf7f-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="edf7f-172">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="edf7f-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="edf7f-173">INPUTOBJECT <IBotServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="edf7f-173">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="edf7f-174">`[ChannelName <ChannelName?>]`: Название ресурса канала.</span><span class="sxs-lookup"><span data-stu-id="edf7f-174">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="edf7f-175">`[ConnectionName <String>]`: имя ресурса Параметра подключения к службе-роботу</span><span class="sxs-lookup"><span data-stu-id="edf7f-175">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="edf7f-176">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="edf7f-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="edf7f-177">`[ResourceGroupName <String>]`: имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="edf7f-177">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="edf7f-178">`[ResourceName <String>]`: Название ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="edf7f-178">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="edf7f-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="edf7f-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="edf7f-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="edf7f-180">RELATED LINKS</span></span>

