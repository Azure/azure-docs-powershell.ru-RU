---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: be76705ab9b5a07b4d5bf654c897b6e396cf85c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956771"
---
# <span data-ttu-id="9e970-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9e970-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="9e970-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e970-102">SYNOPSIS</span></span>
<span data-ttu-id="9e970-103">Получает сопоставления контейнера для защиты от восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="9e970-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

## <span data-ttu-id="9e970-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9e970-104">SYNTAX</span></span>

### <span data-ttu-id="9e970-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e970-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e970-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="9e970-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e970-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e970-107">DESCRIPTION</span></span>
<span data-ttu-id="9e970-108">Для  указанного контейнера защиты ASR в хранилище можно получить сведения о контейнере защиты для сопоставлений (сопоставлений) политики репликации в хранилище.</span><span class="sxs-lookup"><span data-stu-id="9e970-108">The **Get-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="9e970-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9e970-109">EXAMPLES</span></span>

### <span data-ttu-id="9e970-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9e970-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="9e970-111">Список сопоставлений контейнеров защиты для контейнера.</span><span class="sxs-lookup"><span data-stu-id="9e970-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="9e970-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9e970-112">Example 2</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

Name                                  : pcmmapping
ID                                    : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replica
                                        tionProtectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectionContainerMappings/pcmmapping
Health                                : Normal
HealthErrorDetails                    : {}
PolicyFriendlyName                    : V2aTestPolicy
PolicyId                              : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationPolicies/V2aTestPolicy
SourceFabricFriendlyName              : V2A-W2K12-400
SourceProtectionContainerFriendlyName : V2A-W2K12-400
State                                 : Paired
TargetFabricFriendlyName              : Microsoft Azure
TargetProtectionContainerFriendlyName : Microsoft Azure
TargetProtectionContainerId           : Microsoft Azure
```

<span data-ttu-id="9e970-113">Возвращает все сопоставления контейнера защиты для указанного контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="9e970-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="9e970-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e970-114">PARAMETERS</span></span>

### <span data-ttu-id="9e970-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e970-115">-DefaultProfile</span></span>
<span data-ttu-id="9e970-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e970-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9e970-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9e970-117">-Name</span></span>
<span data-ttu-id="9e970-118">Имя сопоставления контейнера защиты, которое нужно получить.</span><span class="sxs-lookup"><span data-stu-id="9e970-118">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="9e970-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9e970-119">-ProtectionContainer</span></span>
<span data-ttu-id="9e970-120">Получите сопоставления контейнеров защиты, соответствующие указанному объекту контейнера защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="9e970-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e970-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e970-121">CommonParameters</span></span>
<span data-ttu-id="9e970-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e970-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e970-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e970-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e970-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e970-124">INPUTS</span></span>

### <span data-ttu-id="9e970-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9e970-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="9e970-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e970-126">OUTPUTS</span></span>

### <span data-ttu-id="9e970-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9e970-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="9e970-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9e970-128">NOTES</span></span>

## <span data-ttu-id="9e970-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e970-129">RELATED LINKS</span></span>

[<span data-ttu-id="9e970-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9e970-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="9e970-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9e970-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
