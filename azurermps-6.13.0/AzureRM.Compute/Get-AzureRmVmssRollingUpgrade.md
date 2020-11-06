---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: ef83792704e24102e8e837768ee5acae5abbe548
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556803"
---
# <span data-ttu-id="7e8ed-101">Get-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="7e8ed-101">Get-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="7e8ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="7e8ed-103">Показывает состояние последней версии набора масштабов виртуальных машин, чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="7e8ed-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e8ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e8ed-104">SYNTAX</span></span>

```
Get-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e8ed-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e8ed-105">DESCRIPTION</span></span>
<span data-ttu-id="7e8ed-106">Показывает состояние последней версии набора масштабов виртуальных машин, чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="7e8ed-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="7e8ed-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e8ed-107">EXAMPLES</span></span>

### <span data-ttu-id="7e8ed-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7e8ed-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="7e8ed-109">Эта команда показывает состояние последнего чередующегося обновления VMSS с именем VMSS001, которое принадлежит группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="7e8ed-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="7e8ed-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e8ed-110">PARAMETERS</span></span>

### <span data-ttu-id="7e8ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e8ed-111">-DefaultProfile</span></span>
<span data-ttu-id="7e8ed-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e8ed-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e8ed-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e8ed-113">-ResourceGroupName</span></span>
<span data-ttu-id="7e8ed-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e8ed-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e8ed-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7e8ed-115">-VMScaleSetName</span></span>
<span data-ttu-id="7e8ed-116">Имя набора масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="7e8ed-116">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e8ed-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e8ed-117">CommonParameters</span></span>
<span data-ttu-id="7e8ed-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e8ed-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e8ed-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e8ed-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e8ed-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e8ed-120">INPUTS</span></span>

### <span data-ttu-id="7e8ed-121">System. String</span><span class="sxs-lookup"><span data-stu-id="7e8ed-121">System.String</span></span>

## <span data-ttu-id="7e8ed-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e8ed-122">OUTPUTS</span></span>

### <span data-ttu-id="7e8ed-123">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRollingUpgradeStatusInfo</span><span class="sxs-lookup"><span data-stu-id="7e8ed-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="7e8ed-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e8ed-124">NOTES</span></span>

## <span data-ttu-id="7e8ed-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e8ed-125">RELATED LINKS</span></span>
