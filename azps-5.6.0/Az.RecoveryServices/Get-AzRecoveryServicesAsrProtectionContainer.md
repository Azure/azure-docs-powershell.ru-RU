---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 1d7f8adfa0db67d66c65c5ac7f3df7c64b665fda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992505"
---
# <span data-ttu-id="a5bb7-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a5bb7-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="a5bb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="a5bb7-103">Получает контейнеры защиты ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="a5bb7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a5bb7-104">SYNTAX</span></span>

### <span data-ttu-id="a5bb7-105">ByFabricObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5bb7-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5bb7-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="a5bb7-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5bb7-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a5bb7-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5bb7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5bb7-108">DESCRIPTION</span></span>
<span data-ttu-id="a5bb7-109">Для получения контейнеров защиты от восстановления сайтов Azure в хранилище служб восстановления возвращается **cmdlet Get-AzRecoveryServicesAsrProtectionContainer.**</span><span class="sxs-lookup"><span data-stu-id="a5bb7-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="a5bb7-110">Контейнер защиты — это логический контейнер для защищенных (обнаруженных) и защищенных объектов, таких как виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="a5bb7-111">Политики репликации определяют параметры репликации для защищенных элементов и могут быть связаны с контейнером защиты и применены к защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="a5bb7-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a5bb7-112">EXAMPLES</span></span>

### <span data-ttu-id="a5bb7-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a5bb7-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="a5bb7-114">Список контейнеров защиты для $fabric.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="a5bb7-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a5bb7-115">Example 2</span></span>
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

<span data-ttu-id="a5bb7-116">Protection container in fabric $fabric with name.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="a5bb7-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a5bb7-117">Example 3</span></span>
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

<span data-ttu-id="a5bb7-118">Protection container in fabric $fabric with friendly Name.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="a5bb7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5bb7-119">PARAMETERS</span></span>

### <span data-ttu-id="a5bb7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5bb7-120">-DefaultProfile</span></span>
<span data-ttu-id="a5bb7-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a5bb7-122">-Ткань</span><span class="sxs-lookup"><span data-stu-id="a5bb7-122">-Fabric</span></span>
<span data-ttu-id="a5bb7-123">На посмотрите, есть ли в указанном материале ASR контейнер защиты.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-123">Look for the protection container in the specified ASR fabric.</span></span>

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

### <span data-ttu-id="a5bb7-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a5bb7-124">-FriendlyName</span></span>
<span data-ttu-id="a5bb7-125">Указывает имя искомого контейнера защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="a5bb7-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a5bb7-126">-Name</span></span>
<span data-ttu-id="a5bb7-127">Имя контейнера защиты ASR, который нужно найти.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="a5bb7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5bb7-128">CommonParameters</span></span>
<span data-ttu-id="a5bb7-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5bb7-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5bb7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5bb7-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5bb7-131">INPUTS</span></span>

### <span data-ttu-id="a5bb7-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="a5bb7-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="a5bb7-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a5bb7-133">OUTPUTS</span></span>

### <span data-ttu-id="a5bb7-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a5bb7-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="a5bb7-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a5bb7-135">NOTES</span></span>

## <span data-ttu-id="a5bb7-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5bb7-136">RELATED LINKS</span></span>
