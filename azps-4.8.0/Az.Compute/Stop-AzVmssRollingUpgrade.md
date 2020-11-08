---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 331f390890e6349c5a48f9b57c3d0e99fa972532
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078105"
---
# <span data-ttu-id="cd3ef-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="cd3ef-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="cd3ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd3ef-102">SYNOPSIS</span></span>
<span data-ttu-id="cd3ef-103">Отменяет текущую виртуальную машину с установленным параметром чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="cd3ef-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="cd3ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd3ef-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd3ef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd3ef-105">DESCRIPTION</span></span>
<span data-ttu-id="cd3ef-106">Отменяет текущую виртуальную машину с установленным параметром чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="cd3ef-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="cd3ef-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd3ef-107">EXAMPLES</span></span>

### <span data-ttu-id="cd3ef-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cd3ef-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="cd3ef-109">Эта команда отменяет переход на новую версию шкалы виртуальных машин "VMSS001" в группе ресурсов "Group001".</span><span class="sxs-lookup"><span data-stu-id="cd3ef-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="cd3ef-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd3ef-110">PARAMETERS</span></span>

### <span data-ttu-id="cd3ef-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd3ef-111">-AsJob</span></span>
<span data-ttu-id="cd3ef-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cd3ef-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd3ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd3ef-113">-DefaultProfile</span></span>
<span data-ttu-id="cd3ef-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd3ef-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd3ef-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cd3ef-115">-Force</span></span>
<span data-ttu-id="cd3ef-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="cd3ef-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cd3ef-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd3ef-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd3ef-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cd3ef-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="cd3ef-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cd3ef-119">-VMScaleSetName</span></span>
<span data-ttu-id="cd3ef-120">Имя набора масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="cd3ef-120">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd3ef-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd3ef-121">-Confirm</span></span>
<span data-ttu-id="cd3ef-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cd3ef-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd3ef-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd3ef-123">-WhatIf</span></span>
<span data-ttu-id="cd3ef-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd3ef-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd3ef-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd3ef-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd3ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd3ef-126">CommonParameters</span></span>
<span data-ttu-id="cd3ef-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd3ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd3ef-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd3ef-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd3ef-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd3ef-129">INPUTS</span></span>

### <span data-ttu-id="cd3ef-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cd3ef-130">System.String</span></span>

## <span data-ttu-id="cd3ef-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd3ef-131">OUTPUTS</span></span>

### <span data-ttu-id="cd3ef-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="cd3ef-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="cd3ef-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd3ef-133">NOTES</span></span>

## <span data-ttu-id="cd3ef-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd3ef-134">RELATED LINKS</span></span>