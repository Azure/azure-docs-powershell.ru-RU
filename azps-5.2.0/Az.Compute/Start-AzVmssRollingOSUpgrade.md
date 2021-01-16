---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: ad5d387a0935150a66924cbfdd19ac40ed57079c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327364"
---
# <span data-ttu-id="1c585-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="1c585-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="1c585-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c585-102">SYNOPSIS</span></span>
<span data-ttu-id="1c585-103">Запускает развертывание обновления для перемещения всех экземпляров набора виртуальных машин на последнюю доступную версию ОС платформы image.</span><span class="sxs-lookup"><span data-stu-id="1c585-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="1c585-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1c585-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c585-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c585-105">DESCRIPTION</span></span>
<span data-ttu-id="1c585-106">Запускает развертывание обновления для перемещения всех экземпляров набора виртуальных машин на последнюю доступную версию ОС платформы image.</span><span class="sxs-lookup"><span data-stu-id="1c585-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="1c585-107">На экземпляры, которые уже работают с последней доступной версией ОС, это не влияет.</span><span class="sxs-lookup"><span data-stu-id="1c585-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="1c585-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1c585-108">EXAMPLES</span></span>

### <span data-ttu-id="1c585-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1c585-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="1c585-110">Эта команда запускает развертывание обновления всех VM-экземпляров набора масштаба VM "VMSS001" в группе ресурсов "Group001".</span><span class="sxs-lookup"><span data-stu-id="1c585-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="1c585-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c585-111">PARAMETERS</span></span>

### <span data-ttu-id="1c585-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c585-112">-AsJob</span></span>
<span data-ttu-id="1c585-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1c585-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c585-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c585-114">-DefaultProfile</span></span>
<span data-ttu-id="1c585-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c585-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c585-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c585-116">-ResourceGroupName</span></span>
<span data-ttu-id="1c585-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c585-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="1c585-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1c585-118">-VMScaleSetName</span></span>
<span data-ttu-id="1c585-119">Имя набора масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="1c585-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="1c585-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c585-120">-Confirm</span></span>
<span data-ttu-id="1c585-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c585-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c585-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c585-122">-WhatIf</span></span>
<span data-ttu-id="1c585-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c585-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c585-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1c585-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c585-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c585-125">CommonParameters</span></span>
<span data-ttu-id="1c585-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c585-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c585-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c585-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c585-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c585-128">INPUTS</span></span>

### <span data-ttu-id="1c585-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1c585-129">System.String</span></span>

## <span data-ttu-id="1c585-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1c585-130">OUTPUTS</span></span>

### <span data-ttu-id="1c585-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="1c585-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="1c585-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1c585-132">NOTES</span></span>

## <span data-ttu-id="1c585-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c585-133">RELATED LINKS</span></span>
