---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: c4af2c651438659508e231bf2710e88de19830cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565465"
---
# <span data-ttu-id="52b2a-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="52b2a-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="52b2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="52b2a-103">Получает тип расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="52b2a-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52b2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52b2a-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52b2a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52b2a-105">DESCRIPTION</span></span>
<span data-ttu-id="52b2a-106">Командлет **Get-AzureRmVMExtensionImageType** получает тип расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="52b2a-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="52b2a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52b2a-107">EXAMPLES</span></span>

### <span data-ttu-id="52b2a-108">Пример 1: получение типа изображения расширения</span><span class="sxs-lookup"><span data-stu-id="52b2a-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="52b2a-109">Эта команда получает тип изображения расширения для указанного издателя и места.</span><span class="sxs-lookup"><span data-stu-id="52b2a-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="52b2a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52b2a-110">PARAMETERS</span></span>

### <span data-ttu-id="52b2a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b2a-111">-DefaultProfile</span></span>
<span data-ttu-id="52b2a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52b2a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52b2a-113">-Location</span><span class="sxs-lookup"><span data-stu-id="52b2a-113">-Location</span></span>
<span data-ttu-id="52b2a-114">Указывает расположение расширения.</span><span class="sxs-lookup"><span data-stu-id="52b2a-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="52b2a-115">Этот командлет получает тип расширения в расположении, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="52b2a-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="52b2a-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="52b2a-116">-PublisherName</span></span>
<span data-ttu-id="52b2a-117">Указывает имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="52b2a-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="52b2a-118">Чтобы получить издатель расширения, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="52b2a-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="52b2a-119">Этот командлет получает тип расширения от издателя, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="52b2a-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="52b2a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b2a-120">CommonParameters</span></span>
<span data-ttu-id="52b2a-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52b2a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b2a-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52b2a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b2a-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52b2a-123">INPUTS</span></span>

### <span data-ttu-id="52b2a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="52b2a-124">System.String</span></span>

## <span data-ttu-id="52b2a-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52b2a-125">OUTPUTS</span></span>

### <span data-ttu-id="52b2a-126">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="52b2a-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="52b2a-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="52b2a-127">NOTES</span></span>

## <span data-ttu-id="52b2a-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52b2a-128">RELATED LINKS</span></span>

[<span data-ttu-id="52b2a-129">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="52b2a-129">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="52b2a-130">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="52b2a-130">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


