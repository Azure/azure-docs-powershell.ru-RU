---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextensionimagetype
schema: 2.0.0
ms.openlocfilehash: 3a310588b77888851684638911f88af95d600db7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913925"
---
# <span data-ttu-id="8c2d3-101">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="8c2d3-101">Get-AzureRmVMExtensionImageType</span></span>

## <span data-ttu-id="8c2d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c2d3-102">SYNOPSIS</span></span>
<span data-ttu-id="8c2d3-103">Получает тип расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="8c2d3-103">Gets the type of an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c2d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c2d3-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c2d3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c2d3-105">DESCRIPTION</span></span>
<span data-ttu-id="8c2d3-106">Командлет **Get-AzureRmVMExtensionImageType** получает тип расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="8c2d3-106">The **Get-AzureRmVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="8c2d3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c2d3-107">EXAMPLES</span></span>

### <span data-ttu-id="8c2d3-108">Пример 1: получение типа изображения расширения</span><span class="sxs-lookup"><span data-stu-id="8c2d3-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="8c2d3-109">Эта команда получает тип изображения расширения для указанного издателя и места.</span><span class="sxs-lookup"><span data-stu-id="8c2d3-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="8c2d3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c2d3-110">PARAMETERS</span></span>

### <span data-ttu-id="8c2d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c2d3-111">-DefaultProfile</span></span>
<span data-ttu-id="8c2d3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c2d3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c2d3-113">-Location</span><span class="sxs-lookup"><span data-stu-id="8c2d3-113">-Location</span></span>
<span data-ttu-id="8c2d3-114">Указывает расположение расширения.</span><span class="sxs-lookup"><span data-stu-id="8c2d3-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="8c2d3-115">Этот командлет получает тип расширения в расположении, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="8c2d3-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="8c2d3-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="8c2d3-116">-PublisherName</span></span>
<span data-ttu-id="8c2d3-117">Указывает имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="8c2d3-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="8c2d3-118">Чтобы получить издатель расширения, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="8c2d3-118">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="8c2d3-119">Этот командлет получает тип расширения от издателя, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="8c2d3-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="8c2d3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c2d3-120">CommonParameters</span></span>
<span data-ttu-id="8c2d3-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c2d3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c2d3-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c2d3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c2d3-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c2d3-123">INPUTS</span></span>

### <span data-ttu-id="8c2d3-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="8c2d3-124">None</span></span>
<span data-ttu-id="8c2d3-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8c2d3-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c2d3-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c2d3-126">OUTPUTS</span></span>

### <span data-ttu-id="8c2d3-127">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="8c2d3-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="8c2d3-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c2d3-128">NOTES</span></span>

## <span data-ttu-id="8c2d3-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c2d3-129">RELATED LINKS</span></span>

[<span data-ttu-id="8c2d3-130">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="8c2d3-130">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="8c2d3-131">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8c2d3-131">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


