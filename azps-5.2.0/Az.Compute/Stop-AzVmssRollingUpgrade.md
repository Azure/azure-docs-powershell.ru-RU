---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 331f390890e6349c5a48f9b57c3d0e99fa972532
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402599"
---
# <span data-ttu-id="761eb-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="761eb-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="761eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="761eb-102">SYNOPSIS</span></span>
<span data-ttu-id="761eb-103">Отмена текущего масштабирования виртуальной машины, настроенного для скользячего обновления.</span><span class="sxs-lookup"><span data-stu-id="761eb-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="761eb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="761eb-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="761eb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="761eb-105">DESCRIPTION</span></span>
<span data-ttu-id="761eb-106">Отмена текущего масштабирования виртуальной машины, настроенного для скользячего обновления.</span><span class="sxs-lookup"><span data-stu-id="761eb-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="761eb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="761eb-107">EXAMPLES</span></span>

### <span data-ttu-id="761eb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="761eb-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="761eb-109">Эта команда отменяет развертывание обновления масштаба VM, установленного с погововой "VMSS001" в группе ресурсов "Группа001".</span><span class="sxs-lookup"><span data-stu-id="761eb-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="761eb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="761eb-110">PARAMETERS</span></span>

### <span data-ttu-id="761eb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="761eb-111">-AsJob</span></span>
<span data-ttu-id="761eb-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="761eb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="761eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="761eb-113">-DefaultProfile</span></span>
<span data-ttu-id="761eb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="761eb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="761eb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="761eb-115">-Force</span></span>
<span data-ttu-id="761eb-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="761eb-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="761eb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="761eb-117">-ResourceGroupName</span></span>
<span data-ttu-id="761eb-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="761eb-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="761eb-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="761eb-119">-VMScaleSetName</span></span>
<span data-ttu-id="761eb-120">Имя набора масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="761eb-120">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="761eb-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="761eb-121">-Confirm</span></span>
<span data-ttu-id="761eb-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="761eb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="761eb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="761eb-123">-WhatIf</span></span>
<span data-ttu-id="761eb-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="761eb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="761eb-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="761eb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="761eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="761eb-126">CommonParameters</span></span>
<span data-ttu-id="761eb-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="761eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="761eb-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="761eb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="761eb-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="761eb-129">INPUTS</span></span>

### <span data-ttu-id="761eb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="761eb-130">System.String</span></span>

## <span data-ttu-id="761eb-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="761eb-131">OUTPUTS</span></span>

### <span data-ttu-id="761eb-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="761eb-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="761eb-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="761eb-133">NOTES</span></span>

## <span data-ttu-id="761eb-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="761eb-134">RELATED LINKS</span></span>
