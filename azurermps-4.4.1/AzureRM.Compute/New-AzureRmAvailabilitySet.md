---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 2e3fc51410ff5a6fa9fca2aaeec0fe326012a8bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570092"
---
# <span data-ttu-id="2dd02-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2dd02-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="2dd02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2dd02-102">SYNOPSIS</span></span>
<span data-ttu-id="2dd02-103">Создает группу доступности Azure.</span><span class="sxs-lookup"><span data-stu-id="2dd02-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dd02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2dd02-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dd02-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dd02-105">DESCRIPTION</span></span>
<span data-ttu-id="2dd02-106">Командлет **New-AzureRmAvailabilitySet** создает группу доступности Azure.</span><span class="sxs-lookup"><span data-stu-id="2dd02-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="2dd02-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2dd02-107">EXAMPLES</span></span>

### <span data-ttu-id="2dd02-108">Пример 1: создание группы доступности</span><span class="sxs-lookup"><span data-stu-id="2dd02-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="2dd02-109">Эта команда создает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2dd02-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="2dd02-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2dd02-110">PARAMETERS</span></span>

### <span data-ttu-id="2dd02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dd02-111">-DefaultProfile</span></span>
<span data-ttu-id="2dd02-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2dd02-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dd02-113">-Location</span><span class="sxs-lookup"><span data-stu-id="2dd02-113">-Location</span></span>
<span data-ttu-id="2dd02-114">Указывает расположение для группы доступности.</span><span class="sxs-lookup"><span data-stu-id="2dd02-114">Specifies the location for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd02-115">-Managed</span><span class="sxs-lookup"><span data-stu-id="2dd02-115">-Managed</span></span>
<span data-ttu-id="2dd02-116">Управляемая установка доступности</span><span class="sxs-lookup"><span data-stu-id="2dd02-116">Managed Availability Set</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd02-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2dd02-117">-Name</span></span>
<span data-ttu-id="2dd02-118">Указывает имя для группы доступности.</span><span class="sxs-lookup"><span data-stu-id="2dd02-118">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd02-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="2dd02-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="2dd02-120">Указывает количество доменов сбоя платформы.</span><span class="sxs-lookup"><span data-stu-id="2dd02-120">Specifies the platform fault domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd02-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="2dd02-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="2dd02-122">Указывает число доменов обновления платформы.</span><span class="sxs-lookup"><span data-stu-id="2dd02-122">Specifies the platform update domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd02-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dd02-123">-ResourceGroupName</span></span>
<span data-ttu-id="2dd02-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2dd02-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2dd02-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="2dd02-125">-Sku</span></span>
<span data-ttu-id="2dd02-126">Название SKU</span><span class="sxs-lookup"><span data-stu-id="2dd02-126">The Name of Sku</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd02-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dd02-127">CommonParameters</span></span>
<span data-ttu-id="2dd02-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2dd02-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dd02-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dd02-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dd02-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2dd02-130">INPUTS</span></span>

## <span data-ttu-id="2dd02-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dd02-131">OUTPUTS</span></span>

## <span data-ttu-id="2dd02-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="2dd02-132">NOTES</span></span>

## <span data-ttu-id="2dd02-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2dd02-133">RELATED LINKS</span></span>

[<span data-ttu-id="2dd02-134">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2dd02-134">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="2dd02-135">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2dd02-135">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


