---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
ms.openlocfilehash: c86bf549c0de3643aaba67143b7df78f6fce798c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559191"
---
# <span data-ttu-id="87251-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="87251-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="87251-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87251-102">SYNOPSIS</span></span>
<span data-ttu-id="87251-103">Получает доступные SKU для VMSS.</span><span class="sxs-lookup"><span data-stu-id="87251-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87251-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87251-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String> [<CommonParameters>]
```

## <span data-ttu-id="87251-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87251-105">DESCRIPTION</span></span>
<span data-ttu-id="87251-106">Командлет **Get-AzureRmVmssSku** получает доступные SKU для установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="87251-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="87251-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87251-107">EXAMPLES</span></span>

### <span data-ttu-id="87251-108">Пример 1: получение всех доступных SKU из VMSS</span><span class="sxs-lookup"><span data-stu-id="87251-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="87251-109">Эта команда получает все доступные SKU из VMSS с именем ContosoVMSS, которые относятся к группе ресурсов с именем ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="87251-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="87251-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87251-110">PARAMETERS</span></span>

### <span data-ttu-id="87251-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87251-111">-ResourceGroupName</span></span>
<span data-ttu-id="87251-112">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="87251-112">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87251-113">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="87251-113">-VMScaleSetName</span></span>
<span data-ttu-id="87251-114">Форель имя VMSS.</span><span class="sxs-lookup"><span data-stu-id="87251-114">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87251-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87251-115">CommonParameters</span></span>
<span data-ttu-id="87251-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87251-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87251-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87251-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87251-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87251-118">INPUTS</span></span>

### <span data-ttu-id="87251-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="87251-119">None</span></span>
<span data-ttu-id="87251-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="87251-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="87251-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87251-121">OUTPUTS</span></span>

### <span data-ttu-id="87251-122">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="87251-122">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="87251-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="87251-123">NOTES</span></span>

## <span data-ttu-id="87251-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87251-124">RELATED LINKS</span></span>

[<span data-ttu-id="87251-125">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="87251-125">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


