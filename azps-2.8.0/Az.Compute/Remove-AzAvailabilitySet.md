---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 7dccf9410ff4d03503763354aabbe6b02d0c0c6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721806"
---
# <span data-ttu-id="b28ad-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b28ad-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="b28ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b28ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b28ad-103">Удаляет группу доступности из Azure.</span><span class="sxs-lookup"><span data-stu-id="b28ad-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="b28ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b28ad-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b28ad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b28ad-105">DESCRIPTION</span></span>
<span data-ttu-id="b28ad-106">Командлет **Remove-AzAvailabilitySet** удаляет группу доступности из Azure.</span><span class="sxs-lookup"><span data-stu-id="b28ad-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="b28ad-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b28ad-107">EXAMPLES</span></span>

### <span data-ttu-id="b28ad-108">Пример 1: Удаление группы доступности</span><span class="sxs-lookup"><span data-stu-id="b28ad-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="b28ad-109">Эта команда удаляет группу доступности с именем AvailabilitySet03 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b28ad-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="b28ad-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b28ad-110">PARAMETERS</span></span>

### <span data-ttu-id="b28ad-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b28ad-111">-AsJob</span></span>
<span data-ttu-id="b28ad-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="b28ad-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b28ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b28ad-113">-DefaultProfile</span></span>
<span data-ttu-id="b28ad-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b28ad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b28ad-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b28ad-115">-Force</span></span>
<span data-ttu-id="b28ad-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b28ad-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b28ad-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b28ad-117">-Name</span></span>
<span data-ttu-id="b28ad-118">Имя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="b28ad-118">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b28ad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b28ad-119">-ResourceGroupName</span></span>
<span data-ttu-id="b28ad-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b28ad-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b28ad-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b28ad-121">-Confirm</span></span>
<span data-ttu-id="b28ad-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b28ad-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b28ad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b28ad-123">-WhatIf</span></span>
<span data-ttu-id="b28ad-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b28ad-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b28ad-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b28ad-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b28ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b28ad-126">CommonParameters</span></span>
<span data-ttu-id="b28ad-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b28ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b28ad-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b28ad-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b28ad-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b28ad-129">INPUTS</span></span>

### <span data-ttu-id="b28ad-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b28ad-130">System.String</span></span>

## <span data-ttu-id="b28ad-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b28ad-131">OUTPUTS</span></span>

### <span data-ttu-id="b28ad-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b28ad-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b28ad-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="b28ad-133">NOTES</span></span>

## <span data-ttu-id="b28ad-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b28ad-134">RELATED LINKS</span></span>

[<span data-ttu-id="b28ad-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b28ad-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="b28ad-136">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b28ad-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


