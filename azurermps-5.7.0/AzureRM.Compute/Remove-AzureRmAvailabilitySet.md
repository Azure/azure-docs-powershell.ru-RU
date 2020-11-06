---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 467b430232805da132b568918ac0a1ed7b6db5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559175"
---
# <span data-ttu-id="d6c3b-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d6c3b-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="d6c3b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="d6c3b-103">Удаляет группу доступности из Azure.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6c3b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6c3b-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6c3b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6c3b-105">DESCRIPTION</span></span>
<span data-ttu-id="d6c3b-106">Командлет **Remove-AzureRmAvailabilitySet** удаляет группу доступности из Azure.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="d6c3b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6c3b-107">EXAMPLES</span></span>

### <span data-ttu-id="d6c3b-108">Пример 1: Удаление группы доступности</span><span class="sxs-lookup"><span data-stu-id="d6c3b-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="d6c3b-109">Эта команда удаляет группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d6c3b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6c3b-110">PARAMETERS</span></span>

### <span data-ttu-id="d6c3b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d6c3b-111">-Force</span></span>
<span data-ttu-id="d6c3b-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6c3b-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d6c3b-113">-Name</span></span>
<span data-ttu-id="d6c3b-114">Имя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-114">The availability set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6c3b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6c3b-115">-ResourceGroupName</span></span>
<span data-ttu-id="d6c3b-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6c3b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6c3b-117">-Confirm</span></span>
<span data-ttu-id="d6c3b-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6c3b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6c3b-119">-WhatIf</span></span>
<span data-ttu-id="d6c3b-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d6c3b-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6c3b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6c3b-122">CommonParameters</span></span>
<span data-ttu-id="d6c3b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6c3b-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6c3b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6c3b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6c3b-125">INPUTS</span></span>

### <span data-ttu-id="d6c3b-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="d6c3b-126">None</span></span>
<span data-ttu-id="d6c3b-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d6c3b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6c3b-128">OUTPUTS</span></span>

## <span data-ttu-id="d6c3b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6c3b-129">NOTES</span></span>

## <span data-ttu-id="d6c3b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6c3b-130">RELATED LINKS</span></span>

[<span data-ttu-id="d6c3b-131">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d6c3b-131">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="d6c3b-132">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d6c3b-132">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


