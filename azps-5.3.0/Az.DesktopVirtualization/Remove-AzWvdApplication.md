---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
ms.openlocfilehash: c65fd55599a78bbaa558ba7ec8efa94fdc3b40e2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506367"
---
# <span data-ttu-id="8649f-101">Remove-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="8649f-101">Remove-AzWvdApplication</span></span>

## <span data-ttu-id="8649f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8649f-102">SYNOPSIS</span></span>
<span data-ttu-id="8649f-103">Удаление приложения.</span><span class="sxs-lookup"><span data-stu-id="8649f-103">Remove an application.</span></span>

## <span data-ttu-id="8649f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8649f-104">SYNTAX</span></span>

### <span data-ttu-id="8649f-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8649f-105">Delete (Default)</span></span>
```
Remove-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8649f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8649f-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8649f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8649f-107">DESCRIPTION</span></span>
<span data-ttu-id="8649f-108">Удаление приложения.</span><span class="sxs-lookup"><span data-stu-id="8649f-108">Remove an application.</span></span>

## <span data-ttu-id="8649f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8649f-109">EXAMPLES</span></span>

### <span data-ttu-id="8649f-110">Пример 1. Удаление приложения виртуального рабочего стола Windows по имени</span><span class="sxs-lookup"><span data-stu-id="8649f-110">Example 1: Delete a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName
```

<span data-ttu-id="8649f-111">Эта команда удаляет приложение Виртуального рабочего стола Windows из соответствующей группы.</span><span class="sxs-lookup"><span data-stu-id="8649f-111">This command deletes a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="8649f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8649f-112">PARAMETERS</span></span>

### <span data-ttu-id="8649f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8649f-113">-DefaultProfile</span></span>
<span data-ttu-id="8649f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8649f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8649f-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="8649f-115">-GroupName</span></span>
<span data-ttu-id="8649f-116">Имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="8649f-116">The name of the application group</span></span>

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

### <span data-ttu-id="8649f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8649f-117">-InputObject</span></span>
<span data-ttu-id="8649f-118">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="8649f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8649f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8649f-119">-Name</span></span>
<span data-ttu-id="8649f-120">Имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="8649f-120">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8649f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8649f-121">-PassThru</span></span>
<span data-ttu-id="8649f-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="8649f-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8649f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8649f-123">-ResourceGroupName</span></span>
<span data-ttu-id="8649f-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8649f-124">The name of the resource group.</span></span>
<span data-ttu-id="8649f-125">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="8649f-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8649f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8649f-126">-SubscriptionId</span></span>
<span data-ttu-id="8649f-127">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="8649f-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8649f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8649f-128">-Confirm</span></span>
<span data-ttu-id="8649f-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8649f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8649f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8649f-130">-WhatIf</span></span>
<span data-ttu-id="8649f-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8649f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8649f-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8649f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8649f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8649f-133">CommonParameters</span></span>
<span data-ttu-id="8649f-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8649f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8649f-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8649f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8649f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8649f-136">INPUTS</span></span>

### <span data-ttu-id="8649f-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="8649f-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8649f-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8649f-138">OUTPUTS</span></span>

### <span data-ttu-id="8649f-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8649f-139">System.Boolean</span></span>

## <span data-ttu-id="8649f-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8649f-140">NOTES</span></span>

<span data-ttu-id="8649f-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8649f-141">ALIASES</span></span>

<span data-ttu-id="8649f-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="8649f-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8649f-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="8649f-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8649f-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8649f-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8649f-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="8649f-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8649f-146">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="8649f-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8649f-147">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="8649f-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8649f-148">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="8649f-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8649f-149">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="8649f-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8649f-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="8649f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8649f-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="8649f-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="8649f-152">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8649f-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8649f-153">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="8649f-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="8649f-154">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="8649f-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8649f-155">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="8649f-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8649f-156">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="8649f-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8649f-157">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="8649f-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="8649f-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8649f-158">RELATED LINKS</span></span>

