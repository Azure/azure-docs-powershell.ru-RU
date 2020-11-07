---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 1864b4c2dcbd4b3d9934ffb15c54fae18082c920
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911523"
---
# <span data-ttu-id="3267b-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="3267b-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="3267b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3267b-102">SYNOPSIS</span></span>
<span data-ttu-id="3267b-103">Возвращает все версии для расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="3267b-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="3267b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3267b-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3267b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3267b-105">DESCRIPTION</span></span>
<span data-ttu-id="3267b-106">Командлет **Get-AzVMExtensionImage** получает все версии для расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="3267b-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="3267b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3267b-107">EXAMPLES</span></span>

### <span data-ttu-id="3267b-108">Пример 1: получение версий изображения расширения</span><span class="sxs-lookup"><span data-stu-id="3267b-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="3267b-109">Эта команда получает все версии изображения расширения для указанных места, издателя и типа.</span><span class="sxs-lookup"><span data-stu-id="3267b-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="3267b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3267b-110">PARAMETERS</span></span>

### <span data-ttu-id="3267b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3267b-111">-DefaultProfile</span></span>
<span data-ttu-id="3267b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3267b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3267b-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="3267b-113">-FilterExpression</span></span>
<span data-ttu-id="3267b-114">Задает выражение фильтра.</span><span class="sxs-lookup"><span data-stu-id="3267b-114">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="3267b-115">-Location</span><span class="sxs-lookup"><span data-stu-id="3267b-115">-Location</span></span>
<span data-ttu-id="3267b-116">Указывает расположение расширения.</span><span class="sxs-lookup"><span data-stu-id="3267b-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="3267b-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="3267b-117">-PublisherName</span></span>
<span data-ttu-id="3267b-118">Указывает имя издателя расширений.</span><span class="sxs-lookup"><span data-stu-id="3267b-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="3267b-119">Чтобы получить издатель расширения, используйте командлет Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="3267b-119">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="3267b-120">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="3267b-120">-Type</span></span>
<span data-ttu-id="3267b-121">Указывает тип расширения.</span><span class="sxs-lookup"><span data-stu-id="3267b-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="3267b-122">Чтобы получить тип расширения, используйте командлет Get-AzVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="3267b-122">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="3267b-123">-Version</span><span class="sxs-lookup"><span data-stu-id="3267b-123">-Version</span></span>
<span data-ttu-id="3267b-124">Указывает версию расширения, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3267b-124">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3267b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3267b-125">CommonParameters</span></span>
<span data-ttu-id="3267b-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3267b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3267b-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3267b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3267b-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3267b-128">INPUTS</span></span>

### <span data-ttu-id="3267b-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="3267b-129">None</span></span>
<span data-ttu-id="3267b-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3267b-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3267b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3267b-131">OUTPUTS</span></span>

### <span data-ttu-id="3267b-132">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="3267b-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="3267b-133">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="3267b-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="3267b-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="3267b-134">NOTES</span></span>

## <span data-ttu-id="3267b-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3267b-135">RELATED LINKS</span></span>

[<span data-ttu-id="3267b-136">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="3267b-136">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="3267b-137">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3267b-137">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="3267b-138">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3267b-138">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


