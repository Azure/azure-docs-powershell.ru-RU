---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: 4a348d4e3aa6089ae3e8f3c0bdf871156111ce93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570235"
---
# <span data-ttu-id="3f5e8-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="3f5e8-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="3f5e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f5e8-102">SYNOPSIS</span></span>
<span data-ttu-id="3f5e8-103">Возвращает все версии для расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="3f5e8-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f5e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f5e8-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f5e8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f5e8-105">DESCRIPTION</span></span>
<span data-ttu-id="3f5e8-106">Командлет **Get-AzureRmVMExtensionImage** получает все версии для расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="3f5e8-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="3f5e8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f5e8-107">EXAMPLES</span></span>

### <span data-ttu-id="3f5e8-108">Пример 1: получение версий изображения расширения</span><span class="sxs-lookup"><span data-stu-id="3f5e8-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="3f5e8-109">Эта команда получает все версии изображения расширения для указанных места, издателя и типа.</span><span class="sxs-lookup"><span data-stu-id="3f5e8-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="3f5e8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f5e8-110">PARAMETERS</span></span>

### <span data-ttu-id="3f5e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f5e8-111">-DefaultProfile</span></span>
<span data-ttu-id="3f5e8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f5e8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f5e8-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="3f5e8-113">-FilterExpression</span></span>
<span data-ttu-id="3f5e8-114">Задает выражение фильтра.</span><span class="sxs-lookup"><span data-stu-id="3f5e8-114">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5e8-115">-Location</span><span class="sxs-lookup"><span data-stu-id="3f5e8-115">-Location</span></span>
<span data-ttu-id="3f5e8-116">Указывает расположение расширения.</span><span class="sxs-lookup"><span data-stu-id="3f5e8-116">Specifies the location of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f5e8-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="3f5e8-117">-PublisherName</span></span>
<span data-ttu-id="3f5e8-118">Указывает имя издателя расширений.</span><span class="sxs-lookup"><span data-stu-id="3f5e8-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="3f5e8-119">Чтобы получить издатель расширения, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="3f5e8-119">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f5e8-120">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="3f5e8-120">-Type</span></span>
<span data-ttu-id="3f5e8-121">Указывает тип расширения.</span><span class="sxs-lookup"><span data-stu-id="3f5e8-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="3f5e8-122">Чтобы получить тип расширения, используйте командлет Get-AzureRmVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="3f5e8-122">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f5e8-123">-Version</span><span class="sxs-lookup"><span data-stu-id="3f5e8-123">-Version</span></span>
<span data-ttu-id="3f5e8-124">Указывает версию расширения, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3f5e8-124">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3f5e8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f5e8-125">CommonParameters</span></span>
<span data-ttu-id="3f5e8-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f5e8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f5e8-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f5e8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f5e8-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f5e8-128">INPUTS</span></span>

### <span data-ttu-id="3f5e8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3f5e8-129">System.String</span></span>

## <span data-ttu-id="3f5e8-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f5e8-130">OUTPUTS</span></span>

### <span data-ttu-id="3f5e8-131">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="3f5e8-131">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="3f5e8-132">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="3f5e8-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="3f5e8-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f5e8-133">NOTES</span></span>

## <span data-ttu-id="3f5e8-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f5e8-134">RELATED LINKS</span></span>

[<span data-ttu-id="3f5e8-135">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="3f5e8-135">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="3f5e8-136">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="3f5e8-136">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="3f5e8-137">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3f5e8-137">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


