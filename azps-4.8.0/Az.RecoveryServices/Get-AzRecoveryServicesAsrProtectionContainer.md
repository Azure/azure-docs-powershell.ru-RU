---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 6db09c69d112e2638026fde97d586f7945f0508e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077699"
---
# <span data-ttu-id="e13fd-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e13fd-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="e13fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e13fd-102">SYNOPSIS</span></span>
<span data-ttu-id="e13fd-103">Возвращает контейнеры защиты ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e13fd-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="e13fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e13fd-104">SYNTAX</span></span>

### <span data-ttu-id="e13fd-105">ByFabricObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e13fd-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e13fd-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e13fd-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e13fd-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e13fd-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e13fd-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e13fd-108">DESCRIPTION</span></span>
<span data-ttu-id="e13fd-109">Командлет **Get-AzRecoveryServicesAsrProtectionContainer** получает контейнеры защиты Azure Site Recovery в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e13fd-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="e13fd-110">Контейнер защиты — это логический контейнер, предназначенный для защиты (обнаруженных) и защищенных объектов, таких как виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="e13fd-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="e13fd-111">Политики репликации определяют параметры репликации для защищенных элементов и могут быть связаны с контейнером защиты и применяются к защищенному элементу.</span><span class="sxs-lookup"><span data-stu-id="e13fd-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="e13fd-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e13fd-112">EXAMPLES</span></span>

### <span data-ttu-id="e13fd-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e13fd-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="e13fd-114">Список контейнеров защиты в $fabricе структуры.</span><span class="sxs-lookup"><span data-stu-id="e13fd-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="e13fd-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e13fd-115">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="e13fd-116">Контейнер защиты в структуре $fabric с именем.</span><span class="sxs-lookup"><span data-stu-id="e13fd-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="e13fd-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e13fd-117">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="e13fd-118">Контейнер защиты в структуре $fabric с понятным именем.</span><span class="sxs-lookup"><span data-stu-id="e13fd-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="e13fd-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e13fd-119">PARAMETERS</span></span>

### <span data-ttu-id="e13fd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e13fd-120">-DefaultProfile</span></span>
<span data-ttu-id="e13fd-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e13fd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e13fd-122">-Fabric</span><span class="sxs-lookup"><span data-stu-id="e13fd-122">-Fabric</span></span>
<span data-ttu-id="e13fd-123">Найдите контейнер защиты в указанной структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="e13fd-123">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e13fd-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e13fd-124">-FriendlyName</span></span>
<span data-ttu-id="e13fd-125">Указывает понятное имя контейнера защиты ASR для поиска.</span><span class="sxs-lookup"><span data-stu-id="e13fd-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="e13fd-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e13fd-126">-Name</span></span>
<span data-ttu-id="e13fd-127">Указывает имя контейнера защиты ASR для поиска.</span><span class="sxs-lookup"><span data-stu-id="e13fd-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="e13fd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e13fd-128">CommonParameters</span></span>
<span data-ttu-id="e13fd-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e13fd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e13fd-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e13fd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e13fd-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e13fd-131">INPUTS</span></span>

### <span data-ttu-id="e13fd-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e13fd-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="e13fd-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e13fd-133">OUTPUTS</span></span>

### <span data-ttu-id="e13fd-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e13fd-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="e13fd-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e13fd-135">NOTES</span></span>

## <span data-ttu-id="e13fd-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e13fd-136">RELATED LINKS</span></span>
