---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/remove-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
ms.openlocfilehash: 2b2a4eba0a062b90866479409e80bbe7e55c1984
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013219"
---
# <span data-ttu-id="0ae5f-101">Remove-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="0ae5f-101">Remove-AzHealthBot</span></span>

## <span data-ttu-id="0ae5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ae5f-102">SYNOPSIS</span></span>
<span data-ttu-id="0ae5f-103">"Удалить HealthBot".</span><span class="sxs-lookup"><span data-stu-id="0ae5f-103">Delete a HealthBot.</span></span>

## <span data-ttu-id="0ae5f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0ae5f-104">SYNTAX</span></span>

### <span data-ttu-id="0ae5f-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ae5f-105">Delete (Default)</span></span>
```
Remove-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0ae5f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0ae5f-106">DeleteViaIdentity</span></span>
```
Remove-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0ae5f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ae5f-107">DESCRIPTION</span></span>
<span data-ttu-id="0ae5f-108">"Удалить HealthBot".</span><span class="sxs-lookup"><span data-stu-id="0ae5f-108">Delete a HealthBot.</span></span>

## <span data-ttu-id="0ae5f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0ae5f-109">EXAMPLES</span></span>

### <span data-ttu-id="0ae5f-110">Пример 1. Удаление HealthBot по resourceGroupName и Name</span><span class="sxs-lookup"><span data-stu-id="0ae5f-110">Example 1: Delete HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzHealthBot -Name yourihealthbot -ResourceGroupName youriTest

```

<span data-ttu-id="0ae5f-111">Delete HealthBot by ResourceGroupName and Name</span><span class="sxs-lookup"><span data-stu-id="0ae5f-111">Delete HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="0ae5f-112">Пример 2. Удаление HealthBot с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="0ae5f-112">Example 2: Delete HealthBot by InputObject</span></span>
```powershell
PS C:\> $gethealthbot = Get-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest
Remove-AzHealthBot -InputObject $gethealthbot

```

<span data-ttu-id="0ae5f-113">Delete HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="0ae5f-113">Delete HealthBot by InputObject</span></span>

## <span data-ttu-id="0ae5f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ae5f-114">PARAMETERS</span></span>

### <span data-ttu-id="0ae5f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ae5f-115">-AsJob</span></span>
<span data-ttu-id="0ae5f-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="0ae5f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0ae5f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ae5f-117">-DefaultProfile</span></span>
<span data-ttu-id="0ae5f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ae5f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ae5f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ae5f-119">-InputObject</span></span>
<span data-ttu-id="0ae5f-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="0ae5f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ae5f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0ae5f-121">-Name</span></span>
<span data-ttu-id="0ae5f-122">Имя ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="0ae5f-122">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="0ae5f-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0ae5f-123">-NoWait</span></span>
<span data-ttu-id="0ae5f-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="0ae5f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0ae5f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ae5f-125">-PassThru</span></span>
<span data-ttu-id="0ae5f-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="0ae5f-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0ae5f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ae5f-127">-ResourceGroupName</span></span>
<span data-ttu-id="0ae5f-128">Имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="0ae5f-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="0ae5f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ae5f-129">-SubscriptionId</span></span>
<span data-ttu-id="0ae5f-130">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="0ae5f-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="0ae5f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ae5f-131">-Confirm</span></span>
<span data-ttu-id="0ae5f-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ae5f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ae5f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ae5f-133">-WhatIf</span></span>
<span data-ttu-id="0ae5f-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ae5f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ae5f-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0ae5f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ae5f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ae5f-136">CommonParameters</span></span>
<span data-ttu-id="0ae5f-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ae5f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ae5f-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ae5f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ae5f-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ae5f-139">INPUTS</span></span>

### <span data-ttu-id="0ae5f-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="0ae5f-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="0ae5f-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0ae5f-141">OUTPUTS</span></span>

### <span data-ttu-id="0ae5f-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0ae5f-142">System.Boolean</span></span>

## <span data-ttu-id="0ae5f-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0ae5f-143">NOTES</span></span>

<span data-ttu-id="0ae5f-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0ae5f-144">ALIASES</span></span>

<span data-ttu-id="0ae5f-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0ae5f-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0ae5f-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="0ae5f-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ae5f-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0ae5f-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0ae5f-148">INPUTOBJECT <IHealthBotIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="0ae5f-148">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0ae5f-149">`[BotName <String>]`: название бота.</span><span class="sxs-lookup"><span data-stu-id="0ae5f-149">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="0ae5f-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="0ae5f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0ae5f-151">`[ResourceGroupName <String>]`: имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="0ae5f-151">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="0ae5f-152">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="0ae5f-152">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="0ae5f-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ae5f-153">RELATED LINKS</span></span>

