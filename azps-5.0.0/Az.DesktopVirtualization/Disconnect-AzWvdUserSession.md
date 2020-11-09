---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: f4156fdc52ffaf01caad49517229ebf63d960fc6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312614"
---
# <span data-ttu-id="335f1-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="335f1-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="335f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="335f1-102">SYNOPSIS</span></span>
<span data-ttu-id="335f1-103">Отключение userSession.</span><span class="sxs-lookup"><span data-stu-id="335f1-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="335f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="335f1-104">SYNTAX</span></span>

### <span data-ttu-id="335f1-105">Отключить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="335f1-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="335f1-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="335f1-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="335f1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="335f1-107">DESCRIPTION</span></span>
<span data-ttu-id="335f1-108">Отключение userSession.</span><span class="sxs-lookup"><span data-stu-id="335f1-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="335f1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="335f1-109">EXAMPLES</span></span>

### <span data-ttu-id="335f1-110">Пример 1: Отключение виртуального рабочего стола Windows UserSession по имени</span><span class="sxs-lookup"><span data-stu-id="335f1-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="335f1-111">Эта команда отключает UserSession виртуальных рабочих столов Windows на узле сеансов.</span><span class="sxs-lookup"><span data-stu-id="335f1-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="335f1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="335f1-112">PARAMETERS</span></span>

### <span data-ttu-id="335f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="335f1-113">-DefaultProfile</span></span>
<span data-ttu-id="335f1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="335f1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="335f1-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="335f1-115">-HostPoolName</span></span>
<span data-ttu-id="335f1-116">Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="335f1-116">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="335f1-117">-ID</span><span class="sxs-lookup"><span data-stu-id="335f1-117">-Id</span></span>
<span data-ttu-id="335f1-118">Имя сеанса пользователя на указанном узле сеанса</span><span class="sxs-lookup"><span data-stu-id="335f1-118">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="335f1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="335f1-119">-InputObject</span></span>
<span data-ttu-id="335f1-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="335f1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="335f1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="335f1-121">-PassThru</span></span>
<span data-ttu-id="335f1-122">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="335f1-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="335f1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="335f1-123">-ResourceGroupName</span></span>
<span data-ttu-id="335f1-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="335f1-124">The name of the resource group.</span></span>
<span data-ttu-id="335f1-125">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="335f1-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="335f1-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="335f1-126">-SessionHostName</span></span>
<span data-ttu-id="335f1-127">Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="335f1-127">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="335f1-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="335f1-128">-SubscriptionId</span></span>
<span data-ttu-id="335f1-129">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="335f1-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="335f1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="335f1-130">-Confirm</span></span>
<span data-ttu-id="335f1-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="335f1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="335f1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="335f1-132">-WhatIf</span></span>
<span data-ttu-id="335f1-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="335f1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="335f1-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="335f1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="335f1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="335f1-135">CommonParameters</span></span>
<span data-ttu-id="335f1-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="335f1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="335f1-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="335f1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="335f1-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="335f1-138">INPUTS</span></span>

### <span data-ttu-id="335f1-139">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="335f1-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="335f1-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="335f1-140">OUTPUTS</span></span>

### <span data-ttu-id="335f1-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="335f1-141">System.Boolean</span></span>

## <span data-ttu-id="335f1-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="335f1-142">NOTES</span></span>

<span data-ttu-id="335f1-143">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="335f1-143">ALIASES</span></span>

<span data-ttu-id="335f1-144">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="335f1-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="335f1-145">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="335f1-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="335f1-146">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="335f1-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="335f1-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="335f1-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="335f1-148">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="335f1-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="335f1-149">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="335f1-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="335f1-150">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="335f1-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="335f1-151">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="335f1-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="335f1-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="335f1-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="335f1-153">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="335f1-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="335f1-154">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="335f1-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="335f1-155">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="335f1-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="335f1-156">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="335f1-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="335f1-157">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="335f1-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="335f1-158">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="335f1-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="335f1-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="335f1-159">RELATED LINKS</span></span>

