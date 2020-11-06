---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4F71DC85-B2E0-4E0B-96F6-69D52C577B22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverypolicydissociationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
ms.openlocfilehash: eb12462b85c4a12416f41f899ebc9b2c46cca465
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567394"
---
# <span data-ttu-id="a7638-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span><span class="sxs-lookup"><span data-stu-id="a7638-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span></span>

## <span data-ttu-id="a7638-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7638-102">SYNOPSIS</span></span>
<span data-ttu-id="a7638-103">Запускает задание относительной связи в политике репликации, связанной с контейнером защиты для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="a7638-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7638-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7638-104">SYNTAX</span></span>

### <span data-ttu-id="a7638-105">EnterpriseToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7638-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7638-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="a7638-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7638-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7638-107">DESCRIPTION</span></span>
<span data-ttu-id="a7638-108">Командлет **Start-AzureRmSiteRecoveryPolicyDissociationJob** инициирует задание на отсвязь в политике репликации, связанной с контейнером защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a7638-108">The **Start-AzureRmSiteRecoveryPolicyDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="a7638-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7638-109">EXAMPLES</span></span>

## <span data-ttu-id="a7638-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7638-110">PARAMETERS</span></span>

### <span data-ttu-id="a7638-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7638-111">-DefaultProfile</span></span>
<span data-ttu-id="a7638-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7638-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7638-113">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="a7638-113">-Policy</span></span>
<span data-ttu-id="a7638-114">Указывает объект политики восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="a7638-114">Specifies an Azure Site Recovery policy object.</span></span>

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

### <span data-ttu-id="a7638-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a7638-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="a7638-116">Задает основной контейнер защиты.</span><span class="sxs-lookup"><span data-stu-id="a7638-116">Specifies a primary protection container.</span></span>

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

### <span data-ttu-id="a7638-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a7638-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="a7638-118">Указывает контейнер защиты восстановления.</span><span class="sxs-lookup"><span data-stu-id="a7638-118">Specifies a recovery protection container.</span></span>

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

### <span data-ttu-id="a7638-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7638-119">CommonParameters</span></span>
<span data-ttu-id="a7638-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7638-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7638-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7638-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7638-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7638-122">INPUTS</span></span>

### <span data-ttu-id="a7638-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="a7638-123">ASRPolicy</span></span>
<span data-ttu-id="a7638-124">Параметр "Policy" принимает значение типа "ASRPolicy" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a7638-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="a7638-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7638-125">OUTPUTS</span></span>

### <span data-ttu-id="a7638-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a7638-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a7638-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7638-127">NOTES</span></span>

## <span data-ttu-id="a7638-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7638-128">RELATED LINKS</span></span>

