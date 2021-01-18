---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: db7d9165b8aec6a69f31850f7a37eddb2450e53b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506450"
---
# <span data-ttu-id="b3a67-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="b3a67-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="b3a67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3a67-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a67-103">Задает свойства для пула экземпляров Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a67-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="b3a67-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b3a67-104">SYNTAX</span></span>

### <span data-ttu-id="b3a67-105">DefaultSetInstancePoolParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3a67-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a67-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3a67-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a67-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3a67-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3a67-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3a67-108">DESCRIPTION</span></span>
<span data-ttu-id="b3a67-109">Cmdlet **Set-AzSqlInstancePool** изменяет свойства пула экземпляров Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b3a67-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="b3a67-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b3a67-110">EXAMPLES</span></span>

### <span data-ttu-id="b3a67-111">Пример 1. Настройка типа лицензии пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="b3a67-111">Example 1 : Set an instance pool license type</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0 -LicenseType LicenseIncluded
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

<span data-ttu-id="b3a67-112">Эта команда задает тип лицензии и (или) теги для пула экземпляров с именем instancePool0.</span><span class="sxs-lookup"><span data-stu-id="b3a67-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="b3a67-113">Пример 2. Настройка типа лицензии на экземпляр с помощью объекта пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="b3a67-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
PS C:\> Set-AzSqlInstancePool -InputObject $instancePool -LicenseType LicenseIncluded
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

<span data-ttu-id="b3a67-114">Эта команда задает тип лицензии и (или) теги для пула экземпляров с помощью объекта пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="b3a67-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="b3a67-115">Пример 3. Настройка типа лицензии пула экземпляров с помощью ИД ресурса пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="b3a67-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0" -LicenseType LicenseIncluded
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

<span data-ttu-id="b3a67-116">Эта команда задает тип лицензии и (или) теги для пула экземпляров с именем instancePool0.</span><span class="sxs-lookup"><span data-stu-id="b3a67-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="b3a67-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3a67-117">PARAMETERS</span></span>

### <span data-ttu-id="b3a67-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3a67-118">-AsJob</span></span>
<span data-ttu-id="b3a67-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b3a67-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3a67-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a67-120">-DefaultProfile</span></span>
<span data-ttu-id="b3a67-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a67-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3a67-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3a67-122">-InputObject</span></span>
<span data-ttu-id="b3a67-123">Объект ввода пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="b3a67-123">The instance pool input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InputObjectSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a67-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b3a67-124">-LicenseType</span></span>
<span data-ttu-id="b3a67-125">Определяет тип лицензии.</span><span class="sxs-lookup"><span data-stu-id="b3a67-125">Determines which License Type to use.</span></span>
<span data-ttu-id="b3a67-126">Возможные значения: BasePrice (с скидкой AHB) и LicenseIncluded (без скидки AHB).</span><span class="sxs-lookup"><span data-stu-id="b3a67-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="b3a67-127">-Name</span><span class="sxs-lookup"><span data-stu-id="b3a67-127">-Name</span></span>
<span data-ttu-id="b3a67-128">Имя пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="b3a67-128">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a67-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a67-129">-ResourceGroupName</span></span>
<span data-ttu-id="b3a67-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b3a67-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a67-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a67-131">-ResourceId</span></span>
<span data-ttu-id="b3a67-132">Идентификатор ресурса пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="b3a67-132">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a67-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3a67-133">-Tag</span></span>
<span data-ttu-id="b3a67-134">Теги, которые нужно связать с экземпляром</span><span class="sxs-lookup"><span data-stu-id="b3a67-134">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a67-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3a67-135">-Confirm</span></span>
<span data-ttu-id="b3a67-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3a67-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3a67-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3a67-137">-WhatIf</span></span>
<span data-ttu-id="b3a67-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3a67-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3a67-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b3a67-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3a67-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a67-140">CommonParameters</span></span>
<span data-ttu-id="b3a67-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a67-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a67-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3a67-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a67-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3a67-143">INPUTS</span></span>

### <span data-ttu-id="b3a67-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="b3a67-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="b3a67-145">System.String</span><span class="sxs-lookup"><span data-stu-id="b3a67-145">System.String</span></span>

## <span data-ttu-id="b3a67-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b3a67-146">OUTPUTS</span></span>

### <span data-ttu-id="b3a67-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="b3a67-147">System.Object</span></span>
## <span data-ttu-id="b3a67-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b3a67-148">NOTES</span></span>

## <span data-ttu-id="b3a67-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3a67-149">RELATED LINKS</span></span>
