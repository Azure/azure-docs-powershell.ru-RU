---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
ms.openlocfilehash: 682f59c5c07643ecd93fd1ae051abc8e74c4e185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980483"
---
# <span data-ttu-id="dc66c-101">Remove-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="dc66c-101">Remove-AzWvdWorkspace</span></span>

## <span data-ttu-id="dc66c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc66c-102">SYNOPSIS</span></span>
<span data-ttu-id="dc66c-103">Удаление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="dc66c-103">Remove a workspace.</span></span>

## <span data-ttu-id="dc66c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dc66c-104">SYNTAX</span></span>

### <span data-ttu-id="dc66c-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc66c-105">Delete (Default)</span></span>
```
Remove-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dc66c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dc66c-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dc66c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc66c-107">DESCRIPTION</span></span>
<span data-ttu-id="dc66c-108">Удаление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="dc66c-108">Remove a workspace.</span></span>

## <span data-ttu-id="dc66c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dc66c-109">EXAMPLES</span></span>

### <span data-ttu-id="dc66c-110">Пример 1. Удаление рабочей области виртуального рабочего стола Windows по имени</span><span class="sxs-lookup"><span data-stu-id="dc66c-110">Example 1: Delete a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Remove-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName
```

<span data-ttu-id="dc66c-111">Эта команда удаляет рабочее пространство Виртуального рабочего стола Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc66c-111">This command deletes a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="dc66c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc66c-112">PARAMETERS</span></span>

### <span data-ttu-id="dc66c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc66c-113">-DefaultProfile</span></span>
<span data-ttu-id="dc66c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc66c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc66c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc66c-115">-InputObject</span></span>
<span data-ttu-id="dc66c-116">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="dc66c-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dc66c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="dc66c-117">-Name</span></span>
<span data-ttu-id="dc66c-118">Имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="dc66c-118">The name of the workspace</span></span>

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

### <span data-ttu-id="dc66c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc66c-119">-PassThru</span></span>
<span data-ttu-id="dc66c-120">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="dc66c-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dc66c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc66c-121">-ResourceGroupName</span></span>
<span data-ttu-id="dc66c-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc66c-122">The name of the resource group.</span></span>
<span data-ttu-id="dc66c-123">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="dc66c-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dc66c-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc66c-124">-SubscriptionId</span></span>
<span data-ttu-id="dc66c-125">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="dc66c-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dc66c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc66c-126">-Confirm</span></span>
<span data-ttu-id="dc66c-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc66c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc66c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc66c-128">-WhatIf</span></span>
<span data-ttu-id="dc66c-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc66c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc66c-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dc66c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc66c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc66c-131">CommonParameters</span></span>
<span data-ttu-id="dc66c-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc66c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc66c-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc66c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc66c-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc66c-134">INPUTS</span></span>

### <span data-ttu-id="dc66c-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="dc66c-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="dc66c-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dc66c-136">OUTPUTS</span></span>

### <span data-ttu-id="dc66c-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dc66c-137">System.Boolean</span></span>

## <span data-ttu-id="dc66c-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dc66c-138">NOTES</span></span>

<span data-ttu-id="dc66c-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="dc66c-139">ALIASES</span></span>

<span data-ttu-id="dc66c-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="dc66c-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dc66c-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="dc66c-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc66c-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dc66c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dc66c-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="dc66c-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dc66c-144">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="dc66c-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="dc66c-145">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="dc66c-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="dc66c-146">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="dc66c-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="dc66c-147">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="dc66c-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="dc66c-148">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="dc66c-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc66c-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="dc66c-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="dc66c-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc66c-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dc66c-151">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="dc66c-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="dc66c-152">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="dc66c-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="dc66c-153">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="dc66c-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dc66c-154">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="dc66c-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="dc66c-155">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="dc66c-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="dc66c-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc66c-156">RELATED LINKS</span></span>

