---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 1b4f405e9bf6377855439d1f6d3cad9f0538920f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505908"
---
# <span data-ttu-id="bef87-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="bef87-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="bef87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bef87-102">SYNOPSIS</span></span>
<span data-ttu-id="bef87-103">Создание пула экземпляров SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bef87-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="bef87-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bef87-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bef87-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bef87-105">DESCRIPTION</span></span>
<span data-ttu-id="bef87-106">С его использованием создается пул экземпляров Azure SQL **AzSqlInstancePool.**</span><span class="sxs-lookup"><span data-stu-id="bef87-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="bef87-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bef87-107">EXAMPLES</span></span>

### <span data-ttu-id="bef87-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bef87-108">Example 1</span></span>
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

<span data-ttu-id="bef87-109">Эта команда создает новый пул экземпляров Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bef87-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="bef87-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bef87-110">PARAMETERS</span></span>

### <span data-ttu-id="bef87-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bef87-111">-AsJob</span></span>
<span data-ttu-id="bef87-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bef87-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bef87-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="bef87-113">-ComputeGeneration</span></span>
<span data-ttu-id="bef87-114">Генерация компьютеров для пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="bef87-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="bef87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bef87-115">-DefaultProfile</span></span>
<span data-ttu-id="bef87-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bef87-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bef87-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="bef87-117">-Edition</span></span>
<span data-ttu-id="bef87-118">Выпуск для пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="bef87-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="bef87-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="bef87-119">-LicenseType</span></span>
<span data-ttu-id="bef87-120">Определяет тип лицензии.</span><span class="sxs-lookup"><span data-stu-id="bef87-120">Determines which License Type to use.</span></span>
<span data-ttu-id="bef87-121">Возможные значения: BasePrice (со скидкой AHB) и LicenseIncluded (без скидки AHB).</span><span class="sxs-lookup"><span data-stu-id="bef87-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="bef87-122">-Location</span><span class="sxs-lookup"><span data-stu-id="bef87-122">-Location</span></span>
<span data-ttu-id="bef87-123">Расположение для создания пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="bef87-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="bef87-124">-Name</span><span class="sxs-lookup"><span data-stu-id="bef87-124">-Name</span></span>
<span data-ttu-id="bef87-125">Имя пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="bef87-125">The name of the instance pool.</span></span>

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

### <span data-ttu-id="bef87-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bef87-126">-ResourceGroupName</span></span>
<span data-ttu-id="bef87-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bef87-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="bef87-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bef87-128">-SubnetId</span></span>
<span data-ttu-id="bef87-129">ИД подсети, который используется для создания пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="bef87-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="bef87-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="bef87-130">-Tag</span></span>
<span data-ttu-id="bef87-131">Теги, которые нужно связать с экземпляром</span><span class="sxs-lookup"><span data-stu-id="bef87-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="bef87-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="bef87-132">-VCore</span></span>
<span data-ttu-id="bef87-133">Определяет, сколько VCore нужно связать с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="bef87-133">Determines how much VCore to associate with instance.</span></span>

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

### <span data-ttu-id="bef87-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bef87-134">-Confirm</span></span>
<span data-ttu-id="bef87-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bef87-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bef87-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bef87-136">-WhatIf</span></span>
<span data-ttu-id="bef87-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bef87-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bef87-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bef87-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bef87-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef87-139">CommonParameters</span></span>
<span data-ttu-id="bef87-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bef87-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef87-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bef87-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef87-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bef87-142">INPUTS</span></span>

### <span data-ttu-id="bef87-143">Нет</span><span class="sxs-lookup"><span data-stu-id="bef87-143">None</span></span>

## <span data-ttu-id="bef87-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bef87-144">OUTPUTS</span></span>

### <span data-ttu-id="bef87-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="bef87-145">System.Object</span></span>
## <span data-ttu-id="bef87-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bef87-146">NOTES</span></span>

## <span data-ttu-id="bef87-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bef87-147">RELATED LINKS</span></span>
