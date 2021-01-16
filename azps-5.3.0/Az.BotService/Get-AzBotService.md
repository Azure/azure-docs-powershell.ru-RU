---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/get-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
ms.openlocfilehash: 4324c1e78ce56cc4b56455eaaff266b52c1d87d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509421"
---
# <span data-ttu-id="a9c38-101">Get-AzBotService</span><span class="sxs-lookup"><span data-stu-id="a9c38-101">Get-AzBotService</span></span>

## <span data-ttu-id="a9c38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9c38-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c38-103">Возвращает ботслужба, заданную параметрами.</span><span class="sxs-lookup"><span data-stu-id="a9c38-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="a9c38-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a9c38-104">SYNTAX</span></span>

### <span data-ttu-id="a9c38-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a9c38-105">List1 (Default)</span></span>
```
Get-AzBotService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a9c38-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a9c38-106">Get</span></span>
```
Get-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a9c38-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a9c38-107">GetViaIdentity</span></span>
```
Get-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a9c38-108">Список</span><span class="sxs-lookup"><span data-stu-id="a9c38-108">List</span></span>
```
Get-AzBotService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9c38-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9c38-109">DESCRIPTION</span></span>
<span data-ttu-id="a9c38-110">Возвращает ботслужба, заданную параметрами.</span><span class="sxs-lookup"><span data-stu-id="a9c38-110">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="a9c38-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a9c38-111">EXAMPLES</span></span>

### <span data-ttu-id="a9c38-112">Пример 1. Получить все BotServices</span><span class="sxs-lookup"><span data-stu-id="a9c38-112">Example 1: Get all BotServices</span></span>
```powershell
PS C:\> Get-AzBotService

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="a9c38-113">Получить все BotServices</span><span class="sxs-lookup"><span data-stu-id="a9c38-113">Get all BotServices</span></span>

### <span data-ttu-id="a9c38-114">Пример 2. Получить BotService по resourceGroupName и Name</span><span class="sxs-lookup"><span data-stu-id="a9c38-114">Example 2: Get the BotService by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot F0              Microsoft.BotService/botServices
```

<span data-ttu-id="a9c38-115">Получить botService по resourceGroupName и Name</span><span class="sxs-lookup"><span data-stu-id="a9c38-115">Get the BotService by ResourceGroupName and Name</span></span>

### <span data-ttu-id="a9c38-116">Пример 3. Получить все BotServices от ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9c38-116">Example 3: Get all BotServices by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzBotService -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="a9c38-117">Получить все BotServices по ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9c38-117">Get all BotServices by ResourceGroupName</span></span>

### <span data-ttu-id="a9c38-118">Пример 4. Получить BotService по inputObject</span><span class="sxs-lookup"><span data-stu-id="a9c38-118">Example 4: Get the BotService by inputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'
Get-AzBotService -InputObject $getAzbot

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="a9c38-119">Получить BotService по inputObject</span><span class="sxs-lookup"><span data-stu-id="a9c38-119">Get the BotService by inputObject</span></span>

## <span data-ttu-id="a9c38-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9c38-120">PARAMETERS</span></span>

### <span data-ttu-id="a9c38-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c38-121">-DefaultProfile</span></span>
<span data-ttu-id="a9c38-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c38-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9c38-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9c38-123">-InputObject</span></span>
<span data-ttu-id="a9c38-124">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="a9c38-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9c38-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a9c38-125">-Name</span></span>
<span data-ttu-id="a9c38-126">Имя ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="a9c38-126">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9c38-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9c38-127">-ResourceGroupName</span></span>
<span data-ttu-id="a9c38-128">Имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="a9c38-128">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9c38-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9c38-129">-SubscriptionId</span></span>
<span data-ttu-id="a9c38-130">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c38-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9c38-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c38-131">CommonParameters</span></span>
<span data-ttu-id="a9c38-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9c38-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c38-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9c38-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c38-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9c38-134">INPUTS</span></span>

### <span data-ttu-id="a9c38-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="a9c38-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="a9c38-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a9c38-136">OUTPUTS</span></span>

### <span data-ttu-id="a9c38-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="a9c38-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="a9c38-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a9c38-138">NOTES</span></span>

<span data-ttu-id="a9c38-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a9c38-139">ALIASES</span></span>

<span data-ttu-id="a9c38-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a9c38-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a9c38-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="a9c38-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a9c38-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a9c38-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a9c38-143">INPUTOBJECT <IBotServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="a9c38-143">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a9c38-144">`[ChannelName <ChannelName?>]`: Название ресурса канала.</span><span class="sxs-lookup"><span data-stu-id="a9c38-144">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="a9c38-145">`[ConnectionName <String>]`: имя ресурса Параметра подключения к службе-роботу</span><span class="sxs-lookup"><span data-stu-id="a9c38-145">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="a9c38-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="a9c38-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a9c38-147">`[ResourceGroupName <String>]`: имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="a9c38-147">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="a9c38-148">`[ResourceName <String>]`: Название ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="a9c38-148">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="a9c38-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="a9c38-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a9c38-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9c38-150">RELATED LINKS</span></span>

