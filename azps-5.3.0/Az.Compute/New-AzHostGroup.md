---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 2fdb5317504bb1bc08ed45e8224a30a61cca8e8c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509098"
---
# <span data-ttu-id="83bfa-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="83bfa-101">New-AzHostGroup</span></span>

## <span data-ttu-id="83bfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="83bfa-103">Создает группу хостов.</span><span class="sxs-lookup"><span data-stu-id="83bfa-103">Creates a host group.</span></span>

## <span data-ttu-id="83bfa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="83bfa-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83bfa-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83bfa-105">DESCRIPTION</span></span>
<span data-ttu-id="83bfa-106">Этот cmdlet создаст группу host (Хост).</span><span class="sxs-lookup"><span data-stu-id="83bfa-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="83bfa-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="83bfa-107">EXAMPLES</span></span>

### <span data-ttu-id="83bfa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="83bfa-108">Example 1</span></span>
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

<span data-ttu-id="83bfa-109">Эта команда создает группу хостов в заданном расположении и зоне.</span><span class="sxs-lookup"><span data-stu-id="83bfa-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="83bfa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83bfa-110">PARAMETERS</span></span>

### <span data-ttu-id="83bfa-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83bfa-111">-AsJob</span></span>
<span data-ttu-id="83bfa-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="83bfa-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="83bfa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83bfa-113">-DefaultProfile</span></span>
<span data-ttu-id="83bfa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83bfa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83bfa-115">-Location</span><span class="sxs-lookup"><span data-stu-id="83bfa-115">-Location</span></span>
<span data-ttu-id="83bfa-116">Определяет расположение.</span><span class="sxs-lookup"><span data-stu-id="83bfa-116">Specifies location.</span></span>

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

### <span data-ttu-id="83bfa-117">-Name</span><span class="sxs-lookup"><span data-stu-id="83bfa-117">-Name</span></span>
<span data-ttu-id="83bfa-118">Указывает имя группы хостов.</span><span class="sxs-lookup"><span data-stu-id="83bfa-118">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="83bfa-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="83bfa-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="83bfa-120">Количество доменов ошибок, которые может использовать группа хостов.</span><span class="sxs-lookup"><span data-stu-id="83bfa-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="83bfa-121">Минимальное значение — 1, максимальное — 3.</span><span class="sxs-lookup"><span data-stu-id="83bfa-121">The minimum value is 1 and the maximum value is 3.</span></span>

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

### <span data-ttu-id="83bfa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83bfa-122">-ResourceGroupName</span></span>
<span data-ttu-id="83bfa-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83bfa-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="83bfa-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="83bfa-124">-Tag</span></span>
<span data-ttu-id="83bfa-125">Определяет теги.</span><span class="sxs-lookup"><span data-stu-id="83bfa-125">Specifies Tags</span></span>

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

### <span data-ttu-id="83bfa-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="83bfa-126">-Zone</span></span>
<span data-ttu-id="83bfa-127">Определяет зоны группы хостов.</span><span class="sxs-lookup"><span data-stu-id="83bfa-127">Specifies Zones of the host group.</span></span>

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

### <span data-ttu-id="83bfa-128">-SupportAutomaticPlacement</span><span class="sxs-lookup"><span data-stu-id="83bfa-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="83bfa-129">Указывает, будет ли HostGroup автоматически размещены VM-ов.</span><span class="sxs-lookup"><span data-stu-id="83bfa-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="83bfa-130">Автоматическое размещение означает, что такие VMs размещаются на выделенных hosts, выбранных Azure, в выделенной группе хостов.</span><span class="sxs-lookup"><span data-stu-id="83bfa-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="83bfa-131">Если он не задан, значение по умолчанию будет истинным.</span><span class="sxs-lookup"><span data-stu-id="83bfa-131">If not specified, default value will be true.</span></span>

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


### <span data-ttu-id="83bfa-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83bfa-132">-Confirm</span></span>
<span data-ttu-id="83bfa-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83bfa-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83bfa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83bfa-134">-WhatIf</span></span>
<span data-ttu-id="83bfa-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83bfa-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83bfa-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="83bfa-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83bfa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83bfa-137">CommonParameters</span></span>
<span data-ttu-id="83bfa-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83bfa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83bfa-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83bfa-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83bfa-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83bfa-140">INPUTS</span></span>

### <span data-ttu-id="83bfa-141">System.String</span><span class="sxs-lookup"><span data-stu-id="83bfa-141">System.String</span></span>

## <span data-ttu-id="83bfa-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="83bfa-142">OUTPUTS</span></span>

### <span data-ttu-id="83bfa-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="83bfa-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="83bfa-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="83bfa-144">NOTES</span></span>

## <span data-ttu-id="83bfa-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83bfa-145">RELATED LINKS</span></span>