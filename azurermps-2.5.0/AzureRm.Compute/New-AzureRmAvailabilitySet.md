---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: f08de8d1ea5f157270617c69a2092764d0ad4657
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913494"
---
# <span data-ttu-id="09bb7-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="09bb7-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="09bb7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="09bb7-103">Создает группу доступности Azure.</span><span class="sxs-lookup"><span data-stu-id="09bb7-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09bb7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09bb7-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09bb7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09bb7-105">DESCRIPTION</span></span>
<span data-ttu-id="09bb7-106">Командлет **New-AzureRmAvailabilitySet** создает группу доступности Azure.</span><span class="sxs-lookup"><span data-stu-id="09bb7-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="09bb7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09bb7-107">EXAMPLES</span></span>

### <span data-ttu-id="09bb7-108">Пример 1: создание группы доступности</span><span class="sxs-lookup"><span data-stu-id="09bb7-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="09bb7-109">Эта команда создает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="09bb7-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="09bb7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09bb7-110">PARAMETERS</span></span>

### <span data-ttu-id="09bb7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09bb7-111">-AsJob</span></span>
<span data-ttu-id="09bb7-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="09bb7-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09bb7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09bb7-113">-DefaultProfile</span></span>
<span data-ttu-id="09bb7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="09bb7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09bb7-115">-Location</span><span class="sxs-lookup"><span data-stu-id="09bb7-115">-Location</span></span>
<span data-ttu-id="09bb7-116">Указывает расположение для группы доступности.</span><span class="sxs-lookup"><span data-stu-id="09bb7-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="09bb7-117">-Managed</span><span class="sxs-lookup"><span data-stu-id="09bb7-117">-Managed</span></span>
<span data-ttu-id="09bb7-118">Управляемая установка доступности</span><span class="sxs-lookup"><span data-stu-id="09bb7-118">Managed Availability Set</span></span>
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

### <span data-ttu-id="09bb7-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="09bb7-119">-Name</span></span>
<span data-ttu-id="09bb7-120">Указывает имя для группы доступности.</span><span class="sxs-lookup"><span data-stu-id="09bb7-120">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="09bb7-121">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="09bb7-121">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="09bb7-122">Указывает количество доменов сбоя платформы.</span><span class="sxs-lookup"><span data-stu-id="09bb7-122">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="09bb7-123">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="09bb7-123">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="09bb7-124">Указывает число доменов обновления платформы.</span><span class="sxs-lookup"><span data-stu-id="09bb7-124">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="09bb7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09bb7-125">-ResourceGroupName</span></span>
<span data-ttu-id="09bb7-126">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="09bb7-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="09bb7-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="09bb7-127">-Sku</span></span>
<span data-ttu-id="09bb7-128">Название SKU</span><span class="sxs-lookup"><span data-stu-id="09bb7-128">The Name of Sku</span></span>
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

### <span data-ttu-id="09bb7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09bb7-129">CommonParameters</span></span>
<span data-ttu-id="09bb7-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09bb7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09bb7-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09bb7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09bb7-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09bb7-132">INPUTS</span></span>

### <span data-ttu-id="09bb7-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="09bb7-133">None</span></span>
<span data-ttu-id="09bb7-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="09bb7-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09bb7-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09bb7-135">OUTPUTS</span></span>

### <span data-ttu-id="09bb7-136">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="09bb7-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="09bb7-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="09bb7-137">NOTES</span></span>

## <span data-ttu-id="09bb7-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09bb7-138">RELATED LINKS</span></span>

[<span data-ttu-id="09bb7-139">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="09bb7-139">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="09bb7-140">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="09bb7-140">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


