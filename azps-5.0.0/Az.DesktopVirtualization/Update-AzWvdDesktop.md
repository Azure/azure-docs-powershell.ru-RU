---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: 7aec3e71e65c20810d8a17e8f7fa14df3c69f577
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247479"
---
# <span data-ttu-id="75055-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="75055-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="75055-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75055-102">SYNOPSIS</span></span>
<span data-ttu-id="75055-103">Обновление рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="75055-103">Update a desktop.</span></span>

## <span data-ttu-id="75055-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75055-104">SYNTAX</span></span>

### <span data-ttu-id="75055-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75055-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="75055-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="75055-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="75055-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75055-107">DESCRIPTION</span></span>
<span data-ttu-id="75055-108">Обновление рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="75055-108">Update a desktop.</span></span>

## <span data-ttu-id="75055-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75055-109">EXAMPLES</span></span>

### <span data-ttu-id="75055-110">Пример 1: обновление рабочего стола Windows для виртуальных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="75055-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
```powershell
PS C:\> Update-AzWvdDesktop -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name DesktopName `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="75055-111">Эта команда обновляет рабочий стол виртуальных рабочих столов Windows в группе applicaton.</span><span class="sxs-lookup"><span data-stu-id="75055-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="75055-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75055-112">PARAMETERS</span></span>

### <span data-ttu-id="75055-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="75055-113">-ApplicationGroupName</span></span>
<span data-ttu-id="75055-114">Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="75055-114">The name of the application group</span></span>

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

### <span data-ttu-id="75055-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75055-115">-DefaultProfile</span></span>
<span data-ttu-id="75055-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75055-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75055-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="75055-117">-Description</span></span>
<span data-ttu-id="75055-118">Описание рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="75055-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="75055-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="75055-119">-FriendlyName</span></span>
<span data-ttu-id="75055-120">Понятное имя рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="75055-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="75055-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75055-121">-InputObject</span></span>
<span data-ttu-id="75055-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="75055-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="75055-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="75055-123">-Name</span></span>
<span data-ttu-id="75055-124">Имя рабочего стола в пределах указанной группы рабочего стола</span><span class="sxs-lookup"><span data-stu-id="75055-124">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75055-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75055-125">-ResourceGroupName</span></span>
<span data-ttu-id="75055-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75055-126">The name of the resource group.</span></span>
<span data-ttu-id="75055-127">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="75055-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="75055-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75055-128">-SubscriptionId</span></span>
<span data-ttu-id="75055-129">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="75055-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="75055-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="75055-130">-Tag</span></span>
<span data-ttu-id="75055-131">Теги для обновления</span><span class="sxs-lookup"><span data-stu-id="75055-131">tags to be updated</span></span>

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

### <span data-ttu-id="75055-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75055-132">-Confirm</span></span>
<span data-ttu-id="75055-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75055-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75055-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75055-134">-WhatIf</span></span>
<span data-ttu-id="75055-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75055-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75055-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75055-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75055-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75055-137">CommonParameters</span></span>
<span data-ttu-id="75055-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75055-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75055-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75055-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75055-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75055-140">INPUTS</span></span>

### <span data-ttu-id="75055-141">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="75055-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="75055-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75055-142">OUTPUTS</span></span>

### <span data-ttu-id="75055-143">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IDesktop</span><span class="sxs-lookup"><span data-stu-id="75055-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

## <span data-ttu-id="75055-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="75055-144">NOTES</span></span>

<span data-ttu-id="75055-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="75055-145">ALIASES</span></span>

<span data-ttu-id="75055-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="75055-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="75055-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="75055-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="75055-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="75055-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="75055-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="75055-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="75055-150">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="75055-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="75055-151">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="75055-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="75055-152">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="75055-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="75055-153">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75055-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="75055-154">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="75055-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="75055-155">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75055-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="75055-156">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="75055-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="75055-157">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="75055-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="75055-158">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="75055-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="75055-159">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="75055-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="75055-160">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="75055-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="75055-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75055-161">RELATED LINKS</span></span>

