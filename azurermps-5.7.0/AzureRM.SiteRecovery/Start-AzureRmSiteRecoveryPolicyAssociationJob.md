---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3DDC8DD8-889C-4C76-B32E-3D2C2AD0AC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverypolicyassociationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
ms.openlocfilehash: 140bec7738d107574db5d0d157cc3f8cfac46583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733953"
---
# <span data-ttu-id="526b2-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span><span class="sxs-lookup"><span data-stu-id="526b2-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span></span>

## <span data-ttu-id="526b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="526b2-102">SYNOPSIS</span></span>
<span data-ttu-id="526b2-103">Запускает задание сопоставления политики репликации восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="526b2-103">Starts a Site Recovery replication policy association job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="526b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="526b2-104">SYNTAX</span></span>

### <span data-ttu-id="526b2-105">EnterpriseToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="526b2-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="526b2-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="526b2-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="526b2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="526b2-107">DESCRIPTION</span></span>
<span data-ttu-id="526b2-108">Командлет **Start-AzureRmSiteRecoveryPolicyAssociationJob** инициирует задание связи для связывания политики репликации с контейнером защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="526b2-108">The **Start-AzureRmSiteRecoveryPolicyAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="526b2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="526b2-109">EXAMPLES</span></span>

## <span data-ttu-id="526b2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="526b2-110">PARAMETERS</span></span>

### <span data-ttu-id="526b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="526b2-111">-DefaultProfile</span></span>
<span data-ttu-id="526b2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="526b2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="526b2-113">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="526b2-113">-Policy</span></span>
<span data-ttu-id="526b2-114">Указывает объект политики восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="526b2-114">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="526b2-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="526b2-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="526b2-116">Задает основной контейнер защиты, для которого нужно применить параметры профиля защиты.</span><span class="sxs-lookup"><span data-stu-id="526b2-116">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="526b2-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="526b2-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="526b2-118">Указывает контейнер защиты восстановления, для которого применяются параметры профиля защиты.</span><span class="sxs-lookup"><span data-stu-id="526b2-118">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="526b2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="526b2-119">CommonParameters</span></span>
<span data-ttu-id="526b2-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="526b2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="526b2-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="526b2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="526b2-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="526b2-122">INPUTS</span></span>

### <span data-ttu-id="526b2-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="526b2-123">ASRPolicy</span></span>
<span data-ttu-id="526b2-124">Параметр "Policy" принимает значение типа "ASRPolicy" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="526b2-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="526b2-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="526b2-125">OUTPUTS</span></span>

### <span data-ttu-id="526b2-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="526b2-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="526b2-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="526b2-127">NOTES</span></span>

## <span data-ttu-id="526b2-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="526b2-128">RELATED LINKS</span></span>

