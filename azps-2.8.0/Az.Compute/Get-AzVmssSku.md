---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: a7696ee9738a885d3edea1eb8a3d2f9f7cea8510
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721879"
---
# <span data-ttu-id="b1721-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="b1721-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="b1721-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1721-102">SYNOPSIS</span></span>
<span data-ttu-id="b1721-103">Получает доступные SKU для VMSS.</span><span class="sxs-lookup"><span data-stu-id="b1721-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="b1721-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1721-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1721-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1721-105">DESCRIPTION</span></span>
<span data-ttu-id="b1721-106">Командлет **Get-AzVmssSku** получает доступные SKU для установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b1721-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="b1721-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1721-107">EXAMPLES</span></span>

### <span data-ttu-id="b1721-108">Пример 1: получение всех доступных SKU из VMSS</span><span class="sxs-lookup"><span data-stu-id="b1721-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="b1721-109">Эта команда получает все доступные SKU из VMSS с именем ContosoVMSS, которые относятся к группе ресурсов с именем ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="b1721-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="b1721-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1721-110">PARAMETERS</span></span>

### <span data-ttu-id="b1721-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1721-111">-DefaultProfile</span></span>
<span data-ttu-id="b1721-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1721-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1721-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1721-113">-ResourceGroupName</span></span>
<span data-ttu-id="b1721-114">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="b1721-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="b1721-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b1721-115">-VMScaleSetName</span></span>
<span data-ttu-id="b1721-116">Форель имя VMSS.</span><span class="sxs-lookup"><span data-stu-id="b1721-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="b1721-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1721-117">CommonParameters</span></span>
<span data-ttu-id="b1721-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1721-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1721-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1721-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1721-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1721-120">INPUTS</span></span>

### <span data-ttu-id="b1721-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b1721-121">System.String</span></span>

## <span data-ttu-id="b1721-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1721-122">OUTPUTS</span></span>

### <span data-ttu-id="b1721-123">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="b1721-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="b1721-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1721-124">NOTES</span></span>

## <span data-ttu-id="b1721-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1721-125">RELATED LINKS</span></span>

[<span data-ttu-id="b1721-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b1721-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


