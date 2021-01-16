---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: 4b17cbb748a9841e0c22f4b8d8742562876fb9db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509145"
---
# <span data-ttu-id="b0174-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="b0174-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="b0174-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0174-102">SYNOPSIS</span></span>
<span data-ttu-id="b0174-103">Возвращает доступные skus для VMSS.</span><span class="sxs-lookup"><span data-stu-id="b0174-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="b0174-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b0174-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0174-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0174-105">DESCRIPTION</span></span>
<span data-ttu-id="b0174-106">Для набора виртуальных машин (VMSS) доступны коды SKKU **для get-AzVmssSku.**</span><span class="sxs-lookup"><span data-stu-id="b0174-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="b0174-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b0174-107">EXAMPLES</span></span>

### <span data-ttu-id="b0174-108">Пример 1. Получить все доступные skus из VMSS</span><span class="sxs-lookup"><span data-stu-id="b0174-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="b0174-109">Эта команда получает все доступные skus из VMSS ContosoVMSS, которые принадлежат группе ресурсов ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="b0174-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="b0174-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0174-110">PARAMETERS</span></span>

### <span data-ttu-id="b0174-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0174-111">-DefaultProfile</span></span>
<span data-ttu-id="b0174-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0174-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0174-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0174-113">-ResourceGroupName</span></span>
<span data-ttu-id="b0174-114">Имя группы ресурсов VMSS.</span><span class="sxs-lookup"><span data-stu-id="b0174-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="b0174-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b0174-115">-VMScaleSetName</span></span>
<span data-ttu-id="b0174-116">Вид имени VMSS.</span><span class="sxs-lookup"><span data-stu-id="b0174-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="b0174-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0174-117">CommonParameters</span></span>
<span data-ttu-id="b0174-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0174-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0174-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0174-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0174-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0174-120">INPUTS</span></span>

### <span data-ttu-id="b0174-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b0174-121">System.String</span></span>

## <span data-ttu-id="b0174-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0174-122">OUTPUTS</span></span>

### <span data-ttu-id="b0174-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="b0174-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="b0174-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b0174-124">NOTES</span></span>

## <span data-ttu-id="b0174-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0174-125">RELATED LINKS</span></span>

[<span data-ttu-id="b0174-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b0174-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


