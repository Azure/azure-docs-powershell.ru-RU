---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 7d3b5735cc52ae190cc16c93ad9806a9f47b452d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065083"
---
# <span data-ttu-id="8b50b-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8b50b-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="8b50b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b50b-102">SYNOPSIS</span></span>
<span data-ttu-id="8b50b-103">Получение сопоставлений контейнеров для восстановления сайта Azure site Protection.</span><span class="sxs-lookup"><span data-stu-id="8b50b-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

## <span data-ttu-id="8b50b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b50b-104">SYNTAX</span></span>

### <span data-ttu-id="8b50b-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b50b-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b50b-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="8b50b-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b50b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b50b-107">DESCRIPTION</span></span>
<span data-ttu-id="8b50b-108">Командлет **Get-AzRecoveryServicesAsrProtectionContainerMapping** получает сведения о контейнере защиты для сопоставлений политик репликации (Ассоциация) в хранилище для указанного контейнера защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="8b50b-108">The **Get-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="8b50b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b50b-109">EXAMPLES</span></span>

### <span data-ttu-id="8b50b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b50b-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="8b50b-111">Список сопоставлений контейнеров защиты для контейнера.</span><span class="sxs-lookup"><span data-stu-id="8b50b-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="8b50b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8b50b-112">Example 2</span></span>
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

<span data-ttu-id="8b50b-113">Получает все сопоставления контейнеров защиты для указанного контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="8b50b-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="8b50b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b50b-114">PARAMETERS</span></span>

### <span data-ttu-id="8b50b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b50b-115">-DefaultProfile</span></span>
<span data-ttu-id="8b50b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b50b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8b50b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8b50b-117">-Name</span></span>
<span data-ttu-id="8b50b-118">Указывает имя сопоставления контейнера защиты, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="8b50b-118">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="8b50b-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8b50b-119">-ProtectionContainer</span></span>
<span data-ttu-id="8b50b-120">Получение сопоставлений контейнеров защиты, соответствующих указанному объекту контейнера защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="8b50b-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

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

### <span data-ttu-id="8b50b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b50b-121">CommonParameters</span></span>
<span data-ttu-id="8b50b-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b50b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b50b-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b50b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b50b-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b50b-124">INPUTS</span></span>

### <span data-ttu-id="8b50b-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8b50b-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="8b50b-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b50b-126">OUTPUTS</span></span>

### <span data-ttu-id="8b50b-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8b50b-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="8b50b-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b50b-128">NOTES</span></span>

## <span data-ttu-id="8b50b-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b50b-129">RELATED LINKS</span></span>

[<span data-ttu-id="8b50b-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8b50b-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="8b50b-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8b50b-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
