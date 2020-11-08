---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 30c0734656b79f532c56b47b64e9d7e918f92fa8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077789"
---
# <span data-ttu-id="75d05-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="75d05-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="75d05-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75d05-102">SYNOPSIS</span></span>
<span data-ttu-id="75d05-103">Обновление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="75d05-103">Update a workspace.</span></span>

## <span data-ttu-id="75d05-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75d05-104">SYNTAX</span></span>

### <span data-ttu-id="75d05-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75d05-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="75d05-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="75d05-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="75d05-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75d05-107">DESCRIPTION</span></span>
<span data-ttu-id="75d05-108">Обновление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="75d05-108">Update a workspace.</span></span>

## <span data-ttu-id="75d05-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75d05-109">EXAMPLES</span></span>

### <span data-ttu-id="75d05-110">Пример 1: Обновление виртуального рабочего стола Windows Worksapce по имени</span><span class="sxs-lookup"><span data-stu-id="75d05-110">Example 1: Update a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> Update-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="75d05-111">Эта команда обновляет рабочую область виртуальных рабочих столов Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75d05-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="75d05-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75d05-112">PARAMETERS</span></span>

### <span data-ttu-id="75d05-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="75d05-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="75d05-114">Список ссылок applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="75d05-114">List of applicationGroup links.</span></span>

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

### <span data-ttu-id="75d05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d05-115">-DefaultProfile</span></span>
<span data-ttu-id="75d05-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75d05-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75d05-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="75d05-117">-Description</span></span>
<span data-ttu-id="75d05-118">Описание рабочей области.</span><span class="sxs-lookup"><span data-stu-id="75d05-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="75d05-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="75d05-119">-FriendlyName</span></span>
<span data-ttu-id="75d05-120">Понятное имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="75d05-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="75d05-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75d05-121">-InputObject</span></span>
<span data-ttu-id="75d05-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="75d05-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75d05-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="75d05-123">-Name</span></span>
<span data-ttu-id="75d05-124">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="75d05-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d05-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d05-125">-ResourceGroupName</span></span>
<span data-ttu-id="75d05-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75d05-126">The name of the resource group.</span></span>
<span data-ttu-id="75d05-127">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="75d05-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="75d05-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75d05-128">-SubscriptionId</span></span>
<span data-ttu-id="75d05-129">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="75d05-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="75d05-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="75d05-130">-Tag</span></span>
<span data-ttu-id="75d05-131">Теги для обновления</span><span class="sxs-lookup"><span data-stu-id="75d05-131">tags to be updated</span></span>

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

### <span data-ttu-id="75d05-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75d05-132">-Confirm</span></span>
<span data-ttu-id="75d05-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75d05-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75d05-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75d05-134">-WhatIf</span></span>
<span data-ttu-id="75d05-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75d05-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75d05-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75d05-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75d05-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d05-137">CommonParameters</span></span>
<span data-ttu-id="75d05-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75d05-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d05-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75d05-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d05-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75d05-140">INPUTS</span></span>

### <span data-ttu-id="75d05-141">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="75d05-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="75d05-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75d05-142">OUTPUTS</span></span>

### <span data-ttu-id="75d05-143">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="75d05-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="75d05-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="75d05-144">NOTES</span></span>

<span data-ttu-id="75d05-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="75d05-145">ALIASES</span></span>

<span data-ttu-id="75d05-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="75d05-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="75d05-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="75d05-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="75d05-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="75d05-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="75d05-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="75d05-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="75d05-150">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="75d05-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="75d05-151">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="75d05-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="75d05-152">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="75d05-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="75d05-153">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75d05-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="75d05-154">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="75d05-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="75d05-155">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75d05-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="75d05-156">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="75d05-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="75d05-157">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="75d05-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="75d05-158">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="75d05-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="75d05-159">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="75d05-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="75d05-160">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="75d05-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="75d05-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75d05-161">RELATED LINKS</span></span>

