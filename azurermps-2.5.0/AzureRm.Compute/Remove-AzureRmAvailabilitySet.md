---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: cc8292940a252844c0aeabe820eec2e62055c954
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914557"
---
# <span data-ttu-id="fb4bc-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fb4bc-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="fb4bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb4bc-102">SYNOPSIS</span></span>
<span data-ttu-id="fb4bc-103">Удаляет группу доступности из Azure.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb4bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb4bc-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb4bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb4bc-105">DESCRIPTION</span></span>
<span data-ttu-id="fb4bc-106">Командлет **Remove-AzureRmAvailabilitySet** удаляет группу доступности из Azure.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="fb4bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb4bc-107">EXAMPLES</span></span>

### <span data-ttu-id="fb4bc-108">Пример 1: Удаление группы доступности</span><span class="sxs-lookup"><span data-stu-id="fb4bc-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="fb4bc-109">Эта команда удаляет группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="fb4bc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb4bc-110">PARAMETERS</span></span>

### <span data-ttu-id="fb4bc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb4bc-111">-AsJob</span></span>
<span data-ttu-id="fb4bc-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fb4bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb4bc-113">-DefaultProfile</span></span>
<span data-ttu-id="fb4bc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb4bc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fb4bc-115">-Force</span></span>
<span data-ttu-id="fb4bc-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fb4bc-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb4bc-117">-Name</span></span>
<span data-ttu-id="fb4bc-118">Имя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-118">The availability set name.</span></span>

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

### <span data-ttu-id="fb4bc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb4bc-119">-ResourceGroupName</span></span>
<span data-ttu-id="fb4bc-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fb4bc-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb4bc-121">-Confirm</span></span>
<span data-ttu-id="fb4bc-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb4bc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb4bc-123">-WhatIf</span></span>
<span data-ttu-id="fb4bc-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="fb4bc-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb4bc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb4bc-126">CommonParameters</span></span>
<span data-ttu-id="fb4bc-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb4bc-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb4bc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb4bc-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb4bc-129">INPUTS</span></span>

### <span data-ttu-id="fb4bc-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="fb4bc-130">None</span></span>
<span data-ttu-id="fb4bc-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb4bc-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb4bc-132">OUTPUTS</span></span>

### <span data-ttu-id="fb4bc-133">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fb4bc-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fb4bc-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb4bc-134">NOTES</span></span>

## <span data-ttu-id="fb4bc-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb4bc-135">RELATED LINKS</span></span>

[<span data-ttu-id="fb4bc-136">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fb4bc-136">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="fb4bc-137">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fb4bc-137">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


