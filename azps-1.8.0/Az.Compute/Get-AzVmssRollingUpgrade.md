---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 344f62f6114eb85e1a9e17b0e4d8c4da0acb93a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901290"
---
# <span data-ttu-id="17bdf-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="17bdf-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="17bdf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="17bdf-103">Показывает состояние последней версии набора масштабов виртуальных машин, чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="17bdf-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="17bdf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17bdf-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17bdf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17bdf-105">DESCRIPTION</span></span>
<span data-ttu-id="17bdf-106">Показывает состояние последней версии набора масштабов виртуальных машин, чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="17bdf-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="17bdf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17bdf-107">EXAMPLES</span></span>

### <span data-ttu-id="17bdf-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="17bdf-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="17bdf-109">Эта команда показывает состояние последнего чередующегося обновления VMSS с именем VMSS001, которое принадлежит группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="17bdf-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="17bdf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17bdf-110">PARAMETERS</span></span>

### <span data-ttu-id="17bdf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17bdf-111">-DefaultProfile</span></span>
<span data-ttu-id="17bdf-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17bdf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17bdf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17bdf-113">-ResourceGroupName</span></span>
<span data-ttu-id="17bdf-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="17bdf-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="17bdf-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="17bdf-115">-VMScaleSetName</span></span>
<span data-ttu-id="17bdf-116">Имя набора масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="17bdf-116">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="17bdf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17bdf-117">CommonParameters</span></span>
<span data-ttu-id="17bdf-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17bdf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17bdf-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17bdf-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17bdf-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17bdf-120">INPUTS</span></span>

### <span data-ttu-id="17bdf-121">System. String</span><span class="sxs-lookup"><span data-stu-id="17bdf-121">System.String</span></span>

## <span data-ttu-id="17bdf-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17bdf-122">OUTPUTS</span></span>

### <span data-ttu-id="17bdf-123">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="17bdf-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="17bdf-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="17bdf-124">NOTES</span></span>

## <span data-ttu-id="17bdf-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17bdf-125">RELATED LINKS</span></span>
