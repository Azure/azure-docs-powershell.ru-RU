---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: bd4280f87d397afdcab3f77e8305a0c1ff4b0ed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561624"
---
# <span data-ttu-id="133fa-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="133fa-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="133fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="133fa-102">SYNOPSIS</span></span>
<span data-ttu-id="133fa-103">Возвращает политики репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="133fa-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="133fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="133fa-104">SYNTAX</span></span>

### <span data-ttu-id="133fa-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="133fa-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="133fa-106">ByName</span><span class="sxs-lookup"><span data-stu-id="133fa-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="133fa-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="133fa-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="133fa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="133fa-108">DESCRIPTION</span></span>
<span data-ttu-id="133fa-109">Командлет **Get-AzureRmRecoveryServicesAsrPolicy** получает список настроенных политик репликации для Azure Site Recovery или определенную политику репликации по имени.</span><span class="sxs-lookup"><span data-stu-id="133fa-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="133fa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="133fa-110">EXAMPLES</span></span>

### <span data-ttu-id="133fa-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="133fa-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy
```

<span data-ttu-id="133fa-112">Retuns списка политик репликации</span><span class="sxs-lookup"><span data-stu-id="133fa-112">Retuns the list of replication policies</span></span>

### <span data-ttu-id="133fa-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="133fa-113">Example 2</span></span>
```
PS C:\>  Get-AzureRmRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="133fa-114">Политика репликации Retuns с именем.</span><span class="sxs-lookup"><span data-stu-id="133fa-114">Retuns replication policy with name.</span></span>

### <span data-ttu-id="133fa-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="133fa-115">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="133fa-116">Возвращает политику репликации с указанным понятным именем.</span><span class="sxs-lookup"><span data-stu-id="133fa-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="133fa-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="133fa-117">PARAMETERS</span></span>

### <span data-ttu-id="133fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="133fa-118">-DefaultProfile</span></span>
<span data-ttu-id="133fa-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="133fa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="133fa-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="133fa-120">-FriendlyName</span></span>
<span data-ttu-id="133fa-121">Указывает понятное имя политики репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="133fa-121">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="133fa-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="133fa-122">-Name</span></span>
<span data-ttu-id="133fa-123">Задает имя политики репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="133fa-123">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="133fa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="133fa-124">CommonParameters</span></span>
<span data-ttu-id="133fa-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="133fa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="133fa-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="133fa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="133fa-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="133fa-127">INPUTS</span></span>

### <span data-ttu-id="133fa-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="133fa-128">None</span></span>

## <span data-ttu-id="133fa-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="133fa-129">OUTPUTS</span></span>

### <span data-ttu-id="133fa-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="133fa-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="133fa-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="133fa-131">NOTES</span></span>

## <span data-ttu-id="133fa-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="133fa-132">RELATED LINKS</span></span>

[<span data-ttu-id="133fa-133">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="133fa-133">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="133fa-134">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="133fa-134">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
