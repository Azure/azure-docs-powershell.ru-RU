---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: 7010808e1879566d3b0fc78f82d0e9f82bdd626b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733399"
---
# <span data-ttu-id="7e208-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="7e208-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="7e208-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e208-102">SYNOPSIS</span></span>
<span data-ttu-id="7e208-103">Возвращает все версии для расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="7e208-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e208-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e208-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e208-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e208-105">DESCRIPTION</span></span>
<span data-ttu-id="7e208-106">Командлет **Get-AzureRmVMExtensionImage** получает все версии для расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="7e208-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="7e208-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e208-107">EXAMPLES</span></span>

### <span data-ttu-id="7e208-108">Пример 1: получение версий изображения расширения</span><span class="sxs-lookup"><span data-stu-id="7e208-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="7e208-109">Эта команда получает все версии изображения расширения для указанных места, издателя и типа.</span><span class="sxs-lookup"><span data-stu-id="7e208-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="7e208-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e208-110">PARAMETERS</span></span>

### <span data-ttu-id="7e208-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e208-111">-DefaultProfile</span></span>
<span data-ttu-id="7e208-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e208-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e208-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="7e208-113">-FilterExpression</span></span>
<span data-ttu-id="7e208-114">Задает выражение фильтра.</span><span class="sxs-lookup"><span data-stu-id="7e208-114">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="7e208-115">-Location</span><span class="sxs-lookup"><span data-stu-id="7e208-115">-Location</span></span>
<span data-ttu-id="7e208-116">Указывает расположение расширения.</span><span class="sxs-lookup"><span data-stu-id="7e208-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="7e208-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="7e208-117">-PublisherName</span></span>
<span data-ttu-id="7e208-118">Указывает имя издателя расширений.</span><span class="sxs-lookup"><span data-stu-id="7e208-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="7e208-119">Чтобы получить издатель расширения, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="7e208-119">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="7e208-120">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="7e208-120">-Type</span></span>
<span data-ttu-id="7e208-121">Указывает тип расширения.</span><span class="sxs-lookup"><span data-stu-id="7e208-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="7e208-122">Чтобы получить тип расширения, используйте командлет Get-AzureRmVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="7e208-122">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="7e208-123">-Version</span><span class="sxs-lookup"><span data-stu-id="7e208-123">-Version</span></span>
<span data-ttu-id="7e208-124">Указывает версию расширения, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7e208-124">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7e208-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e208-125">CommonParameters</span></span>
<span data-ttu-id="7e208-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e208-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e208-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e208-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e208-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e208-128">INPUTS</span></span>

## <span data-ttu-id="7e208-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e208-129">OUTPUTS</span></span>

## <span data-ttu-id="7e208-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e208-130">NOTES</span></span>

## <span data-ttu-id="7e208-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e208-131">RELATED LINKS</span></span>

[<span data-ttu-id="7e208-132">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="7e208-132">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="7e208-133">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="7e208-133">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="7e208-134">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7e208-134">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


