---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5a1d583d9eee535f519b6748867b4026dcc45006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734157"
---
# <span data-ttu-id="35f48-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="35f48-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="35f48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35f48-102">SYNOPSIS</span></span>
<span data-ttu-id="35f48-103">Создает группу доступности Azure.</span><span class="sxs-lookup"><span data-stu-id="35f48-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35f48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35f48-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35f48-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35f48-105">DESCRIPTION</span></span>
<span data-ttu-id="35f48-106">Командлет **New-AzureRmAvailabilitySet** создает группу доступности Azure.</span><span class="sxs-lookup"><span data-stu-id="35f48-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="35f48-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35f48-107">EXAMPLES</span></span>

### <span data-ttu-id="35f48-108">Пример 1: создание группы доступности</span><span class="sxs-lookup"><span data-stu-id="35f48-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="35f48-109">Эта команда создает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="35f48-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="35f48-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35f48-110">PARAMETERS</span></span>

### <span data-ttu-id="35f48-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35f48-111">-AsJob</span></span>
<span data-ttu-id="35f48-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="35f48-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="35f48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f48-113">-DefaultProfile</span></span>
<span data-ttu-id="35f48-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35f48-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35f48-115">-Location</span><span class="sxs-lookup"><span data-stu-id="35f48-115">-Location</span></span>
<span data-ttu-id="35f48-116">Указывает расположение для группы доступности.</span><span class="sxs-lookup"><span data-stu-id="35f48-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="35f48-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35f48-117">-Name</span></span>
<span data-ttu-id="35f48-118">Указывает имя для группы доступности.</span><span class="sxs-lookup"><span data-stu-id="35f48-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="35f48-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="35f48-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="35f48-120">Указывает количество доменов сбоя платформы.</span><span class="sxs-lookup"><span data-stu-id="35f48-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="35f48-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="35f48-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="35f48-122">Указывает число доменов обновления платформы.</span><span class="sxs-lookup"><span data-stu-id="35f48-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="35f48-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35f48-123">-ResourceGroupName</span></span>
<span data-ttu-id="35f48-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35f48-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="35f48-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="35f48-125">-Sku</span></span>
<span data-ttu-id="35f48-126">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="35f48-126">The Name of Sku.</span></span>
<span data-ttu-id="35f48-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="35f48-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35f48-128">Выравнивание: для управляемых дисков</span><span class="sxs-lookup"><span data-stu-id="35f48-128">Aligned: For managed disks</span></span>
- <span data-ttu-id="35f48-129">Классический: для неуправляемых дисков</span><span class="sxs-lookup"><span data-stu-id="35f48-129">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="35f48-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="35f48-130">-Tag</span></span>
<span data-ttu-id="35f48-131">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="35f48-131">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="35f48-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f48-132">CommonParameters</span></span>
<span data-ttu-id="35f48-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35f48-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f48-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35f48-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f48-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35f48-135">INPUTS</span></span>

### <span data-ttu-id="35f48-136">System. String</span><span class="sxs-lookup"><span data-stu-id="35f48-136">System.String</span></span>

### <span data-ttu-id="35f48-137">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="35f48-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="35f48-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35f48-138">OUTPUTS</span></span>

### <span data-ttu-id="35f48-139">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="35f48-139">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="35f48-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="35f48-140">NOTES</span></span>

## <span data-ttu-id="35f48-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35f48-141">RELATED LINKS</span></span>

[<span data-ttu-id="35f48-142">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="35f48-142">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="35f48-143">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="35f48-143">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


