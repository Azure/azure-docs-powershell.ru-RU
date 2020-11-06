---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: c7b33e3f2afd013b6fd54f6d425c0aa1d0d08bd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569596"
---
# <span data-ttu-id="92418-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="92418-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="92418-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92418-102">SYNOPSIS</span></span>
<span data-ttu-id="92418-103">Обновляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="92418-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92418-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92418-104">SYNTAX</span></span>

### <span data-ttu-id="92418-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="92418-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92418-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="92418-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92418-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92418-107">DESCRIPTION</span></span>
<span data-ttu-id="92418-108">Командлет **Update-AzureRmAvailabilitySet** обновляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="92418-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="92418-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92418-109">EXAMPLES</span></span>

### <span data-ttu-id="92418-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="92418-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="92418-111">Эта команда обновляет набор доступности с именем "AvSet01" в группе ресурсов с именем "ResourceGroup01" в управляемый набор доступности.</span><span class="sxs-lookup"><span data-stu-id="92418-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="92418-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92418-112">PARAMETERS</span></span>

### <span data-ttu-id="92418-113">-Группа доступности</span><span class="sxs-lookup"><span data-stu-id="92418-113">-AvailabilitySet</span></span>
<span data-ttu-id="92418-114">Указывает объект группы доступности, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="92418-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="92418-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92418-115">-DefaultProfile</span></span>
<span data-ttu-id="92418-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92418-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92418-117">-Managed</span><span class="sxs-lookup"><span data-stu-id="92418-117">-Managed</span></span>
<span data-ttu-id="92418-118">Управляемая установка доступности</span><span class="sxs-lookup"><span data-stu-id="92418-118">Managed Availability Set</span></span>

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

### <span data-ttu-id="92418-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="92418-119">-Sku</span></span>
<span data-ttu-id="92418-120">Название SKU</span><span class="sxs-lookup"><span data-stu-id="92418-120">The Name of Sku</span></span>

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

### <span data-ttu-id="92418-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92418-121">-Confirm</span></span>
<span data-ttu-id="92418-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="92418-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92418-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92418-123">-WhatIf</span></span>
<span data-ttu-id="92418-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="92418-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92418-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="92418-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92418-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92418-126">CommonParameters</span></span>
<span data-ttu-id="92418-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92418-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92418-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92418-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92418-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92418-129">INPUTS</span></span>

### <span data-ttu-id="92418-130">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="92418-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="92418-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92418-131">OUTPUTS</span></span>

### <span data-ttu-id="92418-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="92418-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="92418-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="92418-133">NOTES</span></span>

## <span data-ttu-id="92418-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92418-134">RELATED LINKS</span></span>

