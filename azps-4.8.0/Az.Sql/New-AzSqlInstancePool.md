---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 1b4f405e9bf6377855439d1f6d3cad9f0538920f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078642"
---
# <span data-ttu-id="8b17e-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="8b17e-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="8b17e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b17e-102">SYNOPSIS</span></span>
<span data-ttu-id="8b17e-103">Создание пула экземпляров Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="8b17e-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="8b17e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b17e-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b17e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b17e-105">DESCRIPTION</span></span>
<span data-ttu-id="8b17e-106">Командлет **New-AzSqlInstancePool** создает пул экземпляров Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="8b17e-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="8b17e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b17e-107">EXAMPLES</span></span>

### <span data-ttu-id="8b17e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b17e-108">Example 1</span></span>
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

<span data-ttu-id="8b17e-109">Эта команда создает новый пул экземпляров Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="8b17e-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="8b17e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b17e-110">PARAMETERS</span></span>

### <span data-ttu-id="8b17e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b17e-111">-AsJob</span></span>
<span data-ttu-id="8b17e-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8b17e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b17e-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="8b17e-113">-ComputeGeneration</span></span>
<span data-ttu-id="8b17e-114">Вычисленое поколение для пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="8b17e-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="8b17e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b17e-115">-DefaultProfile</span></span>
<span data-ttu-id="8b17e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b17e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b17e-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="8b17e-117">-Edition</span></span>
<span data-ttu-id="8b17e-118">Выпуск для пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="8b17e-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="8b17e-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8b17e-119">-LicenseType</span></span>
<span data-ttu-id="8b17e-120">Определяет, какой тип лицензии следует использовать.</span><span class="sxs-lookup"><span data-stu-id="8b17e-120">Determines which License Type to use.</span></span>
<span data-ttu-id="8b17e-121">Возможные значения: BasePrice (скидка AHB) и LicenseIncluded (без скидки AHB).</span><span class="sxs-lookup"><span data-stu-id="8b17e-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="8b17e-122">-Location</span><span class="sxs-lookup"><span data-stu-id="8b17e-122">-Location</span></span>
<span data-ttu-id="8b17e-123">Расположение для создания пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="8b17e-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="8b17e-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8b17e-124">-Name</span></span>
<span data-ttu-id="8b17e-125">Имя пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="8b17e-125">The name of the instance pool.</span></span>

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

### <span data-ttu-id="8b17e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b17e-126">-ResourceGroupName</span></span>
<span data-ttu-id="8b17e-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8b17e-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="8b17e-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8b17e-128">-SubnetId</span></span>
<span data-ttu-id="8b17e-129">Идентификатор подсети, используемый для создания пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="8b17e-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="8b17e-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="8b17e-130">-Tag</span></span>
<span data-ttu-id="8b17e-131">Теги, связываемые с экземпляром</span><span class="sxs-lookup"><span data-stu-id="8b17e-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="8b17e-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="8b17e-132">-VCore</span></span>
<span data-ttu-id="8b17e-133">Определяет, сколько VCore связать с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="8b17e-133">Determines how much VCore to associate with instance.</span></span>

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

### <span data-ttu-id="8b17e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b17e-134">-Confirm</span></span>
<span data-ttu-id="8b17e-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8b17e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b17e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b17e-136">-WhatIf</span></span>
<span data-ttu-id="8b17e-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8b17e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b17e-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8b17e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b17e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b17e-139">CommonParameters</span></span>
<span data-ttu-id="8b17e-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b17e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b17e-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b17e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b17e-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b17e-142">INPUTS</span></span>

### <span data-ttu-id="8b17e-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="8b17e-143">None</span></span>

## <span data-ttu-id="8b17e-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b17e-144">OUTPUTS</span></span>

### <span data-ttu-id="8b17e-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="8b17e-145">System.Object</span></span>
## <span data-ttu-id="8b17e-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b17e-146">NOTES</span></span>

## <span data-ttu-id="8b17e-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b17e-147">RELATED LINKS</span></span>
