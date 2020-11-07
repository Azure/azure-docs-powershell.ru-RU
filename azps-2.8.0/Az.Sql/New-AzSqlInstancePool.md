---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: d65e32992b113dfb587b68dd3fcdc1701b291ad4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906577"
---
# <span data-ttu-id="4c004-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="4c004-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="4c004-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c004-102">SYNOPSIS</span></span>
<span data-ttu-id="4c004-103">Создание пула экземпляров Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4c004-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="4c004-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c004-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c004-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c004-105">DESCRIPTION</span></span>
<span data-ttu-id="4c004-106">Командлет **New-AzSqlInstancePool** создает пул экземпляров Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4c004-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="4c004-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c004-107">EXAMPLES</span></span>

### <span data-ttu-id="4c004-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4c004-108">Example 1</span></span>
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

<span data-ttu-id="4c004-109">Эта команда создает новый пул экземпляров Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4c004-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="4c004-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c004-110">PARAMETERS</span></span>

### <span data-ttu-id="4c004-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c004-111">-AsJob</span></span>
<span data-ttu-id="4c004-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4c004-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c004-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="4c004-113">-ComputeGeneration</span></span>
<span data-ttu-id="4c004-114">Вычисленое поколение для пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4c004-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="4c004-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c004-115">-DefaultProfile</span></span>
<span data-ttu-id="4c004-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c004-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c004-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="4c004-117">-Edition</span></span>
<span data-ttu-id="4c004-118">Выпуск для пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4c004-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="4c004-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4c004-119">-LicenseType</span></span>
<span data-ttu-id="4c004-120">Определяет, какой тип лицензии следует использовать.</span><span class="sxs-lookup"><span data-stu-id="4c004-120">Determines which License Type to use.</span></span>
<span data-ttu-id="4c004-121">Возможные значения: BasePrice (скидка AHB) и LicenseIncluded (без скидки AHB).</span><span class="sxs-lookup"><span data-stu-id="4c004-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="4c004-122">-Location</span><span class="sxs-lookup"><span data-stu-id="4c004-122">-Location</span></span>
<span data-ttu-id="4c004-123">Расположение для создания пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4c004-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="4c004-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4c004-124">-Name</span></span>
<span data-ttu-id="4c004-125">Имя пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4c004-125">The name of the instance pool.</span></span>

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

### <span data-ttu-id="4c004-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c004-126">-ResourceGroupName</span></span>
<span data-ttu-id="4c004-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4c004-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="4c004-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4c004-128">-SubnetId</span></span>
<span data-ttu-id="4c004-129">Идентификатор подсети, используемый для создания пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4c004-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="4c004-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="4c004-130">-Tag</span></span>
<span data-ttu-id="4c004-131">Теги, связываемые с экземпляром</span><span class="sxs-lookup"><span data-stu-id="4c004-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="4c004-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="4c004-132">-VCore</span></span>
<span data-ttu-id="4c004-133">Определяет, сколько VCore связать с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="4c004-133">Determines how much VCore to associate with instance.</span></span>

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

### <span data-ttu-id="4c004-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c004-134">-Confirm</span></span>
<span data-ttu-id="4c004-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4c004-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c004-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c004-136">-WhatIf</span></span>
<span data-ttu-id="4c004-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4c004-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c004-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4c004-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c004-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c004-139">CommonParameters</span></span>
<span data-ttu-id="4c004-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c004-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c004-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c004-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c004-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c004-142">INPUTS</span></span>

### <span data-ttu-id="4c004-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="4c004-143">None</span></span>

## <span data-ttu-id="4c004-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c004-144">OUTPUTS</span></span>

### <span data-ttu-id="4c004-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="4c004-145">System.Object</span></span>
## <span data-ttu-id="4c004-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c004-146">NOTES</span></span>

## <span data-ttu-id="4c004-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c004-147">RELATED LINKS</span></span>
