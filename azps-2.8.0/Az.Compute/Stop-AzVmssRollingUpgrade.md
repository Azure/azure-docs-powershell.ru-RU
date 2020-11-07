---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: cbe44db07cbf32195f92ebefc0a2032a5f288a1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721643"
---
# <span data-ttu-id="3d6ae-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="3d6ae-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="3d6ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d6ae-102">SYNOPSIS</span></span>
<span data-ttu-id="3d6ae-103">Отменяет текущую виртуальную машину с установленным параметром чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="3d6ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d6ae-104">SYNTAX</span></span>

### <span data-ttu-id="3d6ae-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d6ae-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d6ae-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="3d6ae-106">FriendMethod</span></span>
```
Stop-AzVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d6ae-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d6ae-107">DESCRIPTION</span></span>
<span data-ttu-id="3d6ae-108">Отменяет текущую виртуальную машину с установленным параметром чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="3d6ae-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d6ae-109">EXAMPLES</span></span>

### <span data-ttu-id="3d6ae-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3d6ae-110">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="3d6ae-111">Эта команда отменяет переход на новую версию шкалы виртуальных машин "VMSS001" в группе ресурсов "Group001".</span><span class="sxs-lookup"><span data-stu-id="3d6ae-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="3d6ae-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d6ae-112">PARAMETERS</span></span>

### <span data-ttu-id="3d6ae-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d6ae-113">-AsJob</span></span>
<span data-ttu-id="3d6ae-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3d6ae-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d6ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d6ae-115">-DefaultProfile</span></span>
<span data-ttu-id="3d6ae-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d6ae-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3d6ae-117">-Force</span></span>
<span data-ttu-id="3d6ae-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3d6ae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d6ae-119">-ResourceGroupName</span></span>
<span data-ttu-id="3d6ae-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6ae-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3d6ae-121">-VMScaleSetName</span></span>
<span data-ttu-id="3d6ae-122">Имя набора масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-122">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6ae-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d6ae-123">-Confirm</span></span>
<span data-ttu-id="3d6ae-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d6ae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d6ae-125">-WhatIf</span></span>
<span data-ttu-id="3d6ae-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d6ae-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d6ae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6ae-128">CommonParameters</span></span>
<span data-ttu-id="3d6ae-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d6ae-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d6ae-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6ae-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d6ae-131">INPUTS</span></span>

### <span data-ttu-id="3d6ae-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3d6ae-132">System.String</span></span>

## <span data-ttu-id="3d6ae-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d6ae-133">OUTPUTS</span></span>

### <span data-ttu-id="3d6ae-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3d6ae-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3d6ae-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d6ae-135">NOTES</span></span>

## <span data-ttu-id="3d6ae-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d6ae-136">RELATED LINKS</span></span>
