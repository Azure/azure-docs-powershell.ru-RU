---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
ms.openlocfilehash: 420a73dc1890db1b26cff5ca5289dc030666b038
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312485"
---
# <span data-ttu-id="e93c9-101">Remove-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="e93c9-101">Remove-AzWvdWorkspace</span></span>

## <span data-ttu-id="e93c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e93c9-102">SYNOPSIS</span></span>
<span data-ttu-id="e93c9-103">Удаление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e93c9-103">Remove a workspace.</span></span>

## <span data-ttu-id="e93c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e93c9-104">SYNTAX</span></span>

### <span data-ttu-id="e93c9-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e93c9-105">Delete (Default)</span></span>
```
Remove-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e93c9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e93c9-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e93c9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e93c9-107">DESCRIPTION</span></span>
<span data-ttu-id="e93c9-108">Удаление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e93c9-108">Remove a workspace.</span></span>

## <span data-ttu-id="e93c9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e93c9-109">EXAMPLES</span></span>

### <span data-ttu-id="e93c9-110">Пример 1: Удаление виртуального рабочего стола Windows Worksapce по имени</span><span class="sxs-lookup"><span data-stu-id="e93c9-110">Example 1: Delete a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> Remove-AzWvdWorksapce -ResourceGroupName ResourceGroupName -Name WorkspaceName
```

<span data-ttu-id="e93c9-111">Эта команда удаляет рабочую область виртуальных рабочих столов Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e93c9-111">This command deletes a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="e93c9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e93c9-112">PARAMETERS</span></span>

### <span data-ttu-id="e93c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e93c9-113">-DefaultProfile</span></span>
<span data-ttu-id="e93c9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e93c9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e93c9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e93c9-115">-InputObject</span></span>
<span data-ttu-id="e93c9-116">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="e93c9-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e93c9-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e93c9-117">-Name</span></span>
<span data-ttu-id="e93c9-118">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e93c9-118">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e93c9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e93c9-119">-PassThru</span></span>
<span data-ttu-id="e93c9-120">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e93c9-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e93c9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e93c9-121">-ResourceGroupName</span></span>
<span data-ttu-id="e93c9-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e93c9-122">The name of the resource group.</span></span>
<span data-ttu-id="e93c9-123">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="e93c9-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e93c9-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e93c9-124">-SubscriptionId</span></span>
<span data-ttu-id="e93c9-125">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e93c9-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e93c9-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e93c9-126">-Confirm</span></span>
<span data-ttu-id="e93c9-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e93c9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e93c9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e93c9-128">-WhatIf</span></span>
<span data-ttu-id="e93c9-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e93c9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e93c9-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e93c9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e93c9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e93c9-131">CommonParameters</span></span>
<span data-ttu-id="e93c9-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e93c9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e93c9-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e93c9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e93c9-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e93c9-134">INPUTS</span></span>

### <span data-ttu-id="e93c9-135">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="e93c9-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="e93c9-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e93c9-136">OUTPUTS</span></span>

### <span data-ttu-id="e93c9-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e93c9-137">System.Boolean</span></span>

## <span data-ttu-id="e93c9-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="e93c9-138">NOTES</span></span>

<span data-ttu-id="e93c9-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="e93c9-139">ALIASES</span></span>

<span data-ttu-id="e93c9-140">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="e93c9-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e93c9-141">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e93c9-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e93c9-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e93c9-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e93c9-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="e93c9-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e93c9-144">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="e93c9-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="e93c9-145">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="e93c9-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="e93c9-146">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="e93c9-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="e93c9-147">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e93c9-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="e93c9-148">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="e93c9-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e93c9-149">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e93c9-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e93c9-150">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="e93c9-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="e93c9-151">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="e93c9-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="e93c9-152">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e93c9-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e93c9-153">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="e93c9-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="e93c9-154">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e93c9-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="e93c9-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e93c9-155">RELATED LINKS</span></span>

