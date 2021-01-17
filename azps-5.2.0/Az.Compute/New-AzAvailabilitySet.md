---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: cd61e2119ea84ccfc5fb6a7f5fe597e80c9fd417
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415823"
---
# <span data-ttu-id="857f9-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="857f9-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="857f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="857f9-102">SYNOPSIS</span></span>
<span data-ttu-id="857f9-103">Создает набор доступности Azure.</span><span class="sxs-lookup"><span data-stu-id="857f9-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="857f9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="857f9-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="857f9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="857f9-105">DESCRIPTION</span></span>
<span data-ttu-id="857f9-106">Для создания набора доступности Azure создается набор доступности **New-AzAvailabilitySet.**</span><span class="sxs-lookup"><span data-stu-id="857f9-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="857f9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="857f9-107">EXAMPLES</span></span>

### <span data-ttu-id="857f9-108">Пример 1. Создание набора доступности</span><span class="sxs-lookup"><span data-stu-id="857f9-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="857f9-109">Эта команда создает набор доступности с именем AvailabilitySet03 в группе ресурсов "Группа ресурсов11".</span><span class="sxs-lookup"><span data-stu-id="857f9-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="857f9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="857f9-110">PARAMETERS</span></span>

### <span data-ttu-id="857f9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="857f9-111">-AsJob</span></span>
<span data-ttu-id="857f9-112">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="857f9-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="857f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="857f9-113">-DefaultProfile</span></span>
<span data-ttu-id="857f9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="857f9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="857f9-115">-Location</span><span class="sxs-lookup"><span data-stu-id="857f9-115">-Location</span></span>
<span data-ttu-id="857f9-116">Определяет расположение для набора доступности.</span><span class="sxs-lookup"><span data-stu-id="857f9-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="857f9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="857f9-117">-Name</span></span>
<span data-ttu-id="857f9-118">Указывает имя набора доступности.</span><span class="sxs-lookup"><span data-stu-id="857f9-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="857f9-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="857f9-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="857f9-120">Определяет количество доменов неисправности платформы.</span><span class="sxs-lookup"><span data-stu-id="857f9-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="857f9-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="857f9-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="857f9-122">Указывает количество доменов для обновления платформы.</span><span class="sxs-lookup"><span data-stu-id="857f9-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="857f9-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="857f9-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="857f9-124">ИД ресурса группы расположения расположения близости, который можно использовать с этим набором доступности.</span><span class="sxs-lookup"><span data-stu-id="857f9-124">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="857f9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="857f9-125">-ResourceGroupName</span></span>
<span data-ttu-id="857f9-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="857f9-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="857f9-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="857f9-127">-Sku</span></span>
<span data-ttu-id="857f9-128">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="857f9-128">The Name of Sku.</span></span>
<span data-ttu-id="857f9-129">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="857f9-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="857f9-130">Выровнено: для управляемых дисков</span><span class="sxs-lookup"><span data-stu-id="857f9-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="857f9-131">Классический: для неугодных дисков</span><span class="sxs-lookup"><span data-stu-id="857f9-131">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="857f9-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="857f9-132">-Tag</span></span>
<span data-ttu-id="857f9-133">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="857f9-133">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="857f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857f9-134">CommonParameters</span></span>
<span data-ttu-id="857f9-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="857f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857f9-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="857f9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857f9-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="857f9-137">INPUTS</span></span>

### <span data-ttu-id="857f9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="857f9-138">System.String</span></span>

### <span data-ttu-id="857f9-139">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="857f9-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="857f9-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="857f9-140">OUTPUTS</span></span>

### <span data-ttu-id="857f9-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="857f9-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="857f9-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="857f9-142">NOTES</span></span>

## <span data-ttu-id="857f9-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="857f9-143">RELATED LINKS</span></span>

[<span data-ttu-id="857f9-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="857f9-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="857f9-145">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="857f9-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


