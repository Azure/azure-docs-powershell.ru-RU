---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: af4dbdbb2741850cdb01eb88e321f80a4844919a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729722"
---
# <span data-ttu-id="c2406-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c2406-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="c2406-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2406-102">SYNOPSIS</span></span>
<span data-ttu-id="c2406-103">Возвращает свойства элементов, защищенных репликацией Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c2406-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

## <span data-ttu-id="c2406-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2406-104">SYNTAX</span></span>

### <span data-ttu-id="c2406-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2406-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2406-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c2406-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2406-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c2406-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2406-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="c2406-108">ByProtectableItemObject</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2406-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2406-109">DESCRIPTION</span></span>
<span data-ttu-id="c2406-110">Командлет **Get-AzRecoveryServicesAsrReplicationProtectedItem** получает свойства всех или указанного элемента, защищенного РЕПЛИКАЦИей ASR, из указанного контейнера защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="c2406-110">The **Get-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="c2406-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2406-111">EXAMPLES</span></span>

### <span data-ttu-id="c2406-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2406-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="c2406-113">Список всех элементов, защищенных репликацией в указанном контейнере защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="c2406-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="c2406-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2406-114">PARAMETERS</span></span>

### <span data-ttu-id="c2406-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2406-115">-DefaultProfile</span></span>
<span data-ttu-id="c2406-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2406-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c2406-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c2406-117">-FriendlyName</span></span>
<span data-ttu-id="c2406-118">Указывает понятное имя для элемента, защищенного репликацией, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="c2406-118">Specifies the friendly name of the replication protected item to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2406-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2406-119">-Name</span></span>
<span data-ttu-id="c2406-120">Указывает имя защищенного элемента репликации, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="c2406-120">Specifies the name of the replication protected item to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2406-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c2406-121">-ProtectableItem</span></span>
<span data-ttu-id="c2406-122">Указывает объект защищенного элемента ASR.</span><span class="sxs-lookup"><span data-stu-id="c2406-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="c2406-123">Командлет получает защищенный элемент репликации ASR, соответствующий указанному элементу, защищаемому ASR, если элемент защищен.</span><span class="sxs-lookup"><span data-stu-id="c2406-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2406-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c2406-124">-ProtectionContainer</span></span>
<span data-ttu-id="c2406-125">Указывает объект контейнера защиты ASR для контейнера защиты ASR, соответствующего элементу, защищенному репликацией.</span><span class="sxs-lookup"><span data-stu-id="c2406-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2406-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2406-126">CommonParameters</span></span>
<span data-ttu-id="c2406-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2406-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2406-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2406-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2406-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2406-129">INPUTS</span></span>

### <span data-ttu-id="c2406-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c2406-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

### <span data-ttu-id="c2406-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c2406-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="c2406-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2406-132">OUTPUTS</span></span>

### <span data-ttu-id="c2406-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c2406-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c2406-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2406-134">NOTES</span></span>

## <span data-ttu-id="c2406-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2406-135">RELATED LINKS</span></span>

[<span data-ttu-id="c2406-136">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c2406-136">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="c2406-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c2406-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="c2406-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c2406-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
