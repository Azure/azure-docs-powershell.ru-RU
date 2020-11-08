---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: ec80e3382c401f9d64fb469c58a074ed47719ee9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245572"
---
# <span data-ttu-id="4b17c-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="4b17c-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="4b17c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b17c-102">SYNOPSIS</span></span>
<span data-ttu-id="4b17c-103">Обновите узел сеансов.</span><span class="sxs-lookup"><span data-stu-id="4b17c-103">Update a session host.</span></span>

## <span data-ttu-id="4b17c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b17c-104">SYNTAX</span></span>

### <span data-ttu-id="4b17c-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4b17c-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4b17c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4b17c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4b17c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b17c-107">DESCRIPTION</span></span>
<span data-ttu-id="4b17c-108">Обновите узел сеансов.</span><span class="sxs-lookup"><span data-stu-id="4b17c-108">Update a session host.</span></span>

## <span data-ttu-id="4b17c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b17c-109">EXAMPLES</span></span>

### <span data-ttu-id="4b17c-110">Пример 1: Обновление виртуального рабочего стола Windows SessionHost по имени</span><span class="sxs-lookup"><span data-stu-id="4b17c-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="4b17c-111">Эта команда обновляет SessionHost виртуальных рабочих столов Windows в пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="4b17c-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="4b17c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b17c-112">PARAMETERS</span></span>

### <span data-ttu-id="4b17c-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="4b17c-113">-AllowNewSession</span></span>
<span data-ttu-id="4b17c-114">Разрешите новый сеанс.</span><span class="sxs-lookup"><span data-stu-id="4b17c-114">Allow a new session.</span></span>

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

### <span data-ttu-id="4b17c-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="4b17c-115">-AssignedUser</span></span>
<span data-ttu-id="4b17c-116">Пользователь, назначенный SessionHost.</span><span class="sxs-lookup"><span data-stu-id="4b17c-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="4b17c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b17c-117">-DefaultProfile</span></span>
<span data-ttu-id="4b17c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b17c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b17c-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="4b17c-119">-HostPoolName</span></span>
<span data-ttu-id="4b17c-120">Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b17c-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="4b17c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b17c-121">-InputObject</span></span>
<span data-ttu-id="4b17c-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="4b17c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4b17c-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4b17c-123">-Name</span></span>
<span data-ttu-id="4b17c-124">Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="4b17c-124">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b17c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b17c-125">-ResourceGroupName</span></span>
<span data-ttu-id="4b17c-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b17c-126">The name of the resource group.</span></span>
<span data-ttu-id="4b17c-127">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="4b17c-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4b17c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b17c-128">-SubscriptionId</span></span>
<span data-ttu-id="4b17c-129">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="4b17c-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4b17c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b17c-130">-Confirm</span></span>
<span data-ttu-id="4b17c-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4b17c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b17c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b17c-132">-WhatIf</span></span>
<span data-ttu-id="4b17c-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4b17c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b17c-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4b17c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b17c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b17c-135">CommonParameters</span></span>
<span data-ttu-id="4b17c-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b17c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b17c-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b17c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b17c-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b17c-138">INPUTS</span></span>

### <span data-ttu-id="4b17c-139">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="4b17c-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4b17c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b17c-140">OUTPUTS</span></span>

### <span data-ttu-id="4b17c-141">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. ISessionHost</span><span class="sxs-lookup"><span data-stu-id="4b17c-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="4b17c-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b17c-142">NOTES</span></span>

<span data-ttu-id="4b17c-143">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="4b17c-143">ALIASES</span></span>

<span data-ttu-id="4b17c-144">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4b17c-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4b17c-145">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4b17c-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4b17c-146">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4b17c-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4b17c-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="4b17c-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4b17c-148">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="4b17c-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4b17c-149">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="4b17c-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4b17c-150">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="4b17c-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4b17c-151">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b17c-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4b17c-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="4b17c-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4b17c-153">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b17c-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4b17c-154">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="4b17c-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="4b17c-155">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="4b17c-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4b17c-156">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="4b17c-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4b17c-157">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="4b17c-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4b17c-158">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="4b17c-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4b17c-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b17c-159">RELATED LINKS</span></span>

