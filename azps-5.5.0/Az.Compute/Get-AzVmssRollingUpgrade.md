---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 3ab0dc0acb02d2efa9f7da29dd096ad03f1eb57e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211780"
---
# <span data-ttu-id="3b424-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="3b424-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="3b424-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b424-102">SYNOPSIS</span></span>
<span data-ttu-id="3b424-103">Показывает состояние последнего обновления в масштабе виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3b424-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="3b424-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3b424-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b424-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b424-105">DESCRIPTION</span></span>
<span data-ttu-id="3b424-106">Показывает состояние последнего обновления виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3b424-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="3b424-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3b424-107">EXAMPLES</span></span>

### <span data-ttu-id="3b424-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3b424-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="3b424-109">Эта команда показывает состояние последнего ветвного обновления VMSS под названием VMSS001, которое принадлежит группе ресурсов Group001.</span><span class="sxs-lookup"><span data-stu-id="3b424-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="3b424-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b424-110">PARAMETERS</span></span>

### <span data-ttu-id="3b424-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b424-111">-DefaultProfile</span></span>
<span data-ttu-id="3b424-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b424-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b424-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b424-113">-ResourceGroupName</span></span>
<span data-ttu-id="3b424-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3b424-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="3b424-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3b424-115">-VMScaleSetName</span></span>
<span data-ttu-id="3b424-116">Имя набора масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="3b424-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="3b424-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b424-117">CommonParameters</span></span>
<span data-ttu-id="3b424-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b424-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b424-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b424-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b424-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b424-120">INPUTS</span></span>

### <span data-ttu-id="3b424-121">System.String</span><span class="sxs-lookup"><span data-stu-id="3b424-121">System.String</span></span>

## <span data-ttu-id="3b424-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3b424-122">OUTPUTS</span></span>

### <span data-ttu-id="3b424-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="3b424-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="3b424-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3b424-124">NOTES</span></span>

## <span data-ttu-id="3b424-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b424-125">RELATED LINKS</span></span>
