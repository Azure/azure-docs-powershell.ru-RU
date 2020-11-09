---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 73960bb3efbc3d1a55d9894943c2f92bcf931faa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249175"
---
# <span data-ttu-id="d35bd-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d35bd-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d35bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d35bd-102">SYNOPSIS</span></span>
<span data-ttu-id="d35bd-103">Проверка существования экземпляра встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="d35bd-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="d35bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d35bd-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d35bd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d35bd-105">DESCRIPTION</span></span>
<span data-ttu-id="d35bd-106">Командлет Test-AzPowerBIEmbeddedCapacity проверяет наличие экземпляра встроенной емкости PowerBI.</span><span class="sxs-lookup"><span data-stu-id="d35bd-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="d35bd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d35bd-107">EXAMPLES</span></span>

### <span data-ttu-id="d35bd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d35bd-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="d35bd-109">Эта команда пройдет проверку наличия емкости с именем testcapacity</span><span class="sxs-lookup"><span data-stu-id="d35bd-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="d35bd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d35bd-110">PARAMETERS</span></span>

### <span data-ttu-id="d35bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d35bd-111">-DefaultProfile</span></span>
<span data-ttu-id="d35bd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d35bd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d35bd-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d35bd-113">-Name</span></span>
<span data-ttu-id="d35bd-114">Имя встроенной емкости PowerBI</span><span class="sxs-lookup"><span data-stu-id="d35bd-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="d35bd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d35bd-115">CommonParameters</span></span>
<span data-ttu-id="d35bd-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d35bd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d35bd-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d35bd-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d35bd-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d35bd-118">INPUTS</span></span>

### <span data-ttu-id="d35bd-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="d35bd-119">None</span></span>

## <span data-ttu-id="d35bd-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d35bd-120">OUTPUTS</span></span>

### <span data-ttu-id="d35bd-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d35bd-121">System.Boolean</span></span>

## <span data-ttu-id="d35bd-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="d35bd-122">NOTES</span></span>

## <span data-ttu-id="d35bd-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d35bd-123">RELATED LINKS</span></span>

[<span data-ttu-id="d35bd-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d35bd-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="d35bd-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d35bd-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)