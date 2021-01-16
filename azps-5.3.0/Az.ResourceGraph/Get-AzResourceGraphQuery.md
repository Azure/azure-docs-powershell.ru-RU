---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 6d7dbb9acbcc03f266d698d1f9d8ce89f320d04b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506720"
---
# <span data-ttu-id="5320b-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="5320b-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="5320b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5320b-102">SYNOPSIS</span></span>
<span data-ttu-id="5320b-103">Получите запрос по одному графику по имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="5320b-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="5320b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5320b-104">SYNTAX</span></span>

### <span data-ttu-id="5320b-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5320b-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5320b-106">Получить</span><span class="sxs-lookup"><span data-stu-id="5320b-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5320b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5320b-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5320b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5320b-108">DESCRIPTION</span></span>
<span data-ttu-id="5320b-109">Получите запрос по одному графику по имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="5320b-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="5320b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5320b-110">EXAMPLES</span></span>

### <span data-ttu-id="5320b-111">Пример 1. Получить все запросы на график ресурсов в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="5320b-111">Example 1: Get all resource graph query under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="5320b-112">Эта команда получает все запросы на график ресурсов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5320b-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="5320b-113">Пример 2. Получить запрос на график ресурсов по имени</span><span class="sxs-lookup"><span data-stu-id="5320b-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="5320b-114">Эта команда получает запрос на график ресурсов по имени.</span><span class="sxs-lookup"><span data-stu-id="5320b-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="5320b-115">Пример 2. Получить запрос на график ресурсов по неосужаемости</span><span class="sxs-lookup"><span data-stu-id="5320b-115">Example 2: Get a resource graph query by objecy</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="5320b-116">Эта команда получает запрос на график ресурсов для объекта.</span><span class="sxs-lookup"><span data-stu-id="5320b-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="5320b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5320b-117">PARAMETERS</span></span>

### <span data-ttu-id="5320b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5320b-118">-DefaultProfile</span></span>
<span data-ttu-id="5320b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5320b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5320b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5320b-120">-InputObject</span></span>
<span data-ttu-id="5320b-121">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="5320b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5320b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5320b-122">-Name</span></span>
<span data-ttu-id="5320b-123">Имя ресурса Graph Query.</span><span class="sxs-lookup"><span data-stu-id="5320b-123">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="5320b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5320b-124">-ResourceGroupName</span></span>
<span data-ttu-id="5320b-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5320b-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="5320b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5320b-126">-SubscriptionId</span></span>
<span data-ttu-id="5320b-127">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="5320b-127">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="5320b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5320b-128">CommonParameters</span></span>
<span data-ttu-id="5320b-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5320b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5320b-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5320b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5320b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5320b-131">INPUTS</span></span>

### <span data-ttu-id="5320b-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="5320b-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="5320b-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5320b-133">OUTPUTS</span></span>

### <span data-ttu-id="5320b-134">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="5320b-134">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="5320b-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5320b-135">NOTES</span></span>

<span data-ttu-id="5320b-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5320b-136">ALIASES</span></span>

<span data-ttu-id="5320b-137">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5320b-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5320b-138">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="5320b-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5320b-139">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5320b-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5320b-140">INPUTOBJECT <IResourceGraphIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="5320b-140">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5320b-141">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="5320b-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5320b-142">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5320b-142">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5320b-143">`[ResourceName <String>]`: имя ресурса Graph Query.</span><span class="sxs-lookup"><span data-stu-id="5320b-143">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="5320b-144">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="5320b-144">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="5320b-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5320b-145">RELATED LINKS</span></span>

