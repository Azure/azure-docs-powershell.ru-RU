---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: b5e9828c0cf9f73f88a44b7a4471a22bbfbe49af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563700"
---
# <span data-ttu-id="4e035-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4e035-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="4e035-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e035-102">SYNOPSIS</span></span>
<span data-ttu-id="4e035-103">Создает группу доступности Azure.</span><span class="sxs-lookup"><span data-stu-id="4e035-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e035-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e035-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [<CommonParameters>]
```

## <span data-ttu-id="4e035-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e035-105">DESCRIPTION</span></span>
<span data-ttu-id="4e035-106">Командлет **New-AzureRmAvailabilitySet** создает группу доступности Azure.</span><span class="sxs-lookup"><span data-stu-id="4e035-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="4e035-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e035-107">EXAMPLES</span></span>

### <span data-ttu-id="4e035-108">Пример 1: создание группы доступности</span><span class="sxs-lookup"><span data-stu-id="4e035-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="4e035-109">Эта команда создает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="4e035-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="4e035-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e035-110">PARAMETERS</span></span>

### <span data-ttu-id="4e035-111">-Location</span><span class="sxs-lookup"><span data-stu-id="4e035-111">-Location</span></span>
<span data-ttu-id="4e035-112">Указывает расположение для группы доступности.</span><span class="sxs-lookup"><span data-stu-id="4e035-112">Specifies the location for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e035-113">-Managed</span><span class="sxs-lookup"><span data-stu-id="4e035-113">-Managed</span></span>
<span data-ttu-id="4e035-114">Управляемая установка доступности</span><span class="sxs-lookup"><span data-stu-id="4e035-114">Managed Availability Set</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e035-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e035-115">-Name</span></span>
<span data-ttu-id="4e035-116">Указывает имя для группы доступности.</span><span class="sxs-lookup"><span data-stu-id="4e035-116">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e035-117">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="4e035-117">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="4e035-118">Указывает количество доменов сбоя платформы.</span><span class="sxs-lookup"><span data-stu-id="4e035-118">Specifies the platform fault domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e035-119">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="4e035-119">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="4e035-120">Указывает число доменов обновления платформы.</span><span class="sxs-lookup"><span data-stu-id="4e035-120">Specifies the platform update domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e035-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e035-121">-ResourceGroupName</span></span>
<span data-ttu-id="4e035-122">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e035-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4e035-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="4e035-123">-Sku</span></span>
<span data-ttu-id="4e035-124">Название SKU</span><span class="sxs-lookup"><span data-stu-id="4e035-124">The Name of Sku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e035-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e035-125">CommonParameters</span></span>
<span data-ttu-id="4e035-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e035-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e035-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e035-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e035-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e035-128">INPUTS</span></span>

### <span data-ttu-id="4e035-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="4e035-129">None</span></span>
<span data-ttu-id="4e035-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4e035-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e035-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e035-131">OUTPUTS</span></span>

## <span data-ttu-id="4e035-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e035-132">NOTES</span></span>

## <span data-ttu-id="4e035-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e035-133">RELATED LINKS</span></span>

[<span data-ttu-id="4e035-134">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4e035-134">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="4e035-135">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4e035-135">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


