---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepoolusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
ms.openlocfilehash: c2acc357e53a57060f7ba1ff3e19a5344ceee412
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243924"
---
# <span data-ttu-id="711ae-101">Get-AzSqlInstancePoolUsage</span><span class="sxs-lookup"><span data-stu-id="711ae-101">Get-AzSqlInstancePoolUsage</span></span>

## <span data-ttu-id="711ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="711ae-102">SYNOPSIS</span></span>
<span data-ttu-id="711ae-103">Возвращает сведения об использовании пула экземпляров Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="711ae-103">Returns information about an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="711ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="711ae-104">SYNTAX</span></span>

### <span data-ttu-id="711ae-105">InstancePoolUsageDefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="711ae-105">InstancePoolUsageDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceGroupName] <String> [-Name] <String> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="711ae-106">InstancePoolUsageParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="711ae-106">InstancePoolUsageParentObjectParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-InstancePool] <AzureSqlInstancePoolModel> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="711ae-107">InstancePoolUsageResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="711ae-107">InstancePoolUsageResourceIdParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceId] <String> [-ExpandChildren] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="711ae-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="711ae-108">DESCRIPTION</span></span>
<span data-ttu-id="711ae-109">Командлет **Get-AzSqlInstancePoolUsage** возвращает сведения об использовании пула экземпляров Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="711ae-109">The **Get-AzSqlInstancePoolUsage** cmdlet returns information an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="711ae-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="711ae-110">EXAMPLES</span></span>

### <span data-ttu-id="711ae-111">Пример 1: получение сведений об использовании пула экземпляров Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="711ae-111">Example 1 : Gets the usage of an Azure SQL Instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="711ae-112">Получает сведения об использовании пула экземпляров Azure SQL instancepool0.</span><span class="sxs-lookup"><span data-stu-id="711ae-112">Gets the usage for the Azure SQL Instance pool instancepool0.</span></span>

### <span data-ttu-id="711ae-113">Пример 2. Возвращает использование пула экземпляров Azure SQL с помощью объекта пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="711ae-113">Example 2: Gets the usage of an Azure SQL Instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> Get-AzSqlInstancePoolUsage -InstancePool $instancePool

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="711ae-114">Получает сведения об использовании пула экземпляров Azure SQL instancepool0 с использованием объекта пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="711ae-114">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool object.</span></span>

### <span data-ttu-id="711ae-115">Пример 3. Возвращает использование пула экземпляров Azure SQL с помощью идентификатора ресурса пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="711ae-115">Example 3: Gets the usage of an Azure SQL Instance pool using an instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="711ae-116">Возвращает использование для пула экземпляров Azure SQL instancepool0 с использованием идентификатора ресурса пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="711ae-116">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool resource identifier.</span></span>

### <span data-ttu-id="711ae-117">Пример 3: получает использование пула экземпляров Azure SQL с разделением используемых управляемых экземпляров в пуле.</span><span class="sxs-lookup"><span data-stu-id="711ae-117">Example 3: Gets the usage of an Azure SQL Instance pool with a breakdown of the managed instance usages within the pool.</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0 -ExpandChildren

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/vcore_utilization
CurrentValue   :
Limit          : 2
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/storage_utilization
CurrentValue   :
Limit          : 32
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages
```

<span data-ttu-id="711ae-118">Возвращает использование для пула экземпляров Azure SQL instancepool0 и использование управляемых экземпляров в instancepool0.</span><span class="sxs-lookup"><span data-stu-id="711ae-118">Gets the usage for the Azure SQL Instance pool instancepool0 along with the usages of the managed instances within instancepool0.</span></span>

## <span data-ttu-id="711ae-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="711ae-119">PARAMETERS</span></span>

### <span data-ttu-id="711ae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="711ae-120">-DefaultProfile</span></span>
<span data-ttu-id="711ae-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="711ae-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="711ae-122">-ExpandChildren</span><span class="sxs-lookup"><span data-stu-id="711ae-122">-ExpandChildren</span></span>
<span data-ttu-id="711ae-123">Флаг, указывающий, следует ли расширить использование этого пула экземпляров с использованием его дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="711ae-123">Flag indicating whether to expand this instance pool's usage with its children's usage.</span></span>

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

### <span data-ttu-id="711ae-124">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="711ae-124">-InstancePool</span></span>
<span data-ttu-id="711ae-125">Родительский объект пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="711ae-125">The parent instance pool object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InstancePoolUsageParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="711ae-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="711ae-126">-Name</span></span>
<span data-ttu-id="711ae-127">Имя пула управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="711ae-127">The managed instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="711ae-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="711ae-128">-ResourceGroupName</span></span>
<span data-ttu-id="711ae-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="711ae-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="711ae-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="711ae-130">-ResourceId</span></span>
<span data-ttu-id="711ae-131">Родительский идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="711ae-131">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageResourceIdParameterSet
Aliases: InstancePoolResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="711ae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="711ae-132">CommonParameters</span></span>
<span data-ttu-id="711ae-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="711ae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="711ae-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="711ae-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="711ae-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="711ae-135">INPUTS</span></span>

### <span data-ttu-id="711ae-136">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="711ae-136">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="711ae-137">System. String</span><span class="sxs-lookup"><span data-stu-id="711ae-137">System.String</span></span>

## <span data-ttu-id="711ae-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="711ae-138">OUTPUTS</span></span>

### <span data-ttu-id="711ae-139">Microsoft. Azure. Commands. SQL. Usages. Models. AzureSqlUsageModel</span><span class="sxs-lookup"><span data-stu-id="711ae-139">Microsoft.Azure.Commands.Sql.Usages.Models.AzureSqlUsageModel</span></span>

## <span data-ttu-id="711ae-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="711ae-140">NOTES</span></span>

## <span data-ttu-id="711ae-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="711ae-141">RELATED LINKS</span></span>
