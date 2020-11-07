---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 87d89766468008548db70c757ee173cd141dc946
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904990"
---
# <span data-ttu-id="36371-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="36371-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="36371-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36371-102">SYNOPSIS</span></span>
<span data-ttu-id="36371-103">Возвращает политики репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="36371-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="36371-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36371-104">SYNTAX</span></span>

### <span data-ttu-id="36371-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36371-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36371-106">ByName</span><span class="sxs-lookup"><span data-stu-id="36371-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36371-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="36371-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36371-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36371-108">DESCRIPTION</span></span>
<span data-ttu-id="36371-109">Командлет **Get-AzRecoveryServicesAsrPolicy** получает список настроенных политик репликации для Azure Site Recovery или определенную политику репликации по имени.</span><span class="sxs-lookup"><span data-stu-id="36371-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="36371-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36371-110">EXAMPLES</span></span>

### <span data-ttu-id="36371-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="36371-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="36371-112">Возвращает список политик репликации.</span><span class="sxs-lookup"><span data-stu-id="36371-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="36371-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="36371-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="36371-114">Возвращает политику репликации с именем.</span><span class="sxs-lookup"><span data-stu-id="36371-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="36371-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="36371-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="36371-116">Возвращает политику репликации с указанным понятным именем.</span><span class="sxs-lookup"><span data-stu-id="36371-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="36371-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36371-117">PARAMETERS</span></span>

### <span data-ttu-id="36371-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36371-118">-DefaultProfile</span></span>
<span data-ttu-id="36371-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36371-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="36371-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="36371-120">-FriendlyName</span></span>
<span data-ttu-id="36371-121">Указывает понятное имя политики репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="36371-121">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36371-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="36371-122">-Name</span></span>
<span data-ttu-id="36371-123">Задает имя политики репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="36371-123">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36371-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36371-124">CommonParameters</span></span>
<span data-ttu-id="36371-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36371-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36371-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36371-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36371-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36371-127">INPUTS</span></span>

### <span data-ttu-id="36371-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="36371-128">None</span></span>

## <span data-ttu-id="36371-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36371-129">OUTPUTS</span></span>

### <span data-ttu-id="36371-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="36371-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="36371-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="36371-131">NOTES</span></span>

## <span data-ttu-id="36371-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36371-132">RELATED LINKS</span></span>

[<span data-ttu-id="36371-133">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="36371-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="36371-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="36371-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
