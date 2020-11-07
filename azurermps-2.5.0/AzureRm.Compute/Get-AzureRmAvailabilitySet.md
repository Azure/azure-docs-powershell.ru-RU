---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: ef00a9e425f67fbfc1ce47746503b574d483598f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913496"
---
# <span data-ttu-id="d9d0e-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d9d0e-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="d9d0e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9d0e-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d0e-103">Получает наборы доступности Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9d0e-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9d0e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9d0e-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9d0e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9d0e-105">DESCRIPTION</span></span>
<span data-ttu-id="d9d0e-106">Командлет **Get-AzureRmAvailabilitySet** получает наборы доступности Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9d0e-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="d9d0e-107">Вы можете указать имя определенного набора доступности, которое нужно получить.</span><span class="sxs-lookup"><span data-stu-id="d9d0e-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="d9d0e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9d0e-108">EXAMPLES</span></span>

### <span data-ttu-id="d9d0e-109">Пример 1: получение определенной группы доступности</span><span class="sxs-lookup"><span data-stu-id="d9d0e-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="d9d0e-110">Эта команда получает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d9d0e-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="d9d0e-111">Пример 2: получение всех наборов доступности</span><span class="sxs-lookup"><span data-stu-id="d9d0e-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="d9d0e-112">Эта команда получает все наборы доступности в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d9d0e-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d9d0e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9d0e-113">PARAMETERS</span></span>

### <span data-ttu-id="d9d0e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d0e-114">-DefaultProfile</span></span>
<span data-ttu-id="d9d0e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d0e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9d0e-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d9d0e-116">-Name</span></span>
<span data-ttu-id="d9d0e-117">Указывает имя набора доступности, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d9d0e-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d9d0e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9d0e-118">-ResourceGroupName</span></span>
<span data-ttu-id="d9d0e-119">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9d0e-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d9d0e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d0e-120">CommonParameters</span></span>
<span data-ttu-id="d9d0e-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9d0e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d0e-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9d0e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d0e-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9d0e-123">INPUTS</span></span>

### <span data-ttu-id="d9d0e-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="d9d0e-124">None</span></span>
<span data-ttu-id="d9d0e-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d9d0e-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9d0e-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9d0e-126">OUTPUTS</span></span>

### <span data-ttu-id="d9d0e-127">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d9d0e-127">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="d9d0e-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9d0e-128">NOTES</span></span>

## <span data-ttu-id="d9d0e-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9d0e-129">RELATED LINKS</span></span>

[<span data-ttu-id="d9d0e-130">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d9d0e-130">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="d9d0e-131">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d9d0e-131">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


