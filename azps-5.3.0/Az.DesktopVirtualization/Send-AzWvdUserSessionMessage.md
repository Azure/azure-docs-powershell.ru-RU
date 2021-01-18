---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 5b5e5ba314bee8d6260985c65f46d372cce94258
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506363"
---
# <span data-ttu-id="e5047-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="e5047-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="e5047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5047-102">SYNOPSIS</span></span>
<span data-ttu-id="e5047-103">Отправка сообщения пользователю.</span><span class="sxs-lookup"><span data-stu-id="e5047-103">Send a message to a user.</span></span>

## <span data-ttu-id="e5047-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5047-104">SYNTAX</span></span>

### <span data-ttu-id="e5047-105">SendExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5047-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e5047-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e5047-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e5047-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5047-107">DESCRIPTION</span></span>
<span data-ttu-id="e5047-108">Отправка сообщения пользователю.</span><span class="sxs-lookup"><span data-stu-id="e5047-108">Send a message to a user.</span></span>

## <span data-ttu-id="e5047-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5047-109">EXAMPLES</span></span>

### <span data-ttu-id="e5047-110">Пример 1. Отправка сообщения пользователю UserSession</span><span class="sxs-lookup"><span data-stu-id="e5047-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="e5047-111">Эта команда отправляет сообщение пользователю UserSession.</span><span class="sxs-lookup"><span data-stu-id="e5047-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="e5047-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5047-112">PARAMETERS</span></span>

### <span data-ttu-id="e5047-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5047-113">-DefaultProfile</span></span>
<span data-ttu-id="e5047-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5047-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5047-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="e5047-115">-HostPoolName</span></span>
<span data-ttu-id="e5047-116">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="e5047-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5047-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5047-117">-InputObject</span></span>
<span data-ttu-id="e5047-118">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="e5047-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: SendViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5047-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="e5047-119">-MessageBody</span></span>
<span data-ttu-id="e5047-120">Текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="e5047-120">Body of message.</span></span>

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

### <span data-ttu-id="e5047-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="e5047-121">-MessageTitle</span></span>
<span data-ttu-id="e5047-122">Название сообщения.</span><span class="sxs-lookup"><span data-stu-id="e5047-122">Title of message.</span></span>

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

### <span data-ttu-id="e5047-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5047-123">-PassThru</span></span>
<span data-ttu-id="e5047-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="e5047-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e5047-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5047-125">-ResourceGroupName</span></span>
<span data-ttu-id="e5047-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5047-126">The name of the resource group.</span></span>
<span data-ttu-id="e5047-127">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="e5047-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5047-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="e5047-128">-SessionHostName</span></span>
<span data-ttu-id="e5047-129">Имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="e5047-129">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5047-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5047-130">-SubscriptionId</span></span>
<span data-ttu-id="e5047-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e5047-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5047-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="e5047-132">-UserSessionId</span></span>
<span data-ttu-id="e5047-133">Имя сеанса пользователя в заданном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="e5047-133">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5047-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5047-134">-Confirm</span></span>
<span data-ttu-id="e5047-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5047-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5047-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5047-136">-WhatIf</span></span>
<span data-ttu-id="e5047-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5047-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5047-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e5047-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5047-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5047-139">CommonParameters</span></span>
<span data-ttu-id="e5047-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5047-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5047-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5047-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5047-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5047-142">INPUTS</span></span>

### <span data-ttu-id="e5047-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="e5047-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="e5047-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5047-144">OUTPUTS</span></span>

### <span data-ttu-id="e5047-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e5047-145">System.Boolean</span></span>

## <span data-ttu-id="e5047-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5047-146">NOTES</span></span>

<span data-ttu-id="e5047-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e5047-147">ALIASES</span></span>

<span data-ttu-id="e5047-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="e5047-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e5047-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="e5047-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e5047-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e5047-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e5047-151">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="e5047-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e5047-152">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="e5047-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="e5047-153">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="e5047-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="e5047-154">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="e5047-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="e5047-155">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="e5047-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="e5047-156">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="e5047-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e5047-157">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="e5047-157">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="e5047-158">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5047-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e5047-159">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="e5047-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="e5047-160">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="e5047-160">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="e5047-161">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e5047-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e5047-162">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="e5047-162">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="e5047-163">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="e5047-163">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="e5047-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5047-164">RELATED LINKS</span></span>

