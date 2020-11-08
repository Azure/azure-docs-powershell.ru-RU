---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 1b4f405e9bf6377855439d1f6d3cad9f0538920f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066934"
---
# <span data-ttu-id="10c09-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="10c09-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="10c09-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10c09-102">SYNOPSIS</span></span>
<span data-ttu-id="10c09-103">Создание пула экземпляров Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="10c09-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="10c09-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10c09-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10c09-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10c09-105">DESCRIPTION</span></span>
<span data-ttu-id="10c09-106">Командлет **New-AzSqlInstancePool** создает пул экземпляров Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="10c09-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="10c09-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10c09-107">EXAMPLES</span></span>

### <span data-ttu-id="10c09-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="10c09-108">Example 1</span></span>
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

<span data-ttu-id="10c09-109">Эта команда создает новый пул экземпляров Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="10c09-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="10c09-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10c09-110">PARAMETERS</span></span>

### <span data-ttu-id="10c09-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10c09-111">-AsJob</span></span>
<span data-ttu-id="10c09-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="10c09-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10c09-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="10c09-113">-ComputeGeneration</span></span>
<span data-ttu-id="10c09-114">Вычисленое поколение для пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="10c09-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="10c09-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c09-115">-DefaultProfile</span></span>
<span data-ttu-id="10c09-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10c09-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10c09-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="10c09-117">-Edition</span></span>
<span data-ttu-id="10c09-118">Выпуск для пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="10c09-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="10c09-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="10c09-119">-LicenseType</span></span>
<span data-ttu-id="10c09-120">Определяет, какой тип лицензии следует использовать.</span><span class="sxs-lookup"><span data-stu-id="10c09-120">Determines which License Type to use.</span></span>
<span data-ttu-id="10c09-121">Возможные значения: BasePrice (скидка AHB) и LicenseIncluded (без скидки AHB).</span><span class="sxs-lookup"><span data-stu-id="10c09-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="10c09-122">-Location</span><span class="sxs-lookup"><span data-stu-id="10c09-122">-Location</span></span>
<span data-ttu-id="10c09-123">Расположение для создания пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="10c09-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="10c09-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="10c09-124">-Name</span></span>
<span data-ttu-id="10c09-125">Имя пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="10c09-125">The name of the instance pool.</span></span>

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

### <span data-ttu-id="10c09-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10c09-126">-ResourceGroupName</span></span>
<span data-ttu-id="10c09-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="10c09-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="10c09-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="10c09-128">-SubnetId</span></span>
<span data-ttu-id="10c09-129">Идентификатор подсети, используемый для создания пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="10c09-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="10c09-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="10c09-130">-Tag</span></span>
<span data-ttu-id="10c09-131">Теги, связываемые с экземпляром</span><span class="sxs-lookup"><span data-stu-id="10c09-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="10c09-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="10c09-132">-VCore</span></span>
<span data-ttu-id="10c09-133">Определяет, сколько VCore связать с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="10c09-133">Determines how much VCore to associate with instance.</span></span>

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

### <span data-ttu-id="10c09-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10c09-134">-Confirm</span></span>
<span data-ttu-id="10c09-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="10c09-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10c09-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10c09-136">-WhatIf</span></span>
<span data-ttu-id="10c09-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="10c09-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10c09-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="10c09-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10c09-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c09-139">CommonParameters</span></span>
<span data-ttu-id="10c09-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10c09-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c09-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10c09-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c09-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10c09-142">INPUTS</span></span>

### <span data-ttu-id="10c09-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="10c09-143">None</span></span>

## <span data-ttu-id="10c09-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10c09-144">OUTPUTS</span></span>

### <span data-ttu-id="10c09-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="10c09-145">System.Object</span></span>
## <span data-ttu-id="10c09-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="10c09-146">NOTES</span></span>

## <span data-ttu-id="10c09-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10c09-147">RELATED LINKS</span></span>
