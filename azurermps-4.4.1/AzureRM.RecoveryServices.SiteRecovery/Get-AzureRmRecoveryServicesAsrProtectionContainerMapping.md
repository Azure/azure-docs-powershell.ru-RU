---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 06dca346610af2f5ba54eef1c509d18a3465f34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568697"
---
# <span data-ttu-id="d17b1-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d17b1-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="d17b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d17b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d17b1-103">Получение сопоставлений контейнеров для восстановления сайта Azure site Protection.</span><span class="sxs-lookup"><span data-stu-id="d17b1-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d17b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d17b1-104">SYNTAX</span></span>

### <span data-ttu-id="d17b1-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d17b1-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="d17b1-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d17b1-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="d17b1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d17b1-107">DESCRIPTION</span></span>
<span data-ttu-id="d17b1-108">Командлет **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** получает сведения о контейнере защиты для сопоставлений политик репликации (Ассоциация) в хранилище для указанного контейнера защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="d17b1-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="d17b1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d17b1-109">EXAMPLES</span></span>

### <span data-ttu-id="d17b1-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d17b1-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="d17b1-111">Получает все сопоставления контейнеров защиты для указанного контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="d17b1-111">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="d17b1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d17b1-112">PARAMETERS</span></span>

### <span data-ttu-id="d17b1-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d17b1-113">-Name</span></span>
<span data-ttu-id="d17b1-114">Указывает имя сопоставления контейнера защиты, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="d17b1-114">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="d17b1-115">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d17b1-115">-ProtectionContainer</span></span>
<span data-ttu-id="d17b1-116">Получение сопоставлений контейнеров защиты, соответствующих указанному объекту контейнера защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="d17b1-116">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

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

### <span data-ttu-id="d17b1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d17b1-117">CommonParameters</span></span>
<span data-ttu-id="d17b1-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d17b1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d17b1-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d17b1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d17b1-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d17b1-120">INPUTS</span></span>

### <span data-ttu-id="d17b1-121">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d17b1-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="d17b1-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d17b1-122">OUTPUTS</span></span>

### <span data-ttu-id="d17b1-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="d17b1-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d17b1-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="d17b1-124">NOTES</span></span>

## <span data-ttu-id="d17b1-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d17b1-125">RELATED LINKS</span></span>

[<span data-ttu-id="d17b1-126">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d17b1-126">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="d17b1-127">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d17b1-127">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
