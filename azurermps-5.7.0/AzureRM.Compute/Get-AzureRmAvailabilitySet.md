---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5f2769987c87942af78bda238de00df94168249a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565579"
---
# <span data-ttu-id="d1f30-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d1f30-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="d1f30-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1f30-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f30-103">Получает наборы доступности Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1f30-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1f30-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1f30-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="d1f30-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1f30-105">DESCRIPTION</span></span>
<span data-ttu-id="d1f30-106">Командлет **Get-AzureRmAvailabilitySet** получает наборы доступности Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1f30-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="d1f30-107">Вы можете указать имя определенного набора доступности, которое нужно получить.</span><span class="sxs-lookup"><span data-stu-id="d1f30-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="d1f30-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1f30-108">EXAMPLES</span></span>

### <span data-ttu-id="d1f30-109">Пример 1: получение определенной группы доступности</span><span class="sxs-lookup"><span data-stu-id="d1f30-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="d1f30-110">Эта команда получает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d1f30-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="d1f30-111">Пример 2: получение всех наборов доступности</span><span class="sxs-lookup"><span data-stu-id="d1f30-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="d1f30-112">Эта команда получает все наборы доступности в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d1f30-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d1f30-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1f30-113">PARAMETERS</span></span>

### <span data-ttu-id="d1f30-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d1f30-114">-Name</span></span>
<span data-ttu-id="d1f30-115">Указывает имя набора доступности, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d1f30-115">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1f30-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1f30-116">-ResourceGroupName</span></span>
<span data-ttu-id="d1f30-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1f30-117">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1f30-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f30-118">CommonParameters</span></span>
<span data-ttu-id="d1f30-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1f30-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f30-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1f30-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f30-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1f30-121">INPUTS</span></span>

### <span data-ttu-id="d1f30-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="d1f30-122">None</span></span>
<span data-ttu-id="d1f30-123">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d1f30-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d1f30-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1f30-124">OUTPUTS</span></span>

## <span data-ttu-id="d1f30-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1f30-125">NOTES</span></span>

## <span data-ttu-id="d1f30-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1f30-126">RELATED LINKS</span></span>

[<span data-ttu-id="d1f30-127">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d1f30-127">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="d1f30-128">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d1f30-128">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


