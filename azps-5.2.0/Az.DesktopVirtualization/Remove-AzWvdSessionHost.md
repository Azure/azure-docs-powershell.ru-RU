---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: fa480a867cbbe93a756ea38b4534818ca119c098
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398548"
---
# <span data-ttu-id="5b60a-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="5b60a-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="5b60a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b60a-102">SYNOPSIS</span></span>
<span data-ttu-id="5b60a-103">Удалите SessionHost.</span><span class="sxs-lookup"><span data-stu-id="5b60a-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="5b60a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5b60a-104">SYNTAX</span></span>

### <span data-ttu-id="5b60a-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b60a-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5b60a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5b60a-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5b60a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b60a-107">DESCRIPTION</span></span>
<span data-ttu-id="5b60a-108">Удалите SessionHost.</span><span class="sxs-lookup"><span data-stu-id="5b60a-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="5b60a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5b60a-109">EXAMPLES</span></span>

### <span data-ttu-id="5b60a-110">Пример 1. Удаление виртуального рабочего стола Windows По имени</span><span class="sxs-lookup"><span data-stu-id="5b60a-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="5b60a-111">Эта команда удаляет виртуальный настольный сеанс Windows из пула хостов.</span><span class="sxs-lookup"><span data-stu-id="5b60a-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="5b60a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b60a-112">PARAMETERS</span></span>

### <span data-ttu-id="5b60a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b60a-113">-DefaultProfile</span></span>
<span data-ttu-id="5b60a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b60a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b60a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5b60a-115">-Force</span></span>
<span data-ttu-id="5b60a-116">Принудительное пометка для принудительного удаления sessionHost даже при существования userSession.</span><span class="sxs-lookup"><span data-stu-id="5b60a-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="5b60a-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="5b60a-117">-HostPoolName</span></span>
<span data-ttu-id="5b60a-118">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="5b60a-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="5b60a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b60a-119">-InputObject</span></span>
<span data-ttu-id="5b60a-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="5b60a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5b60a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5b60a-121">-Name</span></span>
<span data-ttu-id="5b60a-122">Имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="5b60a-122">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="5b60a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b60a-123">-PassThru</span></span>
<span data-ttu-id="5b60a-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="5b60a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5b60a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b60a-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b60a-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b60a-126">The name of the resource group.</span></span>
<span data-ttu-id="5b60a-127">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="5b60a-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5b60a-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b60a-128">-SubscriptionId</span></span>
<span data-ttu-id="5b60a-129">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="5b60a-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5b60a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b60a-130">-Confirm</span></span>
<span data-ttu-id="5b60a-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5b60a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b60a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b60a-132">-WhatIf</span></span>
<span data-ttu-id="5b60a-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b60a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b60a-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5b60a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b60a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b60a-135">CommonParameters</span></span>
<span data-ttu-id="5b60a-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b60a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b60a-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b60a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b60a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b60a-138">INPUTS</span></span>

### <span data-ttu-id="5b60a-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="5b60a-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5b60a-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5b60a-140">OUTPUTS</span></span>

### <span data-ttu-id="5b60a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5b60a-141">System.Boolean</span></span>

## <span data-ttu-id="5b60a-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5b60a-142">NOTES</span></span>

<span data-ttu-id="5b60a-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5b60a-143">ALIASES</span></span>

<span data-ttu-id="5b60a-144">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5b60a-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5b60a-145">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="5b60a-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5b60a-146">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5b60a-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5b60a-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="5b60a-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5b60a-148">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="5b60a-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5b60a-149">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="5b60a-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5b60a-150">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="5b60a-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5b60a-151">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="5b60a-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5b60a-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="5b60a-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5b60a-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="5b60a-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="5b60a-154">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b60a-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5b60a-155">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="5b60a-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="5b60a-156">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="5b60a-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5b60a-157">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="5b60a-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5b60a-158">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="5b60a-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5b60a-159">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="5b60a-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5b60a-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b60a-160">RELATED LINKS</span></span>

