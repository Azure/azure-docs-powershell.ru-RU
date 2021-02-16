---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 689336bb7fbb7ef59be96a5bd6bcbfe49ddb64c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211481"
---
# <span data-ttu-id="887f1-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="887f1-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="887f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="887f1-102">SYNOPSIS</span></span>
<span data-ttu-id="887f1-103">Обновляет набор доступности.</span><span class="sxs-lookup"><span data-stu-id="887f1-103">Updates an availability set.</span></span>

## <span data-ttu-id="887f1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="887f1-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="887f1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="887f1-105">DESCRIPTION</span></span>
<span data-ttu-id="887f1-106">Набор **обновлений для AzAvailabilitySet** обновляет набор доступности.</span><span class="sxs-lookup"><span data-stu-id="887f1-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="887f1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="887f1-107">EXAMPLES</span></span>

### <span data-ttu-id="887f1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="887f1-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="887f1-109">Эта команда обновляет набор доступности с именем "AvSet01" в группе ресурсов "Группа ресурсов01" на управляемый набор.</span><span class="sxs-lookup"><span data-stu-id="887f1-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="887f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="887f1-110">PARAMETERS</span></span>

### <span data-ttu-id="887f1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="887f1-111">-AsJob</span></span>
<span data-ttu-id="887f1-112">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="887f1-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="887f1-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="887f1-113">-AvailabilitySet</span></span>
<span data-ttu-id="887f1-114">Определяет обновляемый объект набора доступности.</span><span class="sxs-lookup"><span data-stu-id="887f1-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="887f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="887f1-115">-DefaultProfile</span></span>
<span data-ttu-id="887f1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="887f1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="887f1-117">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="887f1-117">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="887f1-118">ИД ресурса группы расположения расположения близости, который можно использовать с этим набором доступности.</span><span class="sxs-lookup"><span data-stu-id="887f1-118">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="887f1-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="887f1-119">-Sku</span></span>
<span data-ttu-id="887f1-120">Название SKU</span><span class="sxs-lookup"><span data-stu-id="887f1-120">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887f1-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="887f1-121">-Tag</span></span>
<span data-ttu-id="887f1-122">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="887f1-122">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="887f1-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="887f1-123">-Confirm</span></span>
<span data-ttu-id="887f1-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="887f1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="887f1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="887f1-125">-WhatIf</span></span>
<span data-ttu-id="887f1-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="887f1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="887f1-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="887f1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="887f1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="887f1-128">CommonParameters</span></span>
<span data-ttu-id="887f1-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="887f1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="887f1-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="887f1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="887f1-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="887f1-131">INPUTS</span></span>

### <span data-ttu-id="887f1-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="887f1-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="887f1-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="887f1-133">OUTPUTS</span></span>

### <span data-ttu-id="887f1-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="887f1-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="887f1-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="887f1-135">NOTES</span></span>

## <span data-ttu-id="887f1-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="887f1-136">RELATED LINKS</span></span>
