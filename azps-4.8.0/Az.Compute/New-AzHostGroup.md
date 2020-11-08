---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 2fdb5317504bb1bc08ed45e8224a30a61cca8e8c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079121"
---
# <span data-ttu-id="2e7a9-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="2e7a9-101">New-AzHostGroup</span></span>

## <span data-ttu-id="2e7a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="2e7a9-103">Создание группы узлов.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-103">Creates a host group.</span></span>

## <span data-ttu-id="2e7a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e7a9-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e7a9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e7a9-105">DESCRIPTION</span></span>
<span data-ttu-id="2e7a9-106">Этот командлет создаст группу узлов.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="2e7a9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e7a9-107">EXAMPLES</span></span>

### <span data-ttu-id="2e7a9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2e7a9-108">Example 1</span></span>
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

<span data-ttu-id="2e7a9-109">Эта команда создает группу узлов в указанном месте и зоне.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="2e7a9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e7a9-110">PARAMETERS</span></span>

### <span data-ttu-id="2e7a9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e7a9-111">-AsJob</span></span>
<span data-ttu-id="2e7a9-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2e7a9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e7a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e7a9-113">-DefaultProfile</span></span>
<span data-ttu-id="2e7a9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e7a9-115">-Location</span><span class="sxs-lookup"><span data-stu-id="2e7a9-115">-Location</span></span>
<span data-ttu-id="2e7a9-116">Указывает расположение.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-116">Specifies location.</span></span>

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

### <span data-ttu-id="2e7a9-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2e7a9-117">-Name</span></span>
<span data-ttu-id="2e7a9-118">Указывает имя группы узлов.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-118">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="2e7a9-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="2e7a9-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="2e7a9-120">Указывает количество доменов сбоя, которые может занимать группа узлов.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="2e7a9-121">Минимальное значение равно 1, а максимальное значение — 3.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-121">The minimum value is 1 and the maximum value is 3.</span></span>

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

### <span data-ttu-id="2e7a9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e7a9-122">-ResourceGroupName</span></span>
<span data-ttu-id="2e7a9-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="2e7a9-124">-Тег</span><span class="sxs-lookup"><span data-stu-id="2e7a9-124">-Tag</span></span>
<span data-ttu-id="2e7a9-125">Указывает Теги</span><span class="sxs-lookup"><span data-stu-id="2e7a9-125">Specifies Tags</span></span>

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

### <span data-ttu-id="2e7a9-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="2e7a9-126">-Zone</span></span>
<span data-ttu-id="2e7a9-127">Задает зоны для группы узлов.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-127">Specifies Zones of the host group.</span></span>

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

### <span data-ttu-id="2e7a9-128">-SupportAutomaticPlacement</span><span class="sxs-lookup"><span data-stu-id="2e7a9-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="2e7a9-129">Указывает, будет ли HostGroup включать функцию автоматического размещения ВМ.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="2e7a9-130">Автоматическое размещение означает, что эти виртуальные машины размещаются на выделенных узлах, выбранном в Azure, в разделе выделенная группа узлов.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="2e7a9-131">Если он не указан, значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-131">If not specified, default value will be true.</span></span>

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


### <span data-ttu-id="2e7a9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e7a9-132">-Confirm</span></span>
<span data-ttu-id="2e7a9-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e7a9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e7a9-134">-WhatIf</span></span>
<span data-ttu-id="2e7a9-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e7a9-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e7a9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e7a9-137">CommonParameters</span></span>
<span data-ttu-id="2e7a9-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e7a9-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e7a9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e7a9-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e7a9-140">INPUTS</span></span>

### <span data-ttu-id="2e7a9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2e7a9-141">System.String</span></span>

## <span data-ttu-id="2e7a9-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e7a9-142">OUTPUTS</span></span>

### <span data-ttu-id="2e7a9-143">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="2e7a9-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="2e7a9-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e7a9-144">NOTES</span></span>

## <span data-ttu-id="2e7a9-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e7a9-145">RELATED LINKS</span></span>
