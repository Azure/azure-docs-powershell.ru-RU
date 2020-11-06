---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4F71DC85-B2E0-4E0B-96F6-69D52C577B22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
ms.openlocfilehash: 7dc64ea2bdbfb5dcbc648143dd094313eb765782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562068"
---
# <span data-ttu-id="e6b71-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span><span class="sxs-lookup"><span data-stu-id="e6b71-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span></span>

## <span data-ttu-id="e6b71-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6b71-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b71-103">Запускает задание относительной связи в политике репликации, связанной с контейнером защиты для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="e6b71-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6b71-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6b71-104">SYNTAX</span></span>

### <span data-ttu-id="e6b71-105">EnterpriseToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6b71-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6b71-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="e6b71-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6b71-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6b71-107">DESCRIPTION</span></span>
<span data-ttu-id="e6b71-108">Командлет **Start-AzureRmSiteRecoveryPolicyDissociationJob** инициирует задание на отсвязь в политике репликации, связанной с контейнером защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e6b71-108">The **Start-AzureRmSiteRecoveryPolicyDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="e6b71-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6b71-109">EXAMPLES</span></span>

## <span data-ttu-id="e6b71-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6b71-110">PARAMETERS</span></span>

### <span data-ttu-id="e6b71-111">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="e6b71-111">-Policy</span></span>
<span data-ttu-id="e6b71-112">Указывает объект политики восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="e6b71-112">Specifies an Azure Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b71-113">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e6b71-113">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="e6b71-114">Задает основной контейнер защиты.</span><span class="sxs-lookup"><span data-stu-id="e6b71-114">Specifies a primary protection container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b71-115">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e6b71-115">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="e6b71-116">Указывает контейнер защиты восстановления.</span><span class="sxs-lookup"><span data-stu-id="e6b71-116">Specifies a recovery protection container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b71-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b71-117">-DefaultProfile</span></span>
<span data-ttu-id="e6b71-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6b71-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b71-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b71-119">CommonParameters</span></span>
<span data-ttu-id="e6b71-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6b71-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b71-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6b71-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b71-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6b71-122">INPUTS</span></span>

### <span data-ttu-id="e6b71-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="e6b71-123">ASRPolicy</span></span>
<span data-ttu-id="e6b71-124">Параметр "Policy" принимает значение типа "ASRPolicy" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e6b71-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="e6b71-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6b71-125">OUTPUTS</span></span>

### <span data-ttu-id="e6b71-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e6b71-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e6b71-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6b71-127">NOTES</span></span>

## <span data-ttu-id="e6b71-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6b71-128">RELATED LINKS</span></span>

