---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: 4051cbb697625f527afdf2e189953c4d6e776214
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901074"
---
# <span data-ttu-id="1f90c-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1f90c-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="1f90c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f90c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f90c-103">Обновляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="1f90c-103">Updates an availability set.</span></span>

## <span data-ttu-id="1f90c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f90c-104">SYNTAX</span></span>

### <span data-ttu-id="1f90c-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f90c-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f90c-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="1f90c-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f90c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f90c-107">DESCRIPTION</span></span>
<span data-ttu-id="1f90c-108">Командлет **Update-AzAvailabilitySet** обновляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="1f90c-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="1f90c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f90c-109">EXAMPLES</span></span>

### <span data-ttu-id="1f90c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1f90c-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="1f90c-111">Эта команда обновляет набор доступности с именем "AvSet01" в группе ресурсов с именем "ResourceGroup01" в управляемый набор доступности.</span><span class="sxs-lookup"><span data-stu-id="1f90c-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="1f90c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f90c-112">PARAMETERS</span></span>

### <span data-ttu-id="1f90c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f90c-113">-AsJob</span></span>
<span data-ttu-id="1f90c-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="1f90c-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1f90c-115">-Группа доступности</span><span class="sxs-lookup"><span data-stu-id="1f90c-115">-AvailabilitySet</span></span>
<span data-ttu-id="1f90c-116">Указывает объект группы доступности, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="1f90c-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="1f90c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f90c-117">-DefaultProfile</span></span>
<span data-ttu-id="1f90c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f90c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f90c-119">-Managed</span><span class="sxs-lookup"><span data-stu-id="1f90c-119">-Managed</span></span>
<span data-ttu-id="1f90c-120">Управляемая установка доступности</span><span class="sxs-lookup"><span data-stu-id="1f90c-120">Managed Availability Set</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f90c-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="1f90c-121">-Sku</span></span>
<span data-ttu-id="1f90c-122">Название SKU</span><span class="sxs-lookup"><span data-stu-id="1f90c-122">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: SkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f90c-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="1f90c-123">-Tag</span></span>
<span data-ttu-id="1f90c-124">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="1f90c-124">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="1f90c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f90c-125">-Confirm</span></span>
<span data-ttu-id="1f90c-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f90c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f90c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f90c-127">-WhatIf</span></span>
<span data-ttu-id="1f90c-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1f90c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f90c-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f90c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f90c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f90c-130">CommonParameters</span></span>
<span data-ttu-id="1f90c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f90c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f90c-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f90c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f90c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f90c-133">INPUTS</span></span>

### <span data-ttu-id="1f90c-134">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1f90c-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="1f90c-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f90c-135">OUTPUTS</span></span>

### <span data-ttu-id="1f90c-136">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1f90c-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="1f90c-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f90c-137">NOTES</span></span>

## <span data-ttu-id="1f90c-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f90c-138">RELATED LINKS</span></span>
