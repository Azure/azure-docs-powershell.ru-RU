---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94245097"
---
# <span data-ttu-id="8b2e1-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="8b2e1-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="8b2e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b2e1-102">SYNOPSIS</span></span>
<span data-ttu-id="8b2e1-103">Операция удаления удостоверения гибридного компьютера в Azure.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="8b2e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b2e1-104">SYNTAX</span></span>

### <span data-ttu-id="8b2e1-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b2e1-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8b2e1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8b2e1-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8b2e1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b2e1-107">DESCRIPTION</span></span>
<span data-ttu-id="8b2e1-108">Операция удаления удостоверения гибридного компьютера в Azure.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="8b2e1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b2e1-109">EXAMPLES</span></span>

### <span data-ttu-id="8b2e1-110">Пример 1: удаление подключенного компьютера</span><span class="sxs-lookup"><span data-stu-id="8b2e1-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="8b2e1-111">Удаляет подключенный компьютер.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="8b2e1-112">Пример 2: удаление подключенных компьютеров через конвейер</span><span class="sxs-lookup"><span data-stu-id="8b2e1-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="8b2e1-113">Удаляет все компьютеры в `contoso-connected-machines` группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="8b2e1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b2e1-114">PARAMETERS</span></span>

### <span data-ttu-id="8b2e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b2e1-115">-DefaultProfile</span></span>
<span data-ttu-id="8b2e1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b2e1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b2e1-117">-InputObject</span></span>
<span data-ttu-id="8b2e1-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b2e1-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8b2e1-119">-Name</span></span>
<span data-ttu-id="8b2e1-120">Имя гибридного компьютера.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="8b2e1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b2e1-121">-PassThru</span></span>
<span data-ttu-id="8b2e1-122">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8b2e1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b2e1-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b2e1-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="8b2e1-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b2e1-125">-SubscriptionId</span></span>
<span data-ttu-id="8b2e1-126">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8b2e1-127">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8b2e1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b2e1-128">-Confirm</span></span>
<span data-ttu-id="8b2e1-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b2e1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b2e1-130">-WhatIf</span></span>
<span data-ttu-id="8b2e1-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b2e1-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b2e1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b2e1-133">CommonParameters</span></span>
<span data-ttu-id="8b2e1-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b2e1-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b2e1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b2e1-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b2e1-136">INPUTS</span></span>

### <span data-ttu-id="8b2e1-137">Microsoft. Azure. PowerShell. командлеты. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="8b2e1-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="8b2e1-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b2e1-138">OUTPUTS</span></span>

### <span data-ttu-id="8b2e1-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b2e1-139">System.Boolean</span></span>

## <span data-ttu-id="8b2e1-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b2e1-140">NOTES</span></span>

<span data-ttu-id="8b2e1-141">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="8b2e1-141">ALIASES</span></span>

<span data-ttu-id="8b2e1-142">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="8b2e1-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8b2e1-143">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8b2e1-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8b2e1-145">INPUTOBJECT <IConnectedMachineIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="8b2e1-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8b2e1-146">`[ExtensionName <String>]`: Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="8b2e1-147">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="8b2e1-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8b2e1-148">`[Name <String>]`: Имя гибридного компьютера.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="8b2e1-149">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="8b2e1-150">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8b2e1-151">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="8b2e1-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8b2e1-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b2e1-152">RELATED LINKS</span></span>

