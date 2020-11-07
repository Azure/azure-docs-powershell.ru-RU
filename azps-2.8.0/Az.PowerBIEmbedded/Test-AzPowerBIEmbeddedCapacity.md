---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 80fc102c31e4019576a6f2c65ee1c93e19b81590
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905110"
---
# <span data-ttu-id="1153d-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1153d-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="1153d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1153d-102">SYNOPSIS</span></span>
<span data-ttu-id="1153d-103">Проверка существования экземпляра встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="1153d-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="1153d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1153d-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1153d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1153d-105">DESCRIPTION</span></span>
<span data-ttu-id="1153d-106">Командлет Test-AzPowerBIEmbeddedCapacity проверяет наличие экземпляра встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="1153d-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="1153d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1153d-107">EXAMPLES</span></span>

### <span data-ttu-id="1153d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1153d-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="1153d-109">Эта команда пройдет проверку наличия емкости с именем testcapacity</span><span class="sxs-lookup"><span data-stu-id="1153d-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="1153d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1153d-110">PARAMETERS</span></span>

### <span data-ttu-id="1153d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1153d-111">-DefaultProfile</span></span>
<span data-ttu-id="1153d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1153d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1153d-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1153d-113">-Name</span></span>
<span data-ttu-id="1153d-114">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="1153d-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="1153d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1153d-115">CommonParameters</span></span>
<span data-ttu-id="1153d-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1153d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1153d-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1153d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1153d-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1153d-118">INPUTS</span></span>

### <span data-ttu-id="1153d-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="1153d-119">None</span></span>

## <span data-ttu-id="1153d-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1153d-120">OUTPUTS</span></span>

### <span data-ttu-id="1153d-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1153d-121">System.Boolean</span></span>

## <span data-ttu-id="1153d-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="1153d-122">NOTES</span></span>

## <span data-ttu-id="1153d-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1153d-123">RELATED LINKS</span></span>

[<span data-ttu-id="1153d-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1153d-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="1153d-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1153d-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
