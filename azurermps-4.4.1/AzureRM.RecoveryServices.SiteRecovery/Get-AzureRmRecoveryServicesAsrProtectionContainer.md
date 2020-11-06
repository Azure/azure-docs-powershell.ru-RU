---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 84a50782e9906271e3943c8cd545780457a1adfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569256"
---
# <span data-ttu-id="63055-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="63055-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="63055-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63055-102">SYNOPSIS</span></span>
<span data-ttu-id="63055-103">Возвращает контейнеры защиты ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="63055-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63055-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63055-104">SYNTAX</span></span>

### <span data-ttu-id="63055-105">ByFabricObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="63055-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="63055-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="63055-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="63055-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="63055-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="63055-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63055-108">DESCRIPTION</span></span>
<span data-ttu-id="63055-109">Командлет **Get-AzureRmRecoveryServicesAsrProtectionContainer** получает контейнеры защиты Azure Site Recovery в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="63055-109">The **Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="63055-110">Контейнер защиты — это логический контейнер, предназначенный для защиты (обнаруженных) и защищенных объектов, таких как виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="63055-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="63055-111">Политики репликации определяют параметры репликации для защищенных элементов и могут быть связаны с контейнером защиты и применяются к защищенному элементу.</span><span class="sxs-lookup"><span data-stu-id="63055-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="63055-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63055-112">EXAMPLES</span></span>

### <span data-ttu-id="63055-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63055-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrProtectionContainer
```

<span data-ttu-id="63055-114">Получает все контейнеры защиты ASR в указанной структуре ASR (входные данные конвейера в приведенном выше примере).</span><span class="sxs-lookup"><span data-stu-id="63055-114">Gets all the ASR protection containers in the specified ASR fabric (the pipeline input in the above example.)</span></span>

## <span data-ttu-id="63055-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63055-115">PARAMETERS</span></span>

### <span data-ttu-id="63055-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="63055-116">-Fabric</span></span>
<span data-ttu-id="63055-117">Найдите контейнер защиты в указанной структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="63055-117">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63055-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="63055-118">-FriendlyName</span></span>
<span data-ttu-id="63055-119">Указывает понятное имя контейнера защиты ASR для поиска.</span><span class="sxs-lookup"><span data-stu-id="63055-119">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="63055-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63055-120">-Name</span></span>
<span data-ttu-id="63055-121">Указывает имя контейнера защиты ASR для поиска.</span><span class="sxs-lookup"><span data-stu-id="63055-121">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="63055-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63055-122">CommonParameters</span></span>
<span data-ttu-id="63055-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63055-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63055-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63055-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63055-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63055-125">INPUTS</span></span>

### <span data-ttu-id="63055-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="63055-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="63055-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63055-127">OUTPUTS</span></span>

### <span data-ttu-id="63055-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="63055-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="63055-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="63055-129">NOTES</span></span>

## <span data-ttu-id="63055-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63055-130">RELATED LINKS</span></span>

