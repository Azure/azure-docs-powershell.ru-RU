---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
ms.openlocfilehash: bff748b8c867b272208469d34229cc2724bc8610
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561068"
---
# <span data-ttu-id="ce1d5-101">Get-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="ce1d5-101">Get-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="ce1d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce1d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ce1d5-103">Получение и перечисление версий изображений коллекции.</span><span class="sxs-lookup"><span data-stu-id="ce1d5-103">Get or list gallery image versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce1d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce1d5-104">SYNTAX</span></span>

### <span data-ttu-id="ce1d5-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ce1d5-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce1d5-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ce1d5-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce1d5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce1d5-107">DESCRIPTION</span></span>
<span data-ttu-id="ce1d5-108">Получение и перечисление версий изображений коллекции.</span><span class="sxs-lookup"><span data-stu-id="ce1d5-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="ce1d5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce1d5-109">EXAMPLES</span></span>

### <span data-ttu-id="ce1d5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ce1d5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="ce1d5-111">Получить версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="ce1d5-111">Get the gallery image version.</span></span>

## <span data-ttu-id="ce1d5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce1d5-112">PARAMETERS</span></span>

### <span data-ttu-id="ce1d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce1d5-113">-DefaultProfile</span></span>
<span data-ttu-id="ce1d5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce1d5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce1d5-115">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="ce1d5-115">-ExpandReplicationStatus</span></span>
<span data-ttu-id="ce1d5-116">Показать состояние репликации.</span><span class="sxs-lookup"><span data-stu-id="ce1d5-116">Show replication status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1d5-117">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="ce1d5-117">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="ce1d5-118">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="ce1d5-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1d5-119">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="ce1d5-119">-GalleryName</span></span>
<span data-ttu-id="ce1d5-120">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="ce1d5-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1d5-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ce1d5-121">-Name</span></span>
<span data-ttu-id="ce1d5-122">Имя версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="ce1d5-122">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1d5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce1d5-123">-ResourceGroupName</span></span>
<span data-ttu-id="ce1d5-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ce1d5-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1d5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce1d5-125">-ResourceId</span></span>
<span data-ttu-id="ce1d5-126">Идентификатор ресурса для версии изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="ce1d5-126">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="ce1d5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce1d5-127">CommonParameters</span></span>
<span data-ttu-id="ce1d5-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce1d5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce1d5-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce1d5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce1d5-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce1d5-130">INPUTS</span></span>

### <span data-ttu-id="ce1d5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ce1d5-131">System.String</span></span>

### <span data-ttu-id="ce1d5-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="ce1d5-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="ce1d5-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce1d5-133">OUTPUTS</span></span>

### <span data-ttu-id="ce1d5-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="ce1d5-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="ce1d5-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce1d5-135">NOTES</span></span>

## <span data-ttu-id="ce1d5-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce1d5-136">RELATED LINKS</span></span>
