---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: e8bd36cd9c054d155dca034f49be8cd422a244bc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910448"
---
# <span data-ttu-id="dadc2-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="dadc2-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="dadc2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dadc2-102">SYNOPSIS</span></span>
<span data-ttu-id="dadc2-103">Обновляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="dadc2-103">Updates an availability set.</span></span>

## <span data-ttu-id="dadc2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dadc2-104">SYNTAX</span></span>

### <span data-ttu-id="dadc2-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="dadc2-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dadc2-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="dadc2-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dadc2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dadc2-107">DESCRIPTION</span></span>
<span data-ttu-id="dadc2-108">Командлет **Update-AzAvailabilitySet** обновляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="dadc2-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="dadc2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dadc2-109">EXAMPLES</span></span>

### <span data-ttu-id="dadc2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dadc2-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="dadc2-111">Эта команда обновляет набор доступности с именем "AvSet01" в группе ресурсов с именем "ResourceGroup01" в управляемый набор доступности.</span><span class="sxs-lookup"><span data-stu-id="dadc2-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="dadc2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dadc2-112">PARAMETERS</span></span>

### <span data-ttu-id="dadc2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dadc2-113">-AsJob</span></span>
<span data-ttu-id="dadc2-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="dadc2-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="dadc2-115">-Группа доступности</span><span class="sxs-lookup"><span data-stu-id="dadc2-115">-AvailabilitySet</span></span>
<span data-ttu-id="dadc2-116">Указывает объект группы доступности, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="dadc2-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="dadc2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dadc2-117">-DefaultProfile</span></span>
<span data-ttu-id="dadc2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dadc2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dadc2-119">-Managed</span><span class="sxs-lookup"><span data-stu-id="dadc2-119">-Managed</span></span>
<span data-ttu-id="dadc2-120">Управляемая установка доступности</span><span class="sxs-lookup"><span data-stu-id="dadc2-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="dadc2-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="dadc2-121">-Sku</span></span>
<span data-ttu-id="dadc2-122">Название SKU</span><span class="sxs-lookup"><span data-stu-id="dadc2-122">The Name of Sku</span></span>

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

### <span data-ttu-id="dadc2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dadc2-123">-Confirm</span></span>
<span data-ttu-id="dadc2-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dadc2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dadc2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dadc2-125">-WhatIf</span></span>
<span data-ttu-id="dadc2-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dadc2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dadc2-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dadc2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dadc2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dadc2-128">CommonParameters</span></span>
<span data-ttu-id="dadc2-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dadc2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dadc2-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dadc2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dadc2-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dadc2-131">INPUTS</span></span>

### <span data-ttu-id="dadc2-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="dadc2-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="dadc2-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dadc2-133">OUTPUTS</span></span>

### <span data-ttu-id="dadc2-134">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="dadc2-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="dadc2-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="dadc2-135">NOTES</span></span>

## <span data-ttu-id="dadc2-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dadc2-136">RELATED LINKS</span></span>

