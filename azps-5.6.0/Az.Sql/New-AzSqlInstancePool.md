---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 818e76c9ea46b2593b3bdd3871f417dbaca044a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977683"
---
# <span data-ttu-id="19c8b-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="19c8b-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="19c8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="19c8b-103">Создает пул экземпляров SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="19c8b-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="19c8b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="19c8b-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19c8b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19c8b-105">DESCRIPTION</span></span>
<span data-ttu-id="19c8b-106">Для **создания пула экземпляров Azure SQL AzSqlInstancePool.**</span><span class="sxs-lookup"><span data-stu-id="19c8b-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="19c8b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="19c8b-107">EXAMPLES</span></span>

### <span data-ttu-id="19c8b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="19c8b-108">Example 1</span></span>
```powershell
PS C:\> New-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0 -Location canadacentral -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -Edition GeneralPurpose -ComputeGeneration Gen5 -LicenseType LicenseIncluded
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

<span data-ttu-id="19c8b-109">Эта команда создает новый пул экземпляров Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="19c8b-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="19c8b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19c8b-110">PARAMETERS</span></span>

### <span data-ttu-id="19c8b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19c8b-111">-AsJob</span></span>
<span data-ttu-id="19c8b-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="19c8b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19c8b-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="19c8b-113">-ComputeGeneration</span></span>
<span data-ttu-id="19c8b-114">Генерация компьютеров для пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="19c8b-114">The compute generation for the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c8b-115">-DefaultProfile</span></span>
<span data-ttu-id="19c8b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19c8b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19c8b-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="19c8b-117">-Edition</span></span>
<span data-ttu-id="19c8b-118">Выпуск для пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="19c8b-118">The edition for the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c8b-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="19c8b-119">-LicenseType</span></span>
<span data-ttu-id="19c8b-120">Определяет тип лицензии.</span><span class="sxs-lookup"><span data-stu-id="19c8b-120">Determines which License Type to use.</span></span>
<span data-ttu-id="19c8b-121">Возможные значения: BasePrice (с скидкой AHB) и LicenseIncluded (без скидки AHB).</span><span class="sxs-lookup"><span data-stu-id="19c8b-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c8b-122">-Location</span><span class="sxs-lookup"><span data-stu-id="19c8b-122">-Location</span></span>
<span data-ttu-id="19c8b-123">Расположение для создания пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="19c8b-123">The location to create the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c8b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="19c8b-124">-Name</span></span>
<span data-ttu-id="19c8b-125">Имя пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="19c8b-125">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c8b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c8b-126">-ResourceGroupName</span></span>
<span data-ttu-id="19c8b-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19c8b-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c8b-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="19c8b-128">-SubnetId</span></span>
<span data-ttu-id="19c8b-129">ИД подсети, который используется для создания пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="19c8b-129">The subnet id to use for instance pool creation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c8b-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="19c8b-130">-Tag</span></span>
<span data-ttu-id="19c8b-131">Теги, которые нужно связать с экземпляром</span><span class="sxs-lookup"><span data-stu-id="19c8b-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="19c8b-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="19c8b-132">-VCore</span></span>
<span data-ttu-id="19c8b-133">Определяет, сколько VCore нужно связать с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="19c8b-133">Determines how much VCore to associate with instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: VCores

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c8b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19c8b-134">-Confirm</span></span>
<span data-ttu-id="19c8b-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="19c8b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19c8b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c8b-136">-WhatIf</span></span>
<span data-ttu-id="19c8b-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19c8b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19c8b-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="19c8b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19c8b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c8b-139">CommonParameters</span></span>
<span data-ttu-id="19c8b-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c8b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c8b-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19c8b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c8b-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19c8b-142">INPUTS</span></span>

### <span data-ttu-id="19c8b-143">Нет</span><span class="sxs-lookup"><span data-stu-id="19c8b-143">None</span></span>

## <span data-ttu-id="19c8b-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="19c8b-144">OUTPUTS</span></span>

### <span data-ttu-id="19c8b-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="19c8b-145">System.Object</span></span>
## <span data-ttu-id="19c8b-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="19c8b-146">NOTES</span></span>

## <span data-ttu-id="19c8b-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19c8b-147">RELATED LINKS</span></span>
