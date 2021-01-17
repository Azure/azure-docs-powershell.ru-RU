---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: 016719f32af1af9acdc4543d565f9acc086b05fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393476"
---
# <span data-ttu-id="765c9-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="765c9-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="765c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="765c9-102">SYNOPSIS</span></span>
<span data-ttu-id="765c9-103">Отключить userSession.</span><span class="sxs-lookup"><span data-stu-id="765c9-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="765c9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="765c9-104">SYNTAX</span></span>

### <span data-ttu-id="765c9-105">Отключить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="765c9-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="765c9-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="765c9-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="765c9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="765c9-107">DESCRIPTION</span></span>
<span data-ttu-id="765c9-108">Отключить userSession.</span><span class="sxs-lookup"><span data-stu-id="765c9-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="765c9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="765c9-109">EXAMPLES</span></span>

### <span data-ttu-id="765c9-110">Пример 1. Отключение пользователя userSession виртуального рабочего стола Windows по имени</span><span class="sxs-lookup"><span data-stu-id="765c9-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="765c9-111">Эта команда отключает userSession виртуального рабочего стола Windows на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="765c9-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="765c9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="765c9-112">PARAMETERS</span></span>

### <span data-ttu-id="765c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="765c9-113">-DefaultProfile</span></span>
<span data-ttu-id="765c9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="765c9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="765c9-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="765c9-115">-HostPoolName</span></span>
<span data-ttu-id="765c9-116">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="765c9-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765c9-117">-Id</span><span class="sxs-lookup"><span data-stu-id="765c9-117">-Id</span></span>
<span data-ttu-id="765c9-118">Имя сеанса пользователя в заданном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="765c9-118">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765c9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="765c9-119">-InputObject</span></span>
<span data-ttu-id="765c9-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="765c9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DisconnectViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="765c9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="765c9-121">-PassThru</span></span>
<span data-ttu-id="765c9-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="765c9-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="765c9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="765c9-123">-ResourceGroupName</span></span>
<span data-ttu-id="765c9-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="765c9-124">The name of the resource group.</span></span>
<span data-ttu-id="765c9-125">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="765c9-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765c9-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="765c9-126">-SessionHostName</span></span>
<span data-ttu-id="765c9-127">Имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="765c9-127">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765c9-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="765c9-128">-SubscriptionId</span></span>
<span data-ttu-id="765c9-129">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="765c9-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="765c9-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="765c9-130">-Confirm</span></span>
<span data-ttu-id="765c9-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="765c9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="765c9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="765c9-132">-WhatIf</span></span>
<span data-ttu-id="765c9-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="765c9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="765c9-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="765c9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="765c9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="765c9-135">CommonParameters</span></span>
<span data-ttu-id="765c9-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="765c9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="765c9-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="765c9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="765c9-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="765c9-138">INPUTS</span></span>

### <span data-ttu-id="765c9-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="765c9-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="765c9-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="765c9-140">OUTPUTS</span></span>

### <span data-ttu-id="765c9-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="765c9-141">System.Boolean</span></span>

## <span data-ttu-id="765c9-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="765c9-142">NOTES</span></span>

<span data-ttu-id="765c9-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="765c9-143">ALIASES</span></span>

<span data-ttu-id="765c9-144">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="765c9-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="765c9-145">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="765c9-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="765c9-146">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="765c9-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="765c9-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="765c9-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="765c9-148">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="765c9-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="765c9-149">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="765c9-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="765c9-150">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="765c9-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="765c9-151">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="765c9-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="765c9-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="765c9-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="765c9-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="765c9-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="765c9-154">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="765c9-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="765c9-155">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="765c9-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="765c9-156">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="765c9-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="765c9-157">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="765c9-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="765c9-158">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="765c9-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="765c9-159">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="765c9-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="765c9-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="765c9-160">RELATED LINKS</span></span>

