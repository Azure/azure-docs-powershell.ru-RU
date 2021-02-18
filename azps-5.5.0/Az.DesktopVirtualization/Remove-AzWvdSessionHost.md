---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: fa480a867cbbe93a756ea38b4534818ca119c098
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214828"
---
# <span data-ttu-id="8a50d-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="8a50d-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="8a50d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a50d-102">SYNOPSIS</span></span>
<span data-ttu-id="8a50d-103">Удалите SessionHost.</span><span class="sxs-lookup"><span data-stu-id="8a50d-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="8a50d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8a50d-104">SYNTAX</span></span>

### <span data-ttu-id="8a50d-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8a50d-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8a50d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8a50d-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8a50d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a50d-107">DESCRIPTION</span></span>
<span data-ttu-id="8a50d-108">Удалить SessionHost.</span><span class="sxs-lookup"><span data-stu-id="8a50d-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="8a50d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8a50d-109">EXAMPLES</span></span>

### <span data-ttu-id="8a50d-110">Пример 1. Удаление виртуального рабочего стола Windows По имени</span><span class="sxs-lookup"><span data-stu-id="8a50d-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="8a50d-111">Эта команда удаляет виртуальный настольный сеанс Windows из пула хостов.</span><span class="sxs-lookup"><span data-stu-id="8a50d-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="8a50d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a50d-112">PARAMETERS</span></span>

### <span data-ttu-id="8a50d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a50d-113">-DefaultProfile</span></span>
<span data-ttu-id="8a50d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a50d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a50d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8a50d-115">-Force</span></span>
<span data-ttu-id="8a50d-116">Принудительное пометка для принудительного удаления sessionHost, даже если существует userSession.</span><span class="sxs-lookup"><span data-stu-id="8a50d-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="8a50d-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="8a50d-117">-HostPoolName</span></span>
<span data-ttu-id="8a50d-118">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="8a50d-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="8a50d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a50d-119">-InputObject</span></span>
<span data-ttu-id="8a50d-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="8a50d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8a50d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8a50d-121">-Name</span></span>
<span data-ttu-id="8a50d-122">Имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="8a50d-122">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="8a50d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a50d-123">-PassThru</span></span>
<span data-ttu-id="8a50d-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="8a50d-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8a50d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a50d-125">-ResourceGroupName</span></span>
<span data-ttu-id="8a50d-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a50d-126">The name of the resource group.</span></span>
<span data-ttu-id="8a50d-127">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="8a50d-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8a50d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a50d-128">-SubscriptionId</span></span>
<span data-ttu-id="8a50d-129">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="8a50d-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8a50d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a50d-130">-Confirm</span></span>
<span data-ttu-id="8a50d-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8a50d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a50d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a50d-132">-WhatIf</span></span>
<span data-ttu-id="8a50d-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a50d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a50d-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8a50d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a50d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a50d-135">CommonParameters</span></span>
<span data-ttu-id="8a50d-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a50d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a50d-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a50d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a50d-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a50d-138">INPUTS</span></span>

### <span data-ttu-id="8a50d-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="8a50d-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8a50d-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8a50d-140">OUTPUTS</span></span>

### <span data-ttu-id="8a50d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8a50d-141">System.Boolean</span></span>

## <span data-ttu-id="8a50d-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8a50d-142">NOTES</span></span>

<span data-ttu-id="8a50d-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8a50d-143">ALIASES</span></span>

<span data-ttu-id="8a50d-144">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="8a50d-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a50d-145">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="8a50d-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a50d-146">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a50d-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a50d-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="8a50d-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a50d-148">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="8a50d-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8a50d-149">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="8a50d-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8a50d-150">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="8a50d-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8a50d-151">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="8a50d-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8a50d-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="8a50d-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a50d-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="8a50d-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="8a50d-154">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a50d-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8a50d-155">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="8a50d-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="8a50d-156">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="8a50d-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8a50d-157">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="8a50d-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8a50d-158">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="8a50d-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8a50d-159">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="8a50d-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="8a50d-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a50d-160">RELATED LINKS</span></span>

