---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 685dafeb72693a617ca627aa1abcae19c5e24389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561096"
---
# <span data-ttu-id="ceabd-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ceabd-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="ceabd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ceabd-102">SYNOPSIS</span></span>
<span data-ttu-id="ceabd-103">Получает наборы доступности Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ceabd-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceabd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ceabd-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceabd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ceabd-105">DESCRIPTION</span></span>
<span data-ttu-id="ceabd-106">Командлет **Get-AzureRmAvailabilitySet** получает наборы доступности Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ceabd-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="ceabd-107">Вы можете указать имя определенного набора доступности, которое нужно получить.</span><span class="sxs-lookup"><span data-stu-id="ceabd-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="ceabd-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ceabd-108">EXAMPLES</span></span>

### <span data-ttu-id="ceabd-109">Пример 1: получение определенной группы доступности</span><span class="sxs-lookup"><span data-stu-id="ceabd-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="ceabd-110">Эта команда получает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ceabd-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="ceabd-111">Пример 2: получение всех наборов доступности</span><span class="sxs-lookup"><span data-stu-id="ceabd-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="ceabd-112">Эта команда получает все наборы доступности в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ceabd-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="ceabd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ceabd-113">PARAMETERS</span></span>

### <span data-ttu-id="ceabd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceabd-114">-DefaultProfile</span></span>
<span data-ttu-id="ceabd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ceabd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceabd-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ceabd-116">-Name</span></span>
<span data-ttu-id="ceabd-117">Указывает имя набора доступности, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ceabd-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceabd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceabd-118">-ResourceGroupName</span></span>
<span data-ttu-id="ceabd-119">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ceabd-119">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceabd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceabd-120">CommonParameters</span></span>
<span data-ttu-id="ceabd-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ceabd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceabd-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceabd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceabd-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ceabd-123">INPUTS</span></span>

### <span data-ttu-id="ceabd-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ceabd-124">System.String</span></span>

## <span data-ttu-id="ceabd-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ceabd-125">OUTPUTS</span></span>

### <span data-ttu-id="ceabd-126">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ceabd-126">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="ceabd-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="ceabd-127">NOTES</span></span>

## <span data-ttu-id="ceabd-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ceabd-128">RELATED LINKS</span></span>

[<span data-ttu-id="ceabd-129">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ceabd-129">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="ceabd-130">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ceabd-130">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


