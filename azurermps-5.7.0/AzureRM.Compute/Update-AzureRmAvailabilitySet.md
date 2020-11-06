---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 7e460c866912387b05a55b6fd228c65ef9b68348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557487"
---
# <span data-ttu-id="52cc3-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="52cc3-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="52cc3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="52cc3-103">Обновляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="52cc3-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52cc3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52cc3-104">SYNTAX</span></span>

### <span data-ttu-id="52cc3-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="52cc3-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52cc3-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="52cc3-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52cc3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52cc3-107">DESCRIPTION</span></span>
<span data-ttu-id="52cc3-108">Командлет **Update-AzureRmAvailabilitySet** обновляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="52cc3-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="52cc3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52cc3-109">EXAMPLES</span></span>

### <span data-ttu-id="52cc3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="52cc3-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="52cc3-111">Эта команда обновляет набор доступности с именем "AvSet01" в группе ресурсов с именем "ResourceGroup01" в управляемый набор доступности.</span><span class="sxs-lookup"><span data-stu-id="52cc3-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="52cc3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52cc3-112">PARAMETERS</span></span>

### <span data-ttu-id="52cc3-113">-Группа доступности</span><span class="sxs-lookup"><span data-stu-id="52cc3-113">-AvailabilitySet</span></span>
<span data-ttu-id="52cc3-114">Указывает объект группы доступности, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="52cc3-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52cc3-115">-Managed</span><span class="sxs-lookup"><span data-stu-id="52cc3-115">-Managed</span></span>
<span data-ttu-id="52cc3-116">Управляемая установка доступности</span><span class="sxs-lookup"><span data-stu-id="52cc3-116">Managed Availability Set</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52cc3-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="52cc3-117">-Sku</span></span>
<span data-ttu-id="52cc3-118">Название SKU</span><span class="sxs-lookup"><span data-stu-id="52cc3-118">The Name of Sku</span></span>

```yaml
Type: String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52cc3-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52cc3-119">-Confirm</span></span>
<span data-ttu-id="52cc3-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="52cc3-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52cc3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52cc3-121">-WhatIf</span></span>
<span data-ttu-id="52cc3-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="52cc3-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52cc3-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="52cc3-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52cc3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52cc3-124">CommonParameters</span></span>
<span data-ttu-id="52cc3-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52cc3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52cc3-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52cc3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52cc3-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52cc3-127">INPUTS</span></span>

### <span data-ttu-id="52cc3-128">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="52cc3-128">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="52cc3-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52cc3-129">OUTPUTS</span></span>

### <span data-ttu-id="52cc3-130">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="52cc3-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="52cc3-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="52cc3-131">NOTES</span></span>

## <span data-ttu-id="52cc3-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52cc3-132">RELATED LINKS</span></span>

