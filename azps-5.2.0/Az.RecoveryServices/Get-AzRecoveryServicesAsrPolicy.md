---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a7cd359714be965c232019310ac2f2abfe0fe233
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396855"
---
# <span data-ttu-id="b5af3-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="b5af3-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="b5af3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5af3-102">SYNOPSIS</span></span>
<span data-ttu-id="b5af3-103">Получает политики репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="b5af3-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="b5af3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b5af3-104">SYNTAX</span></span>

### <span data-ttu-id="b5af3-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5af3-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5af3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b5af3-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5af3-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b5af3-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5af3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5af3-108">DESCRIPTION</span></span>
<span data-ttu-id="b5af3-109">С **помощью cmdlet Get-AzRecoveryServicesAsrPolicy** можно получить список настроенных политик репликации для восстановления сайтов Azure или конкретной политики репликации по имени.</span><span class="sxs-lookup"><span data-stu-id="b5af3-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="b5af3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b5af3-110">EXAMPLES</span></span>

### <span data-ttu-id="b5af3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b5af3-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="b5af3-112">Возвращает список политик репликации.</span><span class="sxs-lookup"><span data-stu-id="b5af3-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="b5af3-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b5af3-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="b5af3-114">Возвращает политику репликации с именем.</span><span class="sxs-lookup"><span data-stu-id="b5af3-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="b5af3-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b5af3-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="b5af3-116">Возвращает политику репликации с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="b5af3-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="b5af3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5af3-117">PARAMETERS</span></span>

### <span data-ttu-id="b5af3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5af3-118">-DefaultProfile</span></span>
<span data-ttu-id="b5af3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5af3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b5af3-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b5af3-120">-FriendlyName</span></span>
<span data-ttu-id="b5af3-121">Указывает удобное имя политики репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="b5af3-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="b5af3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b5af3-122">-Name</span></span>
<span data-ttu-id="b5af3-123">Указывает имя политики репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="b5af3-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="b5af3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5af3-124">CommonParameters</span></span>
<span data-ttu-id="b5af3-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5af3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5af3-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5af3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5af3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5af3-127">INPUTS</span></span>

### <span data-ttu-id="b5af3-128">Нет</span><span class="sxs-lookup"><span data-stu-id="b5af3-128">None</span></span>

## <span data-ttu-id="b5af3-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b5af3-129">OUTPUTS</span></span>

### <span data-ttu-id="b5af3-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="b5af3-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="b5af3-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b5af3-131">NOTES</span></span>

## <span data-ttu-id="b5af3-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5af3-132">RELATED LINKS</span></span>

[<span data-ttu-id="b5af3-133">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="b5af3-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="b5af3-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="b5af3-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
