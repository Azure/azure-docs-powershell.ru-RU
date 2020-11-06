---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 11CE6244-D287-4B99-9585-E3EA2D36A4F9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 44addca6ee4f658f4cc6f8081e0f7a0c39ba4a58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567049"
---
# <span data-ttu-id="4f4a5-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4f4a5-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="4f4a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f4a5-102">SYNOPSIS</span></span>
<span data-ttu-id="4f4a5-103">Создание сопоставления контейнера защиты для Azure Site Recovery путем связывания политики с контейнером защиты.</span><span class="sxs-lookup"><span data-stu-id="4f4a5-103">Creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f4a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f4a5-104">SYNTAX</span></span>

### <span data-ttu-id="4f4a5-105">EnterpriseToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4f4a5-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f4a5-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="4f4a5-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f4a5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f4a5-107">DESCRIPTION</span></span>
<span data-ttu-id="4f4a5-108">Командлет **New-AzureRmSiteRecoveryProtectionContainerMapping** создает сопоставление для контейнера защиты Azure Site Recovery, связывая политику с контейнером защиты.</span><span class="sxs-lookup"><span data-stu-id="4f4a5-108">The **New-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

## <span data-ttu-id="4f4a5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f4a5-109">EXAMPLES</span></span>

## <span data-ttu-id="4f4a5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f4a5-110">PARAMETERS</span></span>

### <span data-ttu-id="4f4a5-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4f4a5-111">-Name</span></span>
<span data-ttu-id="4f4a5-112">Указывает имя сопоставления контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="4f4a5-112">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4a5-113">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="4f4a5-113">-Policy</span></span>
<span data-ttu-id="4f4a5-114">Указывает объект политики восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="4f4a5-114">Specifies the Azure Site Recovery Policy object.</span></span>

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

### <span data-ttu-id="4f4a5-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4f4a5-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="4f4a5-116">Задает основной объект контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="4f4a5-116">Specifies the primary Protection Container object.</span></span>

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

### <span data-ttu-id="4f4a5-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4f4a5-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="4f4a5-118">Указывает объект контейнера защиты восстановления.</span><span class="sxs-lookup"><span data-stu-id="4f4a5-118">Specifies the Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="4f4a5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f4a5-119">-DefaultProfile</span></span>
<span data-ttu-id="4f4a5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f4a5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f4a5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f4a5-121">CommonParameters</span></span>
<span data-ttu-id="4f4a5-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f4a5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f4a5-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f4a5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f4a5-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f4a5-124">INPUTS</span></span>

### <span data-ttu-id="4f4a5-125">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="4f4a5-125">ASRPolicy</span></span>
<span data-ttu-id="4f4a5-126">Параметр "Policy" принимает значение типа "ASRPolicy" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4f4a5-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="4f4a5-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f4a5-127">OUTPUTS</span></span>

### <span data-ttu-id="4f4a5-128">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4f4a5-128">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4f4a5-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f4a5-129">NOTES</span></span>

## <span data-ttu-id="4f4a5-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f4a5-130">RELATED LINKS</span></span>

[<span data-ttu-id="4f4a5-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4f4a5-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="4f4a5-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4f4a5-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
