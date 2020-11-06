---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8f6e161ad9ae2078da15dda659f1aea13929eec9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557276"
---
# <span data-ttu-id="99c78-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="99c78-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="99c78-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99c78-102">SYNOPSIS</span></span>
<span data-ttu-id="99c78-103">Проверка существования экземпляра встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="99c78-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99c78-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99c78-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="99c78-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99c78-105">DESCRIPTION</span></span>
<span data-ttu-id="99c78-106">Командлет Test-AzureRmPowerBIEmbeddedCapacity проверяет наличие экземпляра встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="99c78-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="99c78-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99c78-107">EXAMPLES</span></span>

### <span data-ttu-id="99c78-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="99c78-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="99c78-109">Эта команда пройдет проверку наличия емкости с именем testcapacity</span><span class="sxs-lookup"><span data-stu-id="99c78-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="99c78-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99c78-110">PARAMETERS</span></span>

### <span data-ttu-id="99c78-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="99c78-111">-Name</span></span>
<span data-ttu-id="99c78-112">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="99c78-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="99c78-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c78-113">CommonParameters</span></span>
<span data-ttu-id="99c78-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99c78-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c78-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99c78-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c78-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99c78-116">INPUTS</span></span>

### <span data-ttu-id="99c78-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="99c78-117">None</span></span>
<span data-ttu-id="99c78-118">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="99c78-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="99c78-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99c78-119">OUTPUTS</span></span>

### <span data-ttu-id="99c78-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="99c78-120">System.Boolean</span></span>

## <span data-ttu-id="99c78-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="99c78-121">NOTES</span></span>

## <span data-ttu-id="99c78-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99c78-122">RELATED LINKS</span></span>

[<span data-ttu-id="99c78-123">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="99c78-123">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="99c78-124">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="99c78-124">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
