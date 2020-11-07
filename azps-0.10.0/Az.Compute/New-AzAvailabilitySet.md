---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: 03e121493d8112116f5e8fc6ed492a54b67d47d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911485"
---
# <span data-ttu-id="942e9-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="942e9-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="942e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="942e9-102">SYNOPSIS</span></span>
<span data-ttu-id="942e9-103">Создает группу доступности Azure.</span><span class="sxs-lookup"><span data-stu-id="942e9-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="942e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="942e9-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="942e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="942e9-105">DESCRIPTION</span></span>
<span data-ttu-id="942e9-106">Командлет **New-AzAvailabilitySet** создает группу доступности Azure.</span><span class="sxs-lookup"><span data-stu-id="942e9-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="942e9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="942e9-107">EXAMPLES</span></span>

### <span data-ttu-id="942e9-108">Пример 1: создание группы доступности</span><span class="sxs-lookup"><span data-stu-id="942e9-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="942e9-109">Эта команда создает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="942e9-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="942e9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="942e9-110">PARAMETERS</span></span>

### <span data-ttu-id="942e9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="942e9-111">-AsJob</span></span>
<span data-ttu-id="942e9-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="942e9-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="942e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="942e9-113">-DefaultProfile</span></span>
<span data-ttu-id="942e9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="942e9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="942e9-115">-Location</span><span class="sxs-lookup"><span data-stu-id="942e9-115">-Location</span></span>
<span data-ttu-id="942e9-116">Указывает расположение для группы доступности.</span><span class="sxs-lookup"><span data-stu-id="942e9-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="942e9-117">-Managed</span><span class="sxs-lookup"><span data-stu-id="942e9-117">-Managed</span></span>
<span data-ttu-id="942e9-118">Управляемая установка доступности</span><span class="sxs-lookup"><span data-stu-id="942e9-118">Managed Availability Set</span></span>
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

### <span data-ttu-id="942e9-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="942e9-119">-Name</span></span>
<span data-ttu-id="942e9-120">Указывает имя для группы доступности.</span><span class="sxs-lookup"><span data-stu-id="942e9-120">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="942e9-121">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="942e9-121">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="942e9-122">Указывает количество доменов сбоя платформы.</span><span class="sxs-lookup"><span data-stu-id="942e9-122">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="942e9-123">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="942e9-123">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="942e9-124">Указывает число доменов обновления платформы.</span><span class="sxs-lookup"><span data-stu-id="942e9-124">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="942e9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="942e9-125">-ResourceGroupName</span></span>
<span data-ttu-id="942e9-126">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="942e9-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="942e9-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="942e9-127">-Sku</span></span>
<span data-ttu-id="942e9-128">Название SKU</span><span class="sxs-lookup"><span data-stu-id="942e9-128">The Name of Sku</span></span>
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

### <span data-ttu-id="942e9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="942e9-129">CommonParameters</span></span>
<span data-ttu-id="942e9-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="942e9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="942e9-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="942e9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="942e9-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="942e9-132">INPUTS</span></span>

### <span data-ttu-id="942e9-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="942e9-133">None</span></span>
<span data-ttu-id="942e9-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="942e9-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="942e9-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="942e9-135">OUTPUTS</span></span>

### <span data-ttu-id="942e9-136">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="942e9-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="942e9-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="942e9-137">NOTES</span></span>

## <span data-ttu-id="942e9-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="942e9-138">RELATED LINKS</span></span>

[<span data-ttu-id="942e9-139">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="942e9-139">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="942e9-140">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="942e9-140">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


