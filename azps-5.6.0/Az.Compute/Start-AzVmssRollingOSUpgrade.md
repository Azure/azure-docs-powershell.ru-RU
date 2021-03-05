---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: fb3d6f08eaa540e208830a15563b8edd8c2432ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962451"
---
# <span data-ttu-id="fd565-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="fd565-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="fd565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd565-102">SYNOPSIS</span></span>
<span data-ttu-id="fd565-103">Запускает развертывание обновления, чтобы перенести все экземпляры набора виртуальных машин на последнюю доступную версию ОС платформы image.</span><span class="sxs-lookup"><span data-stu-id="fd565-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="fd565-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fd565-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd565-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd565-105">DESCRIPTION</span></span>
<span data-ttu-id="fd565-106">Запускает развертывание обновления, чтобы перенести все экземпляры набора виртуальных машин на последнюю доступную версию ОС платформы image.</span><span class="sxs-lookup"><span data-stu-id="fd565-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="fd565-107">На экземпляры, которые уже работают с последней доступной версией ОС, это не влияет.</span><span class="sxs-lookup"><span data-stu-id="fd565-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="fd565-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fd565-108">EXAMPLES</span></span>

### <span data-ttu-id="fd565-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fd565-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="fd565-110">Эта команда запускает развертывание обновления всех VM-экземпляров набора масштаба VM "VMSS001" в группе ресурсов "Группа001".</span><span class="sxs-lookup"><span data-stu-id="fd565-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="fd565-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd565-111">PARAMETERS</span></span>

### <span data-ttu-id="fd565-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd565-112">-AsJob</span></span>
<span data-ttu-id="fd565-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fd565-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd565-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd565-114">-DefaultProfile</span></span>
<span data-ttu-id="fd565-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd565-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd565-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd565-116">-ResourceGroupName</span></span>
<span data-ttu-id="fd565-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd565-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="fd565-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fd565-118">-VMScaleSetName</span></span>
<span data-ttu-id="fd565-119">Имя набора масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="fd565-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="fd565-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd565-120">-Confirm</span></span>
<span data-ttu-id="fd565-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd565-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd565-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd565-122">-WhatIf</span></span>
<span data-ttu-id="fd565-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd565-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd565-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fd565-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd565-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd565-125">CommonParameters</span></span>
<span data-ttu-id="fd565-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd565-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd565-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd565-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd565-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd565-128">INPUTS</span></span>

### <span data-ttu-id="fd565-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fd565-129">System.String</span></span>

## <span data-ttu-id="fd565-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fd565-130">OUTPUTS</span></span>

### <span data-ttu-id="fd565-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="fd565-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="fd565-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fd565-132">NOTES</span></span>

## <span data-ttu-id="fd565-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd565-133">RELATED LINKS</span></span>
