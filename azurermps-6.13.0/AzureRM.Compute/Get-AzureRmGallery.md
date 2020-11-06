---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
ms.openlocfilehash: cdb703144daa6f9abd62aee41eaad94b2cfa50e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561084"
---
# <span data-ttu-id="b91c4-101">Get-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="b91c4-101">Get-AzureRmGallery</span></span>

## <span data-ttu-id="b91c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b91c4-102">SYNOPSIS</span></span>
<span data-ttu-id="b91c4-103">Получение списка коллекций.</span><span class="sxs-lookup"><span data-stu-id="b91c4-103">Get or list galleries.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b91c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b91c4-104">SYNTAX</span></span>

### <span data-ttu-id="b91c4-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b91c4-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGallery [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b91c4-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b91c4-106">ResourceIdParameter</span></span>
```
Get-AzureRmGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b91c4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b91c4-107">DESCRIPTION</span></span>
<span data-ttu-id="b91c4-108">Получение списка коллекций.</span><span class="sxs-lookup"><span data-stu-id="b91c4-108">Get or list galleries.</span></span>

## <span data-ttu-id="b91c4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b91c4-109">EXAMPLES</span></span>

### <span data-ttu-id="b91c4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b91c4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGallery -ResourceGroupName $rgname -GalleryName $galleryName

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="b91c4-111">Получение коллекции.</span><span class="sxs-lookup"><span data-stu-id="b91c4-111">Get the gallery.</span></span>

## <span data-ttu-id="b91c4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b91c4-112">PARAMETERS</span></span>

### <span data-ttu-id="b91c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b91c4-113">-DefaultProfile</span></span>
<span data-ttu-id="b91c4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b91c4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b91c4-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b91c4-115">-Name</span></span>
<span data-ttu-id="b91c4-116">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="b91c4-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b91c4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b91c4-117">-ResourceGroupName</span></span>
<span data-ttu-id="b91c4-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b91c4-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b91c4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b91c4-119">-ResourceId</span></span>
<span data-ttu-id="b91c4-120">Идентификатор ресурса для коллекции</span><span class="sxs-lookup"><span data-stu-id="b91c4-120">The resource id for Gallery</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b91c4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b91c4-121">CommonParameters</span></span>
<span data-ttu-id="b91c4-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b91c4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b91c4-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b91c4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b91c4-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b91c4-124">INPUTS</span></span>

### <span data-ttu-id="b91c4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b91c4-125">System.String</span></span>

### <span data-ttu-id="b91c4-126">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="b91c4-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="b91c4-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b91c4-127">OUTPUTS</span></span>

### <span data-ttu-id="b91c4-128">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="b91c4-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="b91c4-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="b91c4-129">NOTES</span></span>

## <span data-ttu-id="b91c4-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b91c4-130">RELATED LINKS</span></span>
