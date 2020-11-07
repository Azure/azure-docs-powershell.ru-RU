---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 306bb6e4e12adcb4a4eda65b2517ddf0648a81fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732910"
---
# <span data-ttu-id="c1171-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c1171-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="c1171-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1171-102">SYNOPSIS</span></span>
<span data-ttu-id="c1171-103">Проверка существования экземпляра встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="c1171-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1171-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1171-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1171-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1171-105">DESCRIPTION</span></span>
<span data-ttu-id="c1171-106">Командлет Test-AzureRmPowerBIEmbeddedCapacity проверяет наличие экземпляра встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="c1171-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="c1171-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1171-107">EXAMPLES</span></span>

### <span data-ttu-id="c1171-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c1171-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="c1171-109">Эта команда пройдет проверку наличия емкости с именем testcapacity</span><span class="sxs-lookup"><span data-stu-id="c1171-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="c1171-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1171-110">PARAMETERS</span></span>

### <span data-ttu-id="c1171-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1171-111">-DefaultProfile</span></span>
<span data-ttu-id="c1171-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1171-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1171-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c1171-113">-Name</span></span>
<span data-ttu-id="c1171-114">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="c1171-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1171-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1171-115">CommonParameters</span></span>
<span data-ttu-id="c1171-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1171-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1171-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1171-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1171-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1171-118">INPUTS</span></span>

### <span data-ttu-id="c1171-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="c1171-119">None</span></span>

## <span data-ttu-id="c1171-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1171-120">OUTPUTS</span></span>

### <span data-ttu-id="c1171-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1171-121">System.Boolean</span></span>

## <span data-ttu-id="c1171-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1171-122">NOTES</span></span>

## <span data-ttu-id="c1171-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1171-123">RELATED LINKS</span></span>

[<span data-ttu-id="c1171-124">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c1171-124">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="c1171-125">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c1171-125">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
