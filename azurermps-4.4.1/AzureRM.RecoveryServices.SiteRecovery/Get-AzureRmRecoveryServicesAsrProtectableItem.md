---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: b209c706a8da88cfc5188b11302166469749c33f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568700"
---
# <span data-ttu-id="7c24b-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7c24b-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="7c24b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c24b-102">SYNOPSIS</span></span>
<span data-ttu-id="7c24b-103">Получение защищенных элементов в контейнере защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="7c24b-103">Get the protectable items in an ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c24b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c24b-104">SYNTAX</span></span>

### <span data-ttu-id="7c24b-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7c24b-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="7c24b-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="7c24b-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="7c24b-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7c24b-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="7c24b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c24b-108">DESCRIPTION</span></span>
<span data-ttu-id="7c24b-109">Командлет **Get-AzureRmRecoveryServicesAsrProtectableItem** получает защищенные элементы в контейнере защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7c24b-109">The **Get-AzureRmRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="7c24b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c24b-110">EXAMPLES</span></span>

### <span data-ttu-id="7c24b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7c24b-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="7c24b-112">Получает все защищенные элементы в указанном контейнере защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="7c24b-112">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="7c24b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c24b-113">PARAMETERS</span></span>

### <span data-ttu-id="7c24b-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7c24b-114">-FriendlyName</span></span>
<span data-ttu-id="7c24b-115">Указывает понятное имя защищенного элемента ASR.</span><span class="sxs-lookup"><span data-stu-id="7c24b-115">Specifies the friendly name of the ASR protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c24b-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7c24b-116">-Name</span></span>
<span data-ttu-id="7c24b-117">Указывает имя защищенного элемента ASR.</span><span class="sxs-lookup"><span data-stu-id="7c24b-117">Specifies the name of the ASR protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c24b-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7c24b-118">-ProtectionContainer</span></span>
<span data-ttu-id="7c24b-119">Указывает объект контейнера защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7c24b-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c24b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c24b-120">CommonParameters</span></span>
<span data-ttu-id="7c24b-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c24b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c24b-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c24b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c24b-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c24b-123">INPUTS</span></span>

### <span data-ttu-id="7c24b-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7c24b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="7c24b-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c24b-125">OUTPUTS</span></span>

### <span data-ttu-id="7c24b-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="7c24b-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7c24b-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c24b-127">NOTES</span></span>

## <span data-ttu-id="7c24b-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c24b-128">RELATED LINKS</span></span>

[<span data-ttu-id="7c24b-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7c24b-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="7c24b-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7c24b-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzureRmRecoveryServicesAsrProtectionEntity.md)
