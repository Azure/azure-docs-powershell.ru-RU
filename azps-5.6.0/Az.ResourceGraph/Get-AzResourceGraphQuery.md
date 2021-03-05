---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 46f59df272a62ca9cd6b517d3672436a01a75ffb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000152"
---
# <span data-ttu-id="495ad-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="495ad-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="495ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="495ad-102">SYNOPSIS</span></span>
<span data-ttu-id="495ad-103">Получите запрос по одному графику по имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="495ad-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="495ad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="495ad-104">SYNTAX</span></span>

### <span data-ttu-id="495ad-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="495ad-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="495ad-106">Получить</span><span class="sxs-lookup"><span data-stu-id="495ad-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="495ad-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="495ad-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="495ad-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="495ad-108">DESCRIPTION</span></span>
<span data-ttu-id="495ad-109">Получите запрос по одному графику по имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="495ad-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="495ad-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="495ad-110">EXAMPLES</span></span>

### <span data-ttu-id="495ad-111">Пример 1. Получить все запросы на график ресурсов в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="495ad-111">Example 1: Get all resource graph queries under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="495ad-112">Эта команда получает все запросы на график ресурсов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="495ad-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="495ad-113">Пример 2. Получить запрос на график ресурсов по имени</span><span class="sxs-lookup"><span data-stu-id="495ad-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="495ad-114">Эта команда получает запрос на график ресурсов по имени.</span><span class="sxs-lookup"><span data-stu-id="495ad-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="495ad-115">Пример 2. Получить запрос на график ресурсов по объекту</span><span class="sxs-lookup"><span data-stu-id="495ad-115">Example 2: Get a resource graph query by object</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="495ad-116">Эта команда получает запрос на график ресурсов для объекта.</span><span class="sxs-lookup"><span data-stu-id="495ad-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="495ad-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="495ad-117">PARAMETERS</span></span>

### <span data-ttu-id="495ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="495ad-118">-DefaultProfile</span></span>
<span data-ttu-id="495ad-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="495ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="495ad-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="495ad-120">-InputObject</span></span>
<span data-ttu-id="495ad-121">Параметр identity</span><span class="sxs-lookup"><span data-stu-id="495ad-121">Identity Parameter</span></span>

<span data-ttu-id="495ad-122">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="495ad-122">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="495ad-123">-Name</span><span class="sxs-lookup"><span data-stu-id="495ad-123">-Name</span></span>
<span data-ttu-id="495ad-124">Имя ресурса Graph Query.</span><span class="sxs-lookup"><span data-stu-id="495ad-124">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495ad-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="495ad-125">-ResourceGroupName</span></span>
<span data-ttu-id="495ad-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="495ad-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="495ad-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="495ad-127">-SubscriptionId</span></span>
<span data-ttu-id="495ad-128">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="495ad-128">The Azure subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495ad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="495ad-129">CommonParameters</span></span>
<span data-ttu-id="495ad-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="495ad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="495ad-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="495ad-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="495ad-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="495ad-132">INPUTS</span></span>

### <span data-ttu-id="495ad-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="495ad-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="495ad-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="495ad-134">OUTPUTS</span></span>

### <span data-ttu-id="495ad-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="495ad-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="495ad-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="495ad-136">NOTES</span></span>

<span data-ttu-id="495ad-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="495ad-137">ALIASES</span></span>

<span data-ttu-id="495ad-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="495ad-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="495ad-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="495ad-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="495ad-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="495ad-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="495ad-141">INPUTOBJECT <IResourceGraphIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="495ad-141">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="495ad-142">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="495ad-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="495ad-143">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="495ad-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="495ad-144">`[ResourceName <String>]`: имя ресурса Graph Query.</span><span class="sxs-lookup"><span data-stu-id="495ad-144">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="495ad-145">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="495ad-145">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="495ad-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="495ad-146">RELATED LINKS</span></span>

