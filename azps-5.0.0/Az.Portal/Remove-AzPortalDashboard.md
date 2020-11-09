---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318428"
---
# <span data-ttu-id="98d0c-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="98d0c-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="98d0c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="98d0c-103">Удаляет панель мониторинга.</span><span class="sxs-lookup"><span data-stu-id="98d0c-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="98d0c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98d0c-104">SYNTAX</span></span>

### <span data-ttu-id="98d0c-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98d0c-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="98d0c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="98d0c-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="98d0c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98d0c-107">DESCRIPTION</span></span>
<span data-ttu-id="98d0c-108">Удаляет панель мониторинга.</span><span class="sxs-lookup"><span data-stu-id="98d0c-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="98d0c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98d0c-109">EXAMPLES</span></span>

### <span data-ttu-id="98d0c-110">Пример 1: Удаление панели мониторинга</span><span class="sxs-lookup"><span data-stu-id="98d0c-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="98d0c-111">Удаление Dashbaord с помощью имени группы ресурсов и имени панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="98d0c-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="98d0c-112">Пример 2: Удаление панели мониторинга с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="98d0c-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="98d0c-113">Удаление панели мониторинга, возвращенной из вызова Get-AzDashboard.</span><span class="sxs-lookup"><span data-stu-id="98d0c-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="98d0c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98d0c-114">PARAMETERS</span></span>

### <span data-ttu-id="98d0c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d0c-115">-DefaultProfile</span></span>
<span data-ttu-id="98d0c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98d0c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98d0c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98d0c-117">-InputObject</span></span>
<span data-ttu-id="98d0c-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="98d0c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98d0c-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98d0c-119">-Name</span></span>
<span data-ttu-id="98d0c-120">Имя панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="98d0c-120">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98d0c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98d0c-121">-PassThru</span></span>
<span data-ttu-id="98d0c-122">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="98d0c-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="98d0c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98d0c-123">-ResourceGroupName</span></span>
<span data-ttu-id="98d0c-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98d0c-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="98d0c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98d0c-125">-SubscriptionId</span></span>
<span data-ttu-id="98d0c-126">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="98d0c-126">The Azure subscription ID.</span></span>
<span data-ttu-id="98d0c-127">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="98d0c-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="98d0c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98d0c-128">-Confirm</span></span>
<span data-ttu-id="98d0c-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="98d0c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98d0c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98d0c-130">-WhatIf</span></span>
<span data-ttu-id="98d0c-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="98d0c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98d0c-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="98d0c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98d0c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d0c-133">CommonParameters</span></span>
<span data-ttu-id="98d0c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98d0c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d0c-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98d0c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d0c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98d0c-136">INPUTS</span></span>

### <span data-ttu-id="98d0c-137">Microsoft. Azure. PowerShell. командлеты. Portal. Models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="98d0c-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="98d0c-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98d0c-138">OUTPUTS</span></span>

### <span data-ttu-id="98d0c-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98d0c-139">System.Boolean</span></span>

## <span data-ttu-id="98d0c-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="98d0c-140">NOTES</span></span>

<span data-ttu-id="98d0c-141">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="98d0c-141">ALIASES</span></span>

<span data-ttu-id="98d0c-142">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="98d0c-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="98d0c-143">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="98d0c-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="98d0c-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="98d0c-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="98d0c-145">INPUTOBJECT <IPortalIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="98d0c-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="98d0c-146">`[DashboardName <String>]`: Имя панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="98d0c-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="98d0c-147">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="98d0c-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="98d0c-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98d0c-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="98d0c-149">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="98d0c-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="98d0c-150">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="98d0c-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="98d0c-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98d0c-151">RELATED LINKS</span></span>

