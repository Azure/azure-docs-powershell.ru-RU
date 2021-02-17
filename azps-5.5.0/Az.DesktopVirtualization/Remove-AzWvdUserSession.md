---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: d460b3e10ccc0e2d37a4e2aeb208d0b9f8006a10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220108"
---
# <span data-ttu-id="45847-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="45847-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="45847-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45847-102">SYNOPSIS</span></span>
<span data-ttu-id="45847-103">Удаление userSession.</span><span class="sxs-lookup"><span data-stu-id="45847-103">Remove a userSession.</span></span>

## <span data-ttu-id="45847-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="45847-104">SYNTAX</span></span>

### <span data-ttu-id="45847-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45847-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="45847-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="45847-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="45847-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45847-107">DESCRIPTION</span></span>
<span data-ttu-id="45847-108">Удаление userSession.</span><span class="sxs-lookup"><span data-stu-id="45847-108">Remove a userSession.</span></span>

## <span data-ttu-id="45847-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="45847-109">EXAMPLES</span></span>

### <span data-ttu-id="45847-110">Пример 1. Удаление пользователя виртуального рабочего стола Windows по имени</span><span class="sxs-lookup"><span data-stu-id="45847-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="45847-111">Эта команда удаляет пользователя виртуального рабочего стола Windows на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="45847-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="45847-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45847-112">PARAMETERS</span></span>

### <span data-ttu-id="45847-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45847-113">-DefaultProfile</span></span>
<span data-ttu-id="45847-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45847-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45847-115">-Force</span><span class="sxs-lookup"><span data-stu-id="45847-115">-Force</span></span>
<span data-ttu-id="45847-116">Принудительное пометка для входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="45847-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="45847-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="45847-117">-HostPoolName</span></span>
<span data-ttu-id="45847-118">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="45847-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="45847-119">-Id</span><span class="sxs-lookup"><span data-stu-id="45847-119">-Id</span></span>
<span data-ttu-id="45847-120">Имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="45847-120">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45847-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45847-121">-InputObject</span></span>
<span data-ttu-id="45847-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="45847-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="45847-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45847-123">-PassThru</span></span>
<span data-ttu-id="45847-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="45847-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="45847-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45847-125">-ResourceGroupName</span></span>
<span data-ttu-id="45847-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45847-126">The name of the resource group.</span></span>
<span data-ttu-id="45847-127">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="45847-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="45847-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="45847-128">-SessionHostName</span></span>
<span data-ttu-id="45847-129">Имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="45847-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="45847-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45847-130">-SubscriptionId</span></span>
<span data-ttu-id="45847-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="45847-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="45847-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45847-132">-Confirm</span></span>
<span data-ttu-id="45847-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45847-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45847-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45847-134">-WhatIf</span></span>
<span data-ttu-id="45847-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45847-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45847-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="45847-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45847-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45847-137">CommonParameters</span></span>
<span data-ttu-id="45847-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45847-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45847-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45847-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45847-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45847-140">INPUTS</span></span>

### <span data-ttu-id="45847-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="45847-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="45847-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="45847-142">OUTPUTS</span></span>

### <span data-ttu-id="45847-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="45847-143">System.Boolean</span></span>

## <span data-ttu-id="45847-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="45847-144">NOTES</span></span>

<span data-ttu-id="45847-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="45847-145">ALIASES</span></span>

<span data-ttu-id="45847-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="45847-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="45847-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="45847-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="45847-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="45847-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="45847-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="45847-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="45847-150">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="45847-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="45847-151">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="45847-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="45847-152">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="45847-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="45847-153">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="45847-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="45847-154">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="45847-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="45847-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="45847-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="45847-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45847-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="45847-157">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="45847-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="45847-158">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="45847-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="45847-159">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="45847-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="45847-160">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="45847-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="45847-161">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="45847-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="45847-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45847-162">RELATED LINKS</span></span>

