---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: 4b17cbb748a9841e0c22f4b8d8742562876fb9db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080032"
---
# <span data-ttu-id="f3c2e-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="f3c2e-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="f3c2e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c2e-103">Получает доступные SKU для VMSS.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="f3c2e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3c2e-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3c2e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3c2e-105">DESCRIPTION</span></span>
<span data-ttu-id="f3c2e-106">Командлет **Get-AzVmssSku** получает доступные SKU для установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f3c2e-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="f3c2e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3c2e-107">EXAMPLES</span></span>

### <span data-ttu-id="f3c2e-108">Пример 1: получение всех доступных SKU из VMSS</span><span class="sxs-lookup"><span data-stu-id="f3c2e-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="f3c2e-109">Эта команда получает все доступные SKU из VMSS с именем ContosoVMSS, которые относятся к группе ресурсов с именем ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="f3c2e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3c2e-110">PARAMETERS</span></span>

### <span data-ttu-id="f3c2e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c2e-111">-DefaultProfile</span></span>
<span data-ttu-id="f3c2e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3c2e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3c2e-113">-ResourceGroupName</span></span>
<span data-ttu-id="f3c2e-114">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="f3c2e-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f3c2e-115">-VMScaleSetName</span></span>
<span data-ttu-id="f3c2e-116">Форель имя VMSS.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="f3c2e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c2e-117">CommonParameters</span></span>
<span data-ttu-id="f3c2e-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3c2e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c2e-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3c2e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c2e-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3c2e-120">INPUTS</span></span>

### <span data-ttu-id="f3c2e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f3c2e-121">System.String</span></span>

## <span data-ttu-id="f3c2e-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3c2e-122">OUTPUTS</span></span>

### <span data-ttu-id="f3c2e-123">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="f3c2e-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="f3c2e-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3c2e-124">NOTES</span></span>

## <span data-ttu-id="f3c2e-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3c2e-125">RELATED LINKS</span></span>

[<span data-ttu-id="f3c2e-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f3c2e-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


