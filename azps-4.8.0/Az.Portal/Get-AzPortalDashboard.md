---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244282"
---
# <span data-ttu-id="4af9a-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="4af9a-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="4af9a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4af9a-102">SYNOPSIS</span></span>
<span data-ttu-id="4af9a-103">Получает панель мониторинга.</span><span class="sxs-lookup"><span data-stu-id="4af9a-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="4af9a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4af9a-104">SYNTAX</span></span>

### <span data-ttu-id="4af9a-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4af9a-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4af9a-106">Получить</span><span class="sxs-lookup"><span data-stu-id="4af9a-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4af9a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4af9a-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4af9a-108">Список</span><span class="sxs-lookup"><span data-stu-id="4af9a-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4af9a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4af9a-109">DESCRIPTION</span></span>
<span data-ttu-id="4af9a-110">Получает панель мониторинга.</span><span class="sxs-lookup"><span data-stu-id="4af9a-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="4af9a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4af9a-111">EXAMPLES</span></span>

### <span data-ttu-id="4af9a-112">Пример 1: список всех панелей мониторинга в подписке</span><span class="sxs-lookup"><span data-stu-id="4af9a-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="4af9a-113">Список всех панелей мониторинга в подписке</span><span class="sxs-lookup"><span data-stu-id="4af9a-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="4af9a-114">Пример 2: получение сведений для одной панели мониторинга портала</span><span class="sxs-lookup"><span data-stu-id="4af9a-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="4af9a-115">Получение подробностей для одной панели мониторинга</span><span class="sxs-lookup"><span data-stu-id="4af9a-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="4af9a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4af9a-116">PARAMETERS</span></span>

### <span data-ttu-id="4af9a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af9a-117">-DefaultProfile</span></span>
<span data-ttu-id="4af9a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4af9a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4af9a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4af9a-119">-InputObject</span></span>
<span data-ttu-id="4af9a-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="4af9a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4af9a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4af9a-121">-Name</span></span>
<span data-ttu-id="4af9a-122">Имя панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="4af9a-122">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af9a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4af9a-123">-ResourceGroupName</span></span>
<span data-ttu-id="4af9a-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4af9a-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af9a-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4af9a-125">-SubscriptionId</span></span>
<span data-ttu-id="4af9a-126">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="4af9a-126">The Azure subscription ID.</span></span>
<span data-ttu-id="4af9a-127">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="4af9a-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af9a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af9a-128">CommonParameters</span></span>
<span data-ttu-id="4af9a-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4af9a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af9a-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4af9a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af9a-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4af9a-131">INPUTS</span></span>

### <span data-ttu-id="4af9a-132">Microsoft. Azure. PowerShell. командлеты. Portal. Models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="4af9a-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="4af9a-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4af9a-133">OUTPUTS</span></span>

### <span data-ttu-id="4af9a-134">Microsoft. Azure. PowerShell. командлеты. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="4af9a-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="4af9a-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="4af9a-135">NOTES</span></span>

<span data-ttu-id="4af9a-136">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="4af9a-136">ALIASES</span></span>

<span data-ttu-id="4af9a-137">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4af9a-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4af9a-138">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4af9a-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4af9a-139">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4af9a-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4af9a-140">INPUTOBJECT <IPortalIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="4af9a-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4af9a-141">`[DashboardName <String>]`: Имя панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="4af9a-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="4af9a-142">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="4af9a-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4af9a-143">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4af9a-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="4af9a-144">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="4af9a-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="4af9a-145">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="4af9a-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="4af9a-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4af9a-146">RELATED LINKS</span></span>

