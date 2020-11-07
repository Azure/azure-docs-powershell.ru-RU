---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimage
schema: 2.0.0
ms.openlocfilehash: ccb48064bb2d6b91801a58ecfa9d229a748889a8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913927"
---
# <span data-ttu-id="b0216-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="b0216-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="b0216-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b0216-102">SYNOPSIS</span></span>
<span data-ttu-id="b0216-103">Возвращает все версии для расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="b0216-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0216-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b0216-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0216-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0216-105">DESCRIPTION</span></span>
<span data-ttu-id="b0216-106">Командлет **Get-AzureRmVMExtensionImage** получает все версии для расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="b0216-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="b0216-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b0216-107">EXAMPLES</span></span>

### <span data-ttu-id="b0216-108">Пример 1: получение версий изображения расширения</span><span class="sxs-lookup"><span data-stu-id="b0216-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="b0216-109">Эта команда получает все версии изображения расширения для указанных места, издателя и типа.</span><span class="sxs-lookup"><span data-stu-id="b0216-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="b0216-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b0216-110">PARAMETERS</span></span>

### <span data-ttu-id="b0216-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0216-111">-DefaultProfile</span></span>
<span data-ttu-id="b0216-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0216-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0216-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="b0216-113">-FilterExpression</span></span>
<span data-ttu-id="b0216-114">Задает выражение фильтра.</span><span class="sxs-lookup"><span data-stu-id="b0216-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0216-115">-Location</span><span class="sxs-lookup"><span data-stu-id="b0216-115">-Location</span></span>
<span data-ttu-id="b0216-116">Указывает расположение расширения.</span><span class="sxs-lookup"><span data-stu-id="b0216-116">Specifies the location of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0216-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="b0216-117">-PublisherName</span></span>
<span data-ttu-id="b0216-118">Указывает имя издателя расширений.</span><span class="sxs-lookup"><span data-stu-id="b0216-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="b0216-119">Чтобы получить издатель расширения, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="b0216-119">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0216-120">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="b0216-120">-Type</span></span>
<span data-ttu-id="b0216-121">Указывает тип расширения.</span><span class="sxs-lookup"><span data-stu-id="b0216-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="b0216-122">Чтобы получить тип расширения, используйте командлет Get-AzureRmVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="b0216-122">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0216-123">-Version</span><span class="sxs-lookup"><span data-stu-id="b0216-123">-Version</span></span>
<span data-ttu-id="b0216-124">Указывает версию расширения, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b0216-124">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0216-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0216-125">CommonParameters</span></span>
<span data-ttu-id="b0216-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b0216-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0216-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0216-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0216-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b0216-128">INPUTS</span></span>

### <span data-ttu-id="b0216-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="b0216-129">None</span></span>
<span data-ttu-id="b0216-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b0216-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b0216-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0216-131">OUTPUTS</span></span>

### <span data-ttu-id="b0216-132">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="b0216-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="b0216-133">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="b0216-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="b0216-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="b0216-134">NOTES</span></span>

## <span data-ttu-id="b0216-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0216-135">RELATED LINKS</span></span>

[<span data-ttu-id="b0216-136">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="b0216-136">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="b0216-137">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b0216-137">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="b0216-138">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="b0216-138">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


