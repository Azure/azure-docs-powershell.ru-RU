---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/add-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: d9ba42966efd4445fa561dff78b69d7e789badb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911642"
---
# <span data-ttu-id="3e8e6-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="3e8e6-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="3e8e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e8e6-102">SYNOPSIS</span></span>
<span data-ttu-id="3e8e6-103">Отправляет элемент коллекции поставщика в хранилище.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="3e8e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e8e6-104">SYNTAX</span></span>

### <span data-ttu-id="3e8e6-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e8e6-105">CreateExpanded (Default)</span></span>
```
Add-AzsGalleryItem [-SubscriptionId <String>] [-GalleryItemUri <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3e8e6-106">Заново</span><span class="sxs-lookup"><span data-stu-id="3e8e6-106">Create</span></span>
```
Add-AzsGalleryItem -GalleryItemUriPayload <IGalleryItemUriPayload> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3e8e6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e8e6-107">DESCRIPTION</span></span>
<span data-ttu-id="3e8e6-108">Отправляет элемент коллекции поставщика в хранилище.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-108">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="3e8e6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e8e6-109">EXAMPLES</span></span>

### <span data-ttu-id="3e8e6-110">Пример 1: Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="3e8e6-110">Example 1: Add-AzsGalleryItem</span></span>
```powershell
PS C:\> Add-AzsGalleryItem -GalleryItemUri https://testsa.blob.redmond.ext-n35r1010.masd.stbtest.microsoft.com/testsc/TestUbuntu.Test.1.0.0.azpkg

Name                  Publisher  PublisherDisplayName ItemName ItemDisplayName       Version Summary
----                  ---------  -------------------- -------- ---------------       ------- -------
TestUbuntu.Test.1.0.0 TestUbuntu TestUbuntu           Test     Test.TestUbuntu.1.0.0 1.0.0   Create a simple VM

```

<span data-ttu-id="3e8e6-111">Выгрузка TestUbuntu. Test. 1.0.0 в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-111">Uploads TestUbuntu.Test.1.0.0 to the gallery.</span></span>

## <span data-ttu-id="3e8e6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e8e6-112">PARAMETERS</span></span>

### <span data-ttu-id="3e8e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e8e6-113">-DefaultProfile</span></span>
<span data-ttu-id="3e8e6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e8e6-115">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="3e8e6-115">-GalleryItemUri</span></span>
<span data-ttu-id="3e8e6-116">Универсальный код ресурса (URI) для пакета коллекции, уже загруженный через Интернет.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-116">URI for your gallery package that has already been uploaded online.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e8e6-117">-GalleryItemUriPayload</span><span class="sxs-lookup"><span data-stu-id="3e8e6-117">-GalleryItemUriPayload</span></span>
<span data-ttu-id="3e8e6-118">Расположение полезных данных элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-118">Location of gallery item payload.</span></span>
<span data-ttu-id="3e8e6-119">Для конструирования ознакомьтесь с разделом "Заметки" для свойств GALLERYITEMURIPAYLOAD и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-119">To construct, see NOTES section for GALLERYITEMURIPAYLOAD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3e8e6-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e8e6-120">-SubscriptionId</span></span>
<span data-ttu-id="3e8e6-121">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-121">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3e8e6-122">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-122">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e8e6-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e8e6-123">-Confirm</span></span>
<span data-ttu-id="3e8e6-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e8e6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e8e6-125">-WhatIf</span></span>
<span data-ttu-id="3e8e6-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e8e6-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e8e6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e8e6-128">CommonParameters</span></span>
<span data-ttu-id="3e8e6-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e8e6-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e8e6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e8e6-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e8e6-131">INPUTS</span></span>

### <span data-ttu-id="3e8e6-132">Microsoft. Azure. PowerShell. командлеты. Gallery. Model. Api20150401. IGalleryItemUriPayload</span><span class="sxs-lookup"><span data-stu-id="3e8e6-132">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload</span></span>

## <span data-ttu-id="3e8e6-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e8e6-133">OUTPUTS</span></span>

### <span data-ttu-id="3e8e6-134">Microsoft. Azure. PowerShell. командлеты. Gallery. Model. Api20150401. IGalleryItem</span><span class="sxs-lookup"><span data-stu-id="3e8e6-134">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItem</span></span>



## <span data-ttu-id="3e8e6-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e8e6-135">NOTES</span></span>

<span data-ttu-id="3e8e6-136">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e8e6-137">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3e8e6-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload> : расположение полезных данных элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload>: Location of gallery item payload.</span></span>
  - <span data-ttu-id="3e8e6-139">`[GalleryItemUri <String>]`: Универсальный код ресурса (URI) для пакета коллекции, уже загруженный через Интернет.</span><span class="sxs-lookup"><span data-stu-id="3e8e6-139">`[GalleryItemUri <String>]`: URI for your gallery package that has already been uploaded online.</span></span>

## <span data-ttu-id="3e8e6-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e8e6-140">RELATED LINKS</span></span>

