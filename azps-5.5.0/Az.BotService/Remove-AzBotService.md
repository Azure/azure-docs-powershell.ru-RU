---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/remove-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
ms.openlocfilehash: ef75ec3e48a68bffce7c5b281f542bd2e3dba9d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229260"
---
# <span data-ttu-id="232d5-101">Remove-AzBotService</span><span class="sxs-lookup"><span data-stu-id="232d5-101">Remove-AzBotService</span></span>

## <span data-ttu-id="232d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="232d5-102">SYNOPSIS</span></span>
<span data-ttu-id="232d5-103">Удаляет службу ботов из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="232d5-103">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="232d5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="232d5-104">SYNTAX</span></span>

### <span data-ttu-id="232d5-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="232d5-105">Delete (Default)</span></span>
```
Remove-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="232d5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="232d5-106">DeleteViaIdentity</span></span>
```
Remove-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="232d5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="232d5-107">DESCRIPTION</span></span>
<span data-ttu-id="232d5-108">Удаляет службу ботов из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="232d5-108">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="232d5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="232d5-109">EXAMPLES</span></span>

### <span data-ttu-id="232d5-110">Пример 1. Удаление службы BotService по имени и ресурсуGroupName</span><span class="sxs-lookup"><span data-stu-id="232d5-110">Example 1: Delete the BotService By Name and ResourceGroupName</span></span>
```powershell
PS C:\> Remove-AzBotService -Name youri-bot -ResourceGroupName youriBotTest

```

<span data-ttu-id="232d5-111">Удаление службы BotService по имени и ресурсу ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="232d5-111">Delete the BotService By Name and ResourceGroupName</span></span>

### <span data-ttu-id="232d5-112">Пример 2. Удаление ботслужбы по inputObject</span><span class="sxs-lookup"><span data-stu-id="232d5-112">Example 2: Delete the BotService By InputObject</span></span>
```powershell
PS C:\> $getservice = Get-AzBotService -Name youriechobottest -ResourceGroupName youriBotTest
Remove-AzBotService -InputObject $getservice

```

<span data-ttu-id="232d5-113">Удаление ботслужбы по inputObject</span><span class="sxs-lookup"><span data-stu-id="232d5-113">Delete the BotService By InputObject</span></span>

## <span data-ttu-id="232d5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="232d5-114">PARAMETERS</span></span>

### <span data-ttu-id="232d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="232d5-115">-DefaultProfile</span></span>
<span data-ttu-id="232d5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="232d5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="232d5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="232d5-117">-InputObject</span></span>
<span data-ttu-id="232d5-118">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="232d5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="232d5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="232d5-119">-Name</span></span>
<span data-ttu-id="232d5-120">Имя ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="232d5-120">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232d5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="232d5-121">-PassThru</span></span>
<span data-ttu-id="232d5-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="232d5-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232d5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="232d5-123">-ResourceGroupName</span></span>
<span data-ttu-id="232d5-124">Имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="232d5-124">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232d5-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="232d5-125">-SubscriptionId</span></span>
<span data-ttu-id="232d5-126">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="232d5-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232d5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="232d5-127">-Confirm</span></span>
<span data-ttu-id="232d5-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="232d5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="232d5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="232d5-129">-WhatIf</span></span>
<span data-ttu-id="232d5-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="232d5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="232d5-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="232d5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="232d5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="232d5-132">CommonParameters</span></span>
<span data-ttu-id="232d5-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="232d5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="232d5-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="232d5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="232d5-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="232d5-135">INPUTS</span></span>

### <span data-ttu-id="232d5-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="232d5-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="232d5-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="232d5-137">OUTPUTS</span></span>

### <span data-ttu-id="232d5-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="232d5-138">System.Boolean</span></span>

## <span data-ttu-id="232d5-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="232d5-139">NOTES</span></span>

<span data-ttu-id="232d5-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="232d5-140">ALIASES</span></span>

<span data-ttu-id="232d5-141">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="232d5-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="232d5-142">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="232d5-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="232d5-143">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="232d5-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="232d5-144">INPUTOBJECT <IBotServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="232d5-144">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="232d5-145">`[ChannelName <ChannelName?>]`: Название ресурса канала.</span><span class="sxs-lookup"><span data-stu-id="232d5-145">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="232d5-146">`[ConnectionName <String>]`: имя ресурса Параметра подключения к службе-роботу</span><span class="sxs-lookup"><span data-stu-id="232d5-146">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="232d5-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="232d5-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="232d5-148">`[ResourceGroupName <String>]`: имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="232d5-148">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="232d5-149">`[ResourceName <String>]`: Название ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="232d5-149">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="232d5-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="232d5-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="232d5-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="232d5-151">RELATED LINKS</span></span>

