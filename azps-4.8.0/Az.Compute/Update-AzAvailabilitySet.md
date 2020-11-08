---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 689336bb7fbb7ef59be96a5bd6bcbfe49ddb64c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078102"
---
# <span data-ttu-id="49843-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="49843-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="49843-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49843-102">SYNOPSIS</span></span>
<span data-ttu-id="49843-103">Обновляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="49843-103">Updates an availability set.</span></span>

## <span data-ttu-id="49843-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49843-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49843-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49843-105">DESCRIPTION</span></span>
<span data-ttu-id="49843-106">Командлет **Update-AzAvailabilitySet** обновляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="49843-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="49843-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49843-107">EXAMPLES</span></span>

### <span data-ttu-id="49843-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="49843-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="49843-109">Эта команда обновляет набор доступности с именем "AvSet01" в группе ресурсов с именем "ResourceGroup01" в управляемый набор доступности.</span><span class="sxs-lookup"><span data-stu-id="49843-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="49843-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49843-110">PARAMETERS</span></span>

### <span data-ttu-id="49843-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49843-111">-AsJob</span></span>
<span data-ttu-id="49843-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="49843-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="49843-113">-Группа доступности</span><span class="sxs-lookup"><span data-stu-id="49843-113">-AvailabilitySet</span></span>
<span data-ttu-id="49843-114">Указывает объект группы доступности, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="49843-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="49843-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49843-115">-DefaultProfile</span></span>
<span data-ttu-id="49843-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49843-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49843-117">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="49843-117">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="49843-118">Идентификатор ресурса группы размещения близкого взаимодействия для использования с этой группой доступности.</span><span class="sxs-lookup"><span data-stu-id="49843-118">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="49843-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="49843-119">-Sku</span></span>
<span data-ttu-id="49843-120">Название SKU</span><span class="sxs-lookup"><span data-stu-id="49843-120">The Name of Sku</span></span>

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

### <span data-ttu-id="49843-121">-Тег</span><span class="sxs-lookup"><span data-stu-id="49843-121">-Tag</span></span>
<span data-ttu-id="49843-122">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="49843-122">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="49843-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49843-123">-Confirm</span></span>
<span data-ttu-id="49843-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="49843-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49843-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49843-125">-WhatIf</span></span>
<span data-ttu-id="49843-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="49843-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49843-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49843-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49843-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49843-128">CommonParameters</span></span>
<span data-ttu-id="49843-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49843-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49843-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49843-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49843-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49843-131">INPUTS</span></span>

### <span data-ttu-id="49843-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="49843-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="49843-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49843-133">OUTPUTS</span></span>

### <span data-ttu-id="49843-134">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="49843-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="49843-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="49843-135">NOTES</span></span>

## <span data-ttu-id="49843-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49843-136">RELATED LINKS</span></span>
