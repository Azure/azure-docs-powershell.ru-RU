---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 3e28cacc8dc6a27f20a93beb3e48ddcc0d0697cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566535"
---
# <span data-ttu-id="6ee45-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6ee45-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="6ee45-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ee45-102">SYNOPSIS</span></span>
<span data-ttu-id="6ee45-103">Обновляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="6ee45-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ee45-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ee45-104">SYNTAX</span></span>

### <span data-ttu-id="6ee45-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ee45-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ee45-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="6ee45-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ee45-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ee45-107">DESCRIPTION</span></span>
<span data-ttu-id="6ee45-108">Командлет **Update-AzureRmAvailabilitySet** обновляет группу доступности.</span><span class="sxs-lookup"><span data-stu-id="6ee45-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="6ee45-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ee45-109">EXAMPLES</span></span>

### <span data-ttu-id="6ee45-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6ee45-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="6ee45-111">Эта команда обновляет набор доступности с именем "AvSet01" в группе ресурсов с именем "ResourceGroup01" в управляемый набор доступности.</span><span class="sxs-lookup"><span data-stu-id="6ee45-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="6ee45-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ee45-112">PARAMETERS</span></span>

### <span data-ttu-id="6ee45-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ee45-113">-AsJob</span></span>
<span data-ttu-id="6ee45-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="6ee45-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6ee45-115">-Группа доступности</span><span class="sxs-lookup"><span data-stu-id="6ee45-115">-AvailabilitySet</span></span>
<span data-ttu-id="6ee45-116">Указывает объект группы доступности, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="6ee45-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="6ee45-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ee45-117">-DefaultProfile</span></span>
<span data-ttu-id="6ee45-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ee45-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ee45-119">-Managed</span><span class="sxs-lookup"><span data-stu-id="6ee45-119">-Managed</span></span>
<span data-ttu-id="6ee45-120">Управляемая установка доступности</span><span class="sxs-lookup"><span data-stu-id="6ee45-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="6ee45-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="6ee45-121">-Sku</span></span>
<span data-ttu-id="6ee45-122">Название SKU</span><span class="sxs-lookup"><span data-stu-id="6ee45-122">The Name of Sku</span></span>

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

### <span data-ttu-id="6ee45-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="6ee45-123">-Tag</span></span>
<span data-ttu-id="6ee45-124">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="6ee45-124">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="6ee45-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ee45-125">-Confirm</span></span>
<span data-ttu-id="6ee45-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6ee45-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ee45-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ee45-127">-WhatIf</span></span>
<span data-ttu-id="6ee45-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6ee45-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ee45-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6ee45-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ee45-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ee45-130">CommonParameters</span></span>
<span data-ttu-id="6ee45-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ee45-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ee45-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ee45-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ee45-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ee45-133">INPUTS</span></span>

### <span data-ttu-id="6ee45-134">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6ee45-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="6ee45-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ee45-135">OUTPUTS</span></span>

### <span data-ttu-id="6ee45-136">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6ee45-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="6ee45-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ee45-137">NOTES</span></span>

## <span data-ttu-id="6ee45-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ee45-138">RELATED LINKS</span></span>
