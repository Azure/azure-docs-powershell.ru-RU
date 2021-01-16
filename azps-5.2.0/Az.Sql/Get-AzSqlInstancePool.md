---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
ms.openlocfilehash: afbd74953f876ede2a03e94c4db46937470a92dc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325236"
---
# <span data-ttu-id="6aa0a-101">Get-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="6aa0a-101">Get-AzSqlInstancePool</span></span>

## <span data-ttu-id="6aa0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aa0a-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa0a-103">Возвращает сведения о пуле экземпляров Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa0a-103">Returns information about the Azure SQL Instance pool.</span></span>

## <span data-ttu-id="6aa0a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6aa0a-104">SYNTAX</span></span>

### <span data-ttu-id="6aa0a-105">ListBySubOrResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6aa0a-105">ListBySubOrResourceGroupParameterSet (Default)</span></span>
```
Get-AzSqlInstancePool [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6aa0a-106">ListByInstancePoolDefaultsParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aa0a-106">ListByInstancePoolDefaultsParameterSet</span></span>
```
Get-AzSqlInstancePool -ResourceGroupName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6aa0a-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aa0a-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6aa0a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6aa0a-108">DESCRIPTION</span></span>
<span data-ttu-id="6aa0a-109">**Cmdlet Get-AzSqlInstancePool** возвращает сведения об одном или SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa0a-109">The **Get-AzSqlInstancePool** cmdlet returns information about one or more Azure SQL Instance pool.</span></span>
<span data-ttu-id="6aa0a-110">Укажите имя пула экземпляров, чтобы увидеть сведения только для этого пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="6aa0a-110">Specify the name of an instance pool to see information for only that instance pool.</span></span>

## <span data-ttu-id="6aa0a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6aa0a-111">EXAMPLES</span></span>

### <span data-ttu-id="6aa0a-112">Пример 1. Все пулы экземпляров для подписки клиента</span><span class="sxs-lookup"><span data-stu-id="6aa0a-112">Example 1: Get all instance pools across a customer subscription</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded

ResourceGroupName : resourcegroup02
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Sql/instancePools/ps-instancepool-1
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="6aa0a-113">Эта команда получает сведения обо всех пулах экземпляров в рамках подписки клиента.</span><span class="sxs-lookup"><span data-stu-id="6aa0a-113">This command gets information about all instance pools within the customer subscription.</span></span>

### <span data-ttu-id="6aa0a-114">Пример 2. Объединение всех пулов экземпляров в группу ресурсов</span><span class="sxs-lookup"><span data-stu-id="6aa0a-114">Example 2: Get all instance pools across a resource group</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="6aa0a-115">Эта команда получает сведения обо всех пулах экземпляров в группе ресурсов resourcegroup01.</span><span class="sxs-lookup"><span data-stu-id="6aa0a-115">This command gets information about all instance pools within the resource group resourcegroup01.</span></span>

### <span data-ttu-id="6aa0a-116">Пример 3. Просмотр сведений о пуле экземпляров</span><span class="sxs-lookup"><span data-stu-id="6aa0a-116">Example 3: Get information about an instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="6aa0a-117">Эта команда получает сведения о экземпляре пула экземпляровPool0.</span><span class="sxs-lookup"><span data-stu-id="6aa0a-117">This command gets information about the instance pool instancePool0.</span></span>

### <span data-ttu-id="6aa0a-118">Пример 4. Получите сведения о пуле экземпляров с помощью ИД ресурса пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="6aa0a-118">Example 4: Get information about an instance pool using instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="6aa0a-119">Эта команда получает сведения о пуле экземпляров с идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="6aa0a-119">This command gets information about the instance pool with its resource identifier.</span></span>

## <span data-ttu-id="6aa0a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6aa0a-120">PARAMETERS</span></span>

### <span data-ttu-id="6aa0a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa0a-121">-DefaultProfile</span></span>
<span data-ttu-id="6aa0a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa0a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aa0a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6aa0a-123">-Name</span></span>
<span data-ttu-id="6aa0a-124">Имя пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="6aa0a-124">The instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aa0a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aa0a-125">-ResourceGroupName</span></span>
<span data-ttu-id="6aa0a-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6aa0a-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListBySubOrResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aa0a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6aa0a-127">-ResourceId</span></span>
<span data-ttu-id="6aa0a-128">Идентификатор ресурса пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="6aa0a-128">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstancePoolByInstancePoolResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa0a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa0a-129">CommonParameters</span></span>
<span data-ttu-id="6aa0a-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aa0a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa0a-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6aa0a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa0a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6aa0a-132">INPUTS</span></span>

### <span data-ttu-id="6aa0a-133">Нет</span><span class="sxs-lookup"><span data-stu-id="6aa0a-133">None</span></span>

## <span data-ttu-id="6aa0a-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6aa0a-134">OUTPUTS</span></span>

### <span data-ttu-id="6aa0a-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="6aa0a-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

## <span data-ttu-id="6aa0a-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6aa0a-136">NOTES</span></span>

## <span data-ttu-id="6aa0a-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6aa0a-137">RELATED LINKS</span></span>
