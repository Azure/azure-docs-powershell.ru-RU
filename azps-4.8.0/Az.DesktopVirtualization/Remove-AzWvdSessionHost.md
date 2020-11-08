---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: f7bad3a88f4d182407a90a2484daed3d538e3a69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244550"
---
# <span data-ttu-id="b8ccd-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="b8ccd-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="b8ccd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ccd-103">Удаление SessionHost.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="b8ccd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8ccd-104">SYNTAX</span></span>

### <span data-ttu-id="b8ccd-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8ccd-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b8ccd-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b8ccd-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b8ccd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8ccd-107">DESCRIPTION</span></span>
<span data-ttu-id="b8ccd-108">Удаление SessionHost.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="b8ccd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8ccd-109">EXAMPLES</span></span>

### <span data-ttu-id="b8ccd-110">Пример 1: Удаление виртуального рабочего стола Windows SessionHost по имени</span><span class="sxs-lookup"><span data-stu-id="b8ccd-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="b8ccd-111">Эта команда удаляет SessionHost виртуальных рабочих столов Windows в пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="b8ccd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8ccd-112">PARAMETERS</span></span>

### <span data-ttu-id="b8ccd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ccd-113">-DefaultProfile</span></span>
<span data-ttu-id="b8ccd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8ccd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b8ccd-115">-Force</span></span>
<span data-ttu-id="b8ccd-116">Принудительная установка принудительного удаления sessionHost, даже если userSession существует.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="b8ccd-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="b8ccd-117">-HostPoolName</span></span>
<span data-ttu-id="b8ccd-118">Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="b8ccd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8ccd-119">-InputObject</span></span>
<span data-ttu-id="b8ccd-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b8ccd-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8ccd-121">-Name</span></span>
<span data-ttu-id="b8ccd-122">Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-122">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ccd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8ccd-123">-PassThru</span></span>
<span data-ttu-id="b8ccd-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b8ccd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8ccd-125">-ResourceGroupName</span></span>
<span data-ttu-id="b8ccd-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-126">The name of the resource group.</span></span>
<span data-ttu-id="b8ccd-127">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b8ccd-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8ccd-128">-SubscriptionId</span></span>
<span data-ttu-id="b8ccd-129">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b8ccd-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8ccd-130">-Confirm</span></span>
<span data-ttu-id="b8ccd-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8ccd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8ccd-132">-WhatIf</span></span>
<span data-ttu-id="b8ccd-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8ccd-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8ccd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ccd-135">CommonParameters</span></span>
<span data-ttu-id="b8ccd-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ccd-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8ccd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ccd-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8ccd-138">INPUTS</span></span>

### <span data-ttu-id="b8ccd-139">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b8ccd-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b8ccd-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8ccd-140">OUTPUTS</span></span>

### <span data-ttu-id="b8ccd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8ccd-141">System.Boolean</span></span>

## <span data-ttu-id="b8ccd-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8ccd-142">NOTES</span></span>

<span data-ttu-id="b8ccd-143">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="b8ccd-143">ALIASES</span></span>

<span data-ttu-id="b8ccd-144">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b8ccd-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b8ccd-145">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b8ccd-146">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b8ccd-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="b8ccd-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b8ccd-148">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b8ccd-149">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b8ccd-150">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b8ccd-151">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b8ccd-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="b8ccd-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b8ccd-153">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b8ccd-154">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="b8ccd-155">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b8ccd-156">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b8ccd-157">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="b8ccd-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b8ccd-158">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b8ccd-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b8ccd-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8ccd-159">RELATED LINKS</span></span>

