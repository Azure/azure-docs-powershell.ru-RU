---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: f7d9181b5ec79434928fc8d291025aea9480b8e9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915338"
---
# <span data-ttu-id="79309-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="79309-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="79309-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79309-102">SYNOPSIS</span></span>
<span data-ttu-id="79309-103">Обновляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="79309-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79309-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79309-104">SYNTAX</span></span>

### <span data-ttu-id="79309-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="79309-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79309-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="79309-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79309-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79309-107">DESCRIPTION</span></span>
<span data-ttu-id="79309-108">Командлет **Update-AzureRmAvailabilitySet** обновляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="79309-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="79309-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79309-109">EXAMPLES</span></span>

### <span data-ttu-id="79309-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="79309-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="79309-111">Эта команда обновляет набор доступности с именем "AvSet01" в группе ресурсов с именем "ResourceGroup01" в управляемый набор доступности.</span><span class="sxs-lookup"><span data-stu-id="79309-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="79309-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79309-112">PARAMETERS</span></span>

### <span data-ttu-id="79309-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79309-113">-AsJob</span></span>
<span data-ttu-id="79309-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="79309-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79309-115">-Группа доступности</span><span class="sxs-lookup"><span data-stu-id="79309-115">-AvailabilitySet</span></span>
<span data-ttu-id="79309-116">Указывает объект группы доступности, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="79309-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="79309-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79309-117">-DefaultProfile</span></span>
<span data-ttu-id="79309-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79309-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79309-119">-Managed</span><span class="sxs-lookup"><span data-stu-id="79309-119">-Managed</span></span>
<span data-ttu-id="79309-120">Управляемая установка доступности</span><span class="sxs-lookup"><span data-stu-id="79309-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="79309-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="79309-121">-Sku</span></span>
<span data-ttu-id="79309-122">Название SKU</span><span class="sxs-lookup"><span data-stu-id="79309-122">The Name of Sku</span></span>

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

### <span data-ttu-id="79309-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79309-123">-Confirm</span></span>
<span data-ttu-id="79309-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="79309-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79309-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79309-125">-WhatIf</span></span>
<span data-ttu-id="79309-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79309-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79309-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79309-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79309-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79309-128">CommonParameters</span></span>
<span data-ttu-id="79309-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79309-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79309-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79309-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79309-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79309-131">INPUTS</span></span>

### <span data-ttu-id="79309-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="79309-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="79309-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79309-133">OUTPUTS</span></span>

### <span data-ttu-id="79309-134">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="79309-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="79309-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="79309-135">NOTES</span></span>

## <span data-ttu-id="79309-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79309-136">RELATED LINKS</span></span>

