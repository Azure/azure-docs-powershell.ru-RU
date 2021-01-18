---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
ms.openlocfilehash: 59ff3c3bd973e3b2189e7f06cd067eaca42870f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507562"
---
# <span data-ttu-id="97e2d-101">Remove-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="97e2d-101">Remove-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="97e2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="97e2d-103">Удалите группу приложений.</span><span class="sxs-lookup"><span data-stu-id="97e2d-103">Remove an applicationGroup.</span></span>

## <span data-ttu-id="97e2d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="97e2d-104">SYNTAX</span></span>

### <span data-ttu-id="97e2d-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="97e2d-105">Delete (Default)</span></span>
```
Remove-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="97e2d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="97e2d-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="97e2d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97e2d-107">DESCRIPTION</span></span>
<span data-ttu-id="97e2d-108">Удалите группу приложений.</span><span class="sxs-lookup"><span data-stu-id="97e2d-108">Remove an applicationGroup.</span></span>

## <span data-ttu-id="97e2d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="97e2d-109">EXAMPLES</span></span>

### <span data-ttu-id="97e2d-110">Пример 1. Удаление группы приложений Виртуального рабочего стола Windows по имени</span><span class="sxs-lookup"><span data-stu-id="97e2d-110">Example 1: Delete a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName
```

<span data-ttu-id="97e2d-111">Эта команда удаляет группу приложений Виртуального рабочего стола Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97e2d-111">This command deletes a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="97e2d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97e2d-112">PARAMETERS</span></span>

### <span data-ttu-id="97e2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e2d-113">-DefaultProfile</span></span>
<span data-ttu-id="97e2d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97e2d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97e2d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97e2d-115">-InputObject</span></span>
<span data-ttu-id="97e2d-116">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="97e2d-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="97e2d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="97e2d-117">-Name</span></span>
<span data-ttu-id="97e2d-118">Имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="97e2d-118">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e2d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97e2d-119">-PassThru</span></span>
<span data-ttu-id="97e2d-120">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="97e2d-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="97e2d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97e2d-121">-ResourceGroupName</span></span>
<span data-ttu-id="97e2d-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97e2d-122">The name of the resource group.</span></span>
<span data-ttu-id="97e2d-123">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="97e2d-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="97e2d-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97e2d-124">-SubscriptionId</span></span>
<span data-ttu-id="97e2d-125">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="97e2d-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="97e2d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97e2d-126">-Confirm</span></span>
<span data-ttu-id="97e2d-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97e2d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97e2d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97e2d-128">-WhatIf</span></span>
<span data-ttu-id="97e2d-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97e2d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97e2d-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="97e2d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97e2d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e2d-131">CommonParameters</span></span>
<span data-ttu-id="97e2d-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97e2d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e2d-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97e2d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e2d-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97e2d-134">INPUTS</span></span>

### <span data-ttu-id="97e2d-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="97e2d-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="97e2d-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="97e2d-136">OUTPUTS</span></span>

### <span data-ttu-id="97e2d-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="97e2d-137">System.Boolean</span></span>

## <span data-ttu-id="97e2d-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="97e2d-138">NOTES</span></span>

<span data-ttu-id="97e2d-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="97e2d-139">ALIASES</span></span>

<span data-ttu-id="97e2d-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="97e2d-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="97e2d-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="97e2d-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97e2d-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97e2d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="97e2d-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="97e2d-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="97e2d-144">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="97e2d-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="97e2d-145">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="97e2d-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="97e2d-146">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="97e2d-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="97e2d-147">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="97e2d-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="97e2d-148">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="97e2d-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97e2d-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="97e2d-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="97e2d-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97e2d-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="97e2d-151">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="97e2d-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="97e2d-152">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="97e2d-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="97e2d-153">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="97e2d-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="97e2d-154">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="97e2d-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="97e2d-155">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="97e2d-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="97e2d-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97e2d-156">RELATED LINKS</span></span>

