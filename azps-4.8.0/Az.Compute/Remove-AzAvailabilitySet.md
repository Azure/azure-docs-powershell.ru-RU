---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 15ecd8c0e22438016ea0f589cf798ecbcb65188f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078122"
---
# <span data-ttu-id="9f1f3-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9f1f3-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="9f1f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f1f3-102">SYNOPSIS</span></span>
<span data-ttu-id="9f1f3-103">Удаляет группу доступности из Azure.</span><span class="sxs-lookup"><span data-stu-id="9f1f3-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="9f1f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f1f3-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f1f3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f1f3-105">DESCRIPTION</span></span>
<span data-ttu-id="9f1f3-106">Командлет **Remove-AzAvailabilitySet** удаляет группу доступности из Azure.</span><span class="sxs-lookup"><span data-stu-id="9f1f3-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="9f1f3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f1f3-107">EXAMPLES</span></span>

### <span data-ttu-id="9f1f3-108">Пример 1: Удаление группы доступности</span><span class="sxs-lookup"><span data-stu-id="9f1f3-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="9f1f3-109">Эта команда удаляет группу доступности с именем AvailabilitySet03 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9f1f3-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="9f1f3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f1f3-110">PARAMETERS</span></span>

### <span data-ttu-id="9f1f3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f1f3-111">-AsJob</span></span>
<span data-ttu-id="9f1f3-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="9f1f3-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9f1f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f1f3-113">-DefaultProfile</span></span>
<span data-ttu-id="9f1f3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f1f3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f1f3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9f1f3-115">-Force</span></span>
<span data-ttu-id="9f1f3-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9f1f3-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9f1f3-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9f1f3-117">-Name</span></span>
<span data-ttu-id="9f1f3-118">Имя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="9f1f3-118">The availability set name.</span></span>

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

### <span data-ttu-id="9f1f3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f1f3-119">-ResourceGroupName</span></span>
<span data-ttu-id="9f1f3-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f1f3-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9f1f3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f1f3-121">-Confirm</span></span>
<span data-ttu-id="9f1f3-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9f1f3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f1f3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f1f3-123">-WhatIf</span></span>
<span data-ttu-id="9f1f3-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9f1f3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f1f3-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9f1f3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f1f3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f1f3-126">CommonParameters</span></span>
<span data-ttu-id="9f1f3-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f1f3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f1f3-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f1f3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f1f3-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f1f3-129">INPUTS</span></span>

### <span data-ttu-id="9f1f3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9f1f3-130">System.String</span></span>

## <span data-ttu-id="9f1f3-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f1f3-131">OUTPUTS</span></span>

### <span data-ttu-id="9f1f3-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9f1f3-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9f1f3-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f1f3-133">NOTES</span></span>

## <span data-ttu-id="9f1f3-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f1f3-134">RELATED LINKS</span></span>

[<span data-ttu-id="9f1f3-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9f1f3-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="9f1f3-136">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9f1f3-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

