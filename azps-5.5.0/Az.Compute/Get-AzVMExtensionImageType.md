---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: eb2c92b0efcbcd5333c600fe481e21752a96be9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244149"
---
# <span data-ttu-id="c5bf4-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="c5bf4-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="c5bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="c5bf4-103">Тип расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="c5bf4-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="c5bf4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c5bf4-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5bf4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="c5bf4-106">Для получения расширения Azure возвращается тип расширения **Get-AzVMExtensionImageType.**</span><span class="sxs-lookup"><span data-stu-id="c5bf4-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="c5bf4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c5bf4-107">EXAMPLES</span></span>

### <span data-ttu-id="c5bf4-108">Пример 1. Получить тип изображения расширения</span><span class="sxs-lookup"><span data-stu-id="c5bf4-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="c5bf4-109">Эта команда получает тип изображения расширения для указанного издателя и расположения.</span><span class="sxs-lookup"><span data-stu-id="c5bf4-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="c5bf4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5bf4-110">PARAMETERS</span></span>

### <span data-ttu-id="c5bf4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5bf4-111">-DefaultProfile</span></span>
<span data-ttu-id="c5bf4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5bf4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5bf4-113">-Location</span><span class="sxs-lookup"><span data-stu-id="c5bf4-113">-Location</span></span>
<span data-ttu-id="c5bf4-114">Определяет расположение расширения.</span><span class="sxs-lookup"><span data-stu-id="c5bf4-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="c5bf4-115">Этот cmdlet возвращает тип расширения в указанном месте.</span><span class="sxs-lookup"><span data-stu-id="c5bf4-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="c5bf4-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="c5bf4-116">-PublisherName</span></span>
<span data-ttu-id="c5bf4-117">Указывает имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="c5bf4-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="c5bf4-118">Чтобы получить издателя расширения, воспользуйтесь Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="c5bf4-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="c5bf4-119">Этот cmdlet возвращает тип расширения от издателя, указанного для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="c5bf4-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="c5bf4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5bf4-120">CommonParameters</span></span>
<span data-ttu-id="c5bf4-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5bf4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5bf4-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5bf4-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5bf4-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5bf4-123">INPUTS</span></span>

### <span data-ttu-id="c5bf4-124">System.String</span><span class="sxs-lookup"><span data-stu-id="c5bf4-124">System.String</span></span>

## <span data-ttu-id="c5bf4-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c5bf4-125">OUTPUTS</span></span>

### <span data-ttu-id="c5bf4-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="c5bf4-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="c5bf4-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c5bf4-127">NOTES</span></span>

## <span data-ttu-id="c5bf4-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5bf4-128">RELATED LINKS</span></span>

[<span data-ttu-id="c5bf4-129">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="c5bf4-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="c5bf4-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c5bf4-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


