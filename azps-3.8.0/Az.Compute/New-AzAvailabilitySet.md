---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: cd61e2119ea84ccfc5fb6a7f5fe597e80c9fd417
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065949"
---
# <span data-ttu-id="f64fa-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f64fa-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="f64fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f64fa-102">SYNOPSIS</span></span>
<span data-ttu-id="f64fa-103">Создает группу доступности Azure.</span><span class="sxs-lookup"><span data-stu-id="f64fa-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="f64fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f64fa-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f64fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f64fa-105">DESCRIPTION</span></span>
<span data-ttu-id="f64fa-106">Командлет **New-AzAvailabilitySet** создает группу доступности Azure.</span><span class="sxs-lookup"><span data-stu-id="f64fa-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="f64fa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f64fa-107">EXAMPLES</span></span>

### <span data-ttu-id="f64fa-108">Пример 1: создание группы доступности</span><span class="sxs-lookup"><span data-stu-id="f64fa-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="f64fa-109">Эта команда создает группу доступности с именем AvailabilitySet03 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f64fa-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="f64fa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f64fa-110">PARAMETERS</span></span>

### <span data-ttu-id="f64fa-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f64fa-111">-AsJob</span></span>
<span data-ttu-id="f64fa-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f64fa-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f64fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f64fa-113">-DefaultProfile</span></span>
<span data-ttu-id="f64fa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f64fa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f64fa-115">-Location</span><span class="sxs-lookup"><span data-stu-id="f64fa-115">-Location</span></span>
<span data-ttu-id="f64fa-116">Указывает расположение для группы доступности.</span><span class="sxs-lookup"><span data-stu-id="f64fa-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="f64fa-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f64fa-117">-Name</span></span>
<span data-ttu-id="f64fa-118">Указывает имя для группы доступности.</span><span class="sxs-lookup"><span data-stu-id="f64fa-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="f64fa-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="f64fa-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="f64fa-120">Указывает количество доменов сбоя платформы.</span><span class="sxs-lookup"><span data-stu-id="f64fa-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="f64fa-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="f64fa-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="f64fa-122">Указывает число доменов обновления платформы.</span><span class="sxs-lookup"><span data-stu-id="f64fa-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="f64fa-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="f64fa-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="f64fa-124">Идентификатор ресурса группы размещения близкого взаимодействия для использования с этой группой доступности.</span><span class="sxs-lookup"><span data-stu-id="f64fa-124">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f64fa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f64fa-125">-ResourceGroupName</span></span>
<span data-ttu-id="f64fa-126">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f64fa-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f64fa-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="f64fa-127">-Sku</span></span>
<span data-ttu-id="f64fa-128">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="f64fa-128">The Name of Sku.</span></span>
<span data-ttu-id="f64fa-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f64fa-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f64fa-130">Выравнивание: для управляемых дисков</span><span class="sxs-lookup"><span data-stu-id="f64fa-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="f64fa-131">Классический: для неуправляемых дисков</span><span class="sxs-lookup"><span data-stu-id="f64fa-131">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="f64fa-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="f64fa-132">-Tag</span></span>
<span data-ttu-id="f64fa-133">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="f64fa-133">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f64fa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f64fa-134">CommonParameters</span></span>
<span data-ttu-id="f64fa-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f64fa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f64fa-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f64fa-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f64fa-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f64fa-137">INPUTS</span></span>

### <span data-ttu-id="f64fa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f64fa-138">System.String</span></span>

### <span data-ttu-id="f64fa-139">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f64fa-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f64fa-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f64fa-140">OUTPUTS</span></span>

### <span data-ttu-id="f64fa-141">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f64fa-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="f64fa-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f64fa-142">NOTES</span></span>

## <span data-ttu-id="f64fa-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f64fa-143">RELATED LINKS</span></span>

[<span data-ttu-id="f64fa-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f64fa-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="f64fa-145">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f64fa-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


