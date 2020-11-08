---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: da00f15a43b74cbdbc516b86da442f0777775627
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236727"
---
# <span data-ttu-id="03acc-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="03acc-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="03acc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03acc-102">SYNOPSIS</span></span>
<span data-ttu-id="03acc-103">Удаление userSession.</span><span class="sxs-lookup"><span data-stu-id="03acc-103">Remove a userSession.</span></span>

## <span data-ttu-id="03acc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03acc-104">SYNTAX</span></span>

### <span data-ttu-id="03acc-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="03acc-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="03acc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="03acc-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="03acc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03acc-107">DESCRIPTION</span></span>
<span data-ttu-id="03acc-108">Удаление userSession.</span><span class="sxs-lookup"><span data-stu-id="03acc-108">Remove a userSession.</span></span>

## <span data-ttu-id="03acc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03acc-109">EXAMPLES</span></span>

### <span data-ttu-id="03acc-110">Пример 1: Удаление виртуального рабочего стола Windows UserSession по имени</span><span class="sxs-lookup"><span data-stu-id="03acc-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="03acc-111">Эта команда удаляет UserSession виртуальных рабочих столов Windows на узле сеансов.</span><span class="sxs-lookup"><span data-stu-id="03acc-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="03acc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03acc-112">PARAMETERS</span></span>

### <span data-ttu-id="03acc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03acc-113">-DefaultProfile</span></span>
<span data-ttu-id="03acc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="03acc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03acc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="03acc-115">-Force</span></span>
<span data-ttu-id="03acc-116">Принудительная Пометка для входа в userSession.</span><span class="sxs-lookup"><span data-stu-id="03acc-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="03acc-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="03acc-117">-HostPoolName</span></span>
<span data-ttu-id="03acc-118">Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="03acc-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="03acc-119">-ID</span><span class="sxs-lookup"><span data-stu-id="03acc-119">-Id</span></span>
<span data-ttu-id="03acc-120">Имя сеанса пользователя на указанном узле сеанса</span><span class="sxs-lookup"><span data-stu-id="03acc-120">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="03acc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03acc-121">-InputObject</span></span>
<span data-ttu-id="03acc-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="03acc-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="03acc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03acc-123">-PassThru</span></span>
<span data-ttu-id="03acc-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="03acc-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="03acc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03acc-125">-ResourceGroupName</span></span>
<span data-ttu-id="03acc-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="03acc-126">The name of the resource group.</span></span>
<span data-ttu-id="03acc-127">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="03acc-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="03acc-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="03acc-128">-SessionHostName</span></span>
<span data-ttu-id="03acc-129">Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="03acc-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="03acc-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03acc-130">-SubscriptionId</span></span>
<span data-ttu-id="03acc-131">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="03acc-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="03acc-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03acc-132">-Confirm</span></span>
<span data-ttu-id="03acc-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="03acc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03acc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03acc-134">-WhatIf</span></span>
<span data-ttu-id="03acc-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="03acc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03acc-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="03acc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03acc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03acc-137">CommonParameters</span></span>
<span data-ttu-id="03acc-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03acc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03acc-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03acc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03acc-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03acc-140">INPUTS</span></span>

### <span data-ttu-id="03acc-141">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="03acc-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="03acc-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03acc-142">OUTPUTS</span></span>

### <span data-ttu-id="03acc-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03acc-143">System.Boolean</span></span>

## <span data-ttu-id="03acc-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="03acc-144">NOTES</span></span>

<span data-ttu-id="03acc-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="03acc-145">ALIASES</span></span>

<span data-ttu-id="03acc-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="03acc-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="03acc-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="03acc-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="03acc-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="03acc-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="03acc-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="03acc-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="03acc-150">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="03acc-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="03acc-151">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="03acc-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="03acc-152">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="03acc-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="03acc-153">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="03acc-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="03acc-154">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="03acc-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="03acc-155">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="03acc-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="03acc-156">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="03acc-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="03acc-157">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="03acc-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="03acc-158">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="03acc-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="03acc-159">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="03acc-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="03acc-160">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="03acc-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="03acc-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03acc-161">RELATED LINKS</span></span>

