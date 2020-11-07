---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: db7d9165b8aec6a69f31850f7a37eddb2450e53b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912511"
---
# <span data-ttu-id="13464-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="13464-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="13464-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13464-102">SYNOPSIS</span></span>
<span data-ttu-id="13464-103">Задает свойства для пула экземпляров Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="13464-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="13464-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13464-104">SYNTAX</span></span>

### <span data-ttu-id="13464-105">DefaultSetInstancePoolParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13464-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13464-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="13464-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13464-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="13464-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13464-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13464-108">DESCRIPTION</span></span>
<span data-ttu-id="13464-109">Командлет **Set-AzSqlInstancePool** изменяет свойства пула экземпляров Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="13464-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="13464-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13464-110">EXAMPLES</span></span>

### <span data-ttu-id="13464-111">Пример 1: Настройка типа лицензии для пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="13464-111">Example 1 : Set an instance pool license type</span></span>
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

<span data-ttu-id="13464-112">Эта команда задает тип лицензии и (или) Теги для пула экземпляров с именем instancePool0.</span><span class="sxs-lookup"><span data-stu-id="13464-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="13464-113">Пример 2: Настройка типа лицензии пула экземпляров с помощью объекта пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="13464-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
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

<span data-ttu-id="13464-114">Эта команда задает тип лицензии и (или) Теги для пула экземпляров с помощью объекта пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="13464-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="13464-115">Пример 3: Настройка типа лицензии пула экземпляров с помощью идентификатора ресурса пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="13464-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
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

<span data-ttu-id="13464-116">Эта команда задает тип лицензии и (или) Теги для пула экземпляров с именем instancePool0.</span><span class="sxs-lookup"><span data-stu-id="13464-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="13464-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13464-117">PARAMETERS</span></span>

### <span data-ttu-id="13464-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13464-118">-AsJob</span></span>
<span data-ttu-id="13464-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="13464-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13464-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13464-120">-DefaultProfile</span></span>
<span data-ttu-id="13464-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13464-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13464-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13464-122">-InputObject</span></span>
<span data-ttu-id="13464-123">Входной объект пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="13464-123">The instance pool input object.</span></span>

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

### <span data-ttu-id="13464-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="13464-124">-LicenseType</span></span>
<span data-ttu-id="13464-125">Определяет, какой тип лицензии следует использовать.</span><span class="sxs-lookup"><span data-stu-id="13464-125">Determines which License Type to use.</span></span>
<span data-ttu-id="13464-126">Возможные значения: BasePrice (скидка AHB) и LicenseIncluded (без скидки AHB).</span><span class="sxs-lookup"><span data-stu-id="13464-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="13464-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13464-127">-Name</span></span>
<span data-ttu-id="13464-128">Имя пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="13464-128">The name of the instance pool.</span></span>

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

### <span data-ttu-id="13464-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13464-129">-ResourceGroupName</span></span>
<span data-ttu-id="13464-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13464-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="13464-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13464-131">-ResourceId</span></span>
<span data-ttu-id="13464-132">Идентификатор ресурса пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="13464-132">The instance pool resource identifier.</span></span>

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

### <span data-ttu-id="13464-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="13464-133">-Tag</span></span>
<span data-ttu-id="13464-134">Теги, связываемые с экземпляром</span><span class="sxs-lookup"><span data-stu-id="13464-134">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="13464-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13464-135">-Confirm</span></span>
<span data-ttu-id="13464-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="13464-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13464-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13464-137">-WhatIf</span></span>
<span data-ttu-id="13464-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="13464-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13464-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="13464-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13464-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13464-140">CommonParameters</span></span>
<span data-ttu-id="13464-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13464-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13464-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13464-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13464-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13464-143">INPUTS</span></span>

### <span data-ttu-id="13464-144">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="13464-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="13464-145">System. String</span><span class="sxs-lookup"><span data-stu-id="13464-145">System.String</span></span>

## <span data-ttu-id="13464-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13464-146">OUTPUTS</span></span>

### <span data-ttu-id="13464-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="13464-147">System.Object</span></span>
## <span data-ttu-id="13464-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="13464-148">NOTES</span></span>

## <span data-ttu-id="13464-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13464-149">RELATED LINKS</span></span>
