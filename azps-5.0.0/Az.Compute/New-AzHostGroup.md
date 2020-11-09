---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 2fdb5317504bb1bc08ed45e8224a30a61cca8e8c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247067"
---
# <span data-ttu-id="a2052-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="a2052-101">New-AzHostGroup</span></span>

## <span data-ttu-id="a2052-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2052-102">SYNOPSIS</span></span>
<span data-ttu-id="a2052-103">Создание группы узлов.</span><span class="sxs-lookup"><span data-stu-id="a2052-103">Creates a host group.</span></span>

## <span data-ttu-id="a2052-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2052-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2052-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2052-105">DESCRIPTION</span></span>
<span data-ttu-id="a2052-106">Этот командлет создаст группу узлов.</span><span class="sxs-lookup"><span data-stu-id="a2052-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="a2052-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2052-107">EXAMPLES</span></span>

### <span data-ttu-id="a2052-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2052-108">Example 1</span></span>
```
PS C:\> New-AzHostGroup -ResourceGroupName $resourceGroupName -Name $hostGroupName -Location $location -Zone $zone

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="a2052-109">Эта команда создает группу узлов в указанном месте и зоне.</span><span class="sxs-lookup"><span data-stu-id="a2052-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="a2052-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2052-110">PARAMETERS</span></span>

### <span data-ttu-id="a2052-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2052-111">-AsJob</span></span>
<span data-ttu-id="a2052-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a2052-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2052-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2052-113">-DefaultProfile</span></span>
<span data-ttu-id="a2052-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2052-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2052-115">-Location</span><span class="sxs-lookup"><span data-stu-id="a2052-115">-Location</span></span>
<span data-ttu-id="a2052-116">Указывает расположение.</span><span class="sxs-lookup"><span data-stu-id="a2052-116">Specifies location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2052-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a2052-117">-Name</span></span>
<span data-ttu-id="a2052-118">Указывает имя группы узлов.</span><span class="sxs-lookup"><span data-stu-id="a2052-118">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2052-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="a2052-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="a2052-120">Указывает количество доменов сбоя, которые может занимать группа узлов.</span><span class="sxs-lookup"><span data-stu-id="a2052-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="a2052-121">Минимальное значение равно 1, а максимальное значение — 3.</span><span class="sxs-lookup"><span data-stu-id="a2052-121">The minimum value is 1 and the maximum value is 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2052-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2052-122">-ResourceGroupName</span></span>
<span data-ttu-id="a2052-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2052-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2052-124">-Тег</span><span class="sxs-lookup"><span data-stu-id="a2052-124">-Tag</span></span>
<span data-ttu-id="a2052-125">Указывает Теги</span><span class="sxs-lookup"><span data-stu-id="a2052-125">Specifies Tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2052-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="a2052-126">-Zone</span></span>
<span data-ttu-id="a2052-127">Задает зоны для группы узлов.</span><span class="sxs-lookup"><span data-stu-id="a2052-127">Specifies Zones of the host group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2052-128">-SupportAutomaticPlacement</span><span class="sxs-lookup"><span data-stu-id="a2052-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="a2052-129">Указывает, будет ли HostGroup включать функцию автоматического размещения ВМ.</span><span class="sxs-lookup"><span data-stu-id="a2052-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="a2052-130">Автоматическое размещение означает, что эти виртуальные машины размещаются на выделенных узлах, выбранном в Azure, в разделе выделенная группа узлов.</span><span class="sxs-lookup"><span data-stu-id="a2052-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="a2052-131">Если он не указан, значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="a2052-131">If not specified, default value will be true.</span></span>

```yaml
Type: bool
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="a2052-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2052-132">-Confirm</span></span>
<span data-ttu-id="a2052-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a2052-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2052-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2052-134">-WhatIf</span></span>
<span data-ttu-id="a2052-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a2052-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2052-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a2052-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2052-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2052-137">CommonParameters</span></span>
<span data-ttu-id="a2052-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2052-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2052-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2052-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2052-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2052-140">INPUTS</span></span>

### <span data-ttu-id="a2052-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a2052-141">System.String</span></span>

## <span data-ttu-id="a2052-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2052-142">OUTPUTS</span></span>

### <span data-ttu-id="a2052-143">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="a2052-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="a2052-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2052-144">NOTES</span></span>

## <span data-ttu-id="a2052-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2052-145">RELATED LINKS</span></span>