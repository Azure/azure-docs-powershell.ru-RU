---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: fbd2f518d3bdcf64599e32b55cdb9f416c29be21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569252"
---
# <span data-ttu-id="179b6-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="179b6-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="179b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="179b6-102">SYNOPSIS</span></span>
<span data-ttu-id="179b6-103">Возвращает свойства элементов, защищенных репликацией Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="179b6-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="179b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="179b6-104">SYNTAX</span></span>

### <span data-ttu-id="179b6-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="179b6-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="179b6-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="179b6-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### <span data-ttu-id="179b6-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="179b6-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### <span data-ttu-id="179b6-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="179b6-108">ByProtectableItemObject</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [<CommonParameters>]
```

## <span data-ttu-id="179b6-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="179b6-109">DESCRIPTION</span></span>
<span data-ttu-id="179b6-110">Командлет **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** получает свойства всех или указанного элемента, защищенного РЕПЛИКАЦИей ASR, из указанного контейнера защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="179b6-110">The **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="179b6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="179b6-111">EXAMPLES</span></span>

### <span data-ttu-id="179b6-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="179b6-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="179b6-113">Список всех элементов, защищенных репликацией в указанном контейнере защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="179b6-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="179b6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="179b6-114">PARAMETERS</span></span>

### <span data-ttu-id="179b6-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="179b6-115">-FriendlyName</span></span>
<span data-ttu-id="179b6-116">Указывает понятное имя для элемента, защищенного репликацией, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="179b6-116">Specifies the friendly name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="179b6-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="179b6-117">-Name</span></span>
<span data-ttu-id="179b6-118">Указывает имя защищенного элемента репликации, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="179b6-118">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="179b6-119">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="179b6-119">-ProtectableItem</span></span>
<span data-ttu-id="179b6-120">Указывает объект защищенного элемента ASR.</span><span class="sxs-lookup"><span data-stu-id="179b6-120">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="179b6-121">Командлет получает защищенный элемент репликации ASR, соответствующий указанному элементу, защищаемому ASR, если элемент защищен.</span><span class="sxs-lookup"><span data-stu-id="179b6-121">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="179b6-122">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="179b6-122">-ProtectionContainer</span></span>
<span data-ttu-id="179b6-123">Указывает объект контейнера защиты ASR для контейнера защиты ASR, соответствующего элементу, защищенному репликацией.</span><span class="sxs-lookup"><span data-stu-id="179b6-123">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="179b6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="179b6-124">CommonParameters</span></span>
<span data-ttu-id="179b6-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="179b6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="179b6-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="179b6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="179b6-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="179b6-127">INPUTS</span></span>

### <span data-ttu-id="179b6-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="179b6-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>
<span data-ttu-id="179b6-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="179b6-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="179b6-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="179b6-130">OUTPUTS</span></span>

### <span data-ttu-id="179b6-131">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="179b6-131">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="179b6-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="179b6-132">NOTES</span></span>

## <span data-ttu-id="179b6-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="179b6-133">RELATED LINKS</span></span>

[<span data-ttu-id="179b6-134">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="179b6-134">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="179b6-135">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="179b6-135">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="179b6-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="179b6-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
