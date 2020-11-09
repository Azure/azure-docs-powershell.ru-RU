---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 3ab0dc0acb02d2efa9f7da29dd096ad03f1eb57e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316695"
---
# <span data-ttu-id="e6b70-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="e6b70-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="e6b70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6b70-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b70-103">Показывает состояние последней версии набора масштабов виртуальных машин, чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="e6b70-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="e6b70-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6b70-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6b70-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6b70-105">DESCRIPTION</span></span>
<span data-ttu-id="e6b70-106">Показывает состояние последней версии набора масштабов виртуальных машин, чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="e6b70-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="e6b70-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6b70-107">EXAMPLES</span></span>

### <span data-ttu-id="e6b70-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e6b70-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="e6b70-109">Эта команда показывает состояние последнего чередующегося обновления VMSS с именем VMSS001, которое принадлежит группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="e6b70-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="e6b70-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6b70-110">PARAMETERS</span></span>

### <span data-ttu-id="e6b70-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b70-111">-DefaultProfile</span></span>
<span data-ttu-id="e6b70-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6b70-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6b70-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6b70-113">-ResourceGroupName</span></span>
<span data-ttu-id="e6b70-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6b70-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="e6b70-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e6b70-115">-VMScaleSetName</span></span>
<span data-ttu-id="e6b70-116">Имя набора масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="e6b70-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="e6b70-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b70-117">CommonParameters</span></span>
<span data-ttu-id="e6b70-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6b70-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b70-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6b70-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b70-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6b70-120">INPUTS</span></span>

### <span data-ttu-id="e6b70-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e6b70-121">System.String</span></span>

## <span data-ttu-id="e6b70-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6b70-122">OUTPUTS</span></span>

### <span data-ttu-id="e6b70-123">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="e6b70-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="e6b70-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6b70-124">NOTES</span></span>

## <span data-ttu-id="e6b70-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6b70-125">RELATED LINKS</span></span>
