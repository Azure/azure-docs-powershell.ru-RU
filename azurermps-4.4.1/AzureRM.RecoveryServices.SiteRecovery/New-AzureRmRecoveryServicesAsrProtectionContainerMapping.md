---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: aa2cd93d21ba22405fff0f3c5fcf336d00f2f6b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562279"
---
# <span data-ttu-id="450a5-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="450a5-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="450a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="450a5-102">SYNOPSIS</span></span>
<span data-ttu-id="450a5-103">Создание сопоставления контейнера защиты для Azure Site Recovery путем сопоставления указанной политики репликации с указанным контейнером защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="450a5-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="450a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="450a5-104">SYNTAX</span></span>

### <span data-ttu-id="450a5-105">EnterpriseToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="450a5-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="450a5-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="450a5-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="450a5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="450a5-107">DESCRIPTION</span></span>
<span data-ttu-id="450a5-108">Командлет **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** создает сопоставление с помощью заданной политики репликации с заданным контейнером защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="450a5-108">The **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="450a5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="450a5-109">EXAMPLES</span></span>

### <span data-ttu-id="450a5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="450a5-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="450a5-111">Запускает создание сопоставления контейнера защиты с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="450a5-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="450a5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="450a5-112">PARAMETERS</span></span>

### <span data-ttu-id="450a5-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="450a5-113">-Name</span></span>
<span data-ttu-id="450a5-114">Указывает имя сопоставления контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="450a5-114">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="450a5-115">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="450a5-115">-Policy</span></span>
<span data-ttu-id="450a5-116">Указывает объект политики репликации ASR для политики репликации, используемой в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="450a5-116">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

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

### <span data-ttu-id="450a5-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="450a5-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="450a5-118">Указывает объект контейнера защиты ASR для основного контейнера защиты, который будет использоваться в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="450a5-118">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

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

### <span data-ttu-id="450a5-119">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="450a5-119">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="450a5-120">Указывает объект контейнера защиты ASR для контейнера защиты восстановления, который будет использоваться в сопоставлении (используется при репликации в расположение для восстановления, которое не является Azure).</span><span class="sxs-lookup"><span data-stu-id="450a5-120">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

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

### <span data-ttu-id="450a5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="450a5-121">-Confirm</span></span>
<span data-ttu-id="450a5-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="450a5-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="450a5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="450a5-123">-WhatIf</span></span>
<span data-ttu-id="450a5-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="450a5-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="450a5-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="450a5-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="450a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450a5-126">CommonParameters</span></span>
<span data-ttu-id="450a5-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="450a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450a5-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="450a5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450a5-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="450a5-129">INPUTS</span></span>

### <span data-ttu-id="450a5-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="450a5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="450a5-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="450a5-131">OUTPUTS</span></span>

### <span data-ttu-id="450a5-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="450a5-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="450a5-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="450a5-133">NOTES</span></span>

## <span data-ttu-id="450a5-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="450a5-134">RELATED LINKS</span></span>

[<span data-ttu-id="450a5-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="450a5-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="450a5-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="450a5-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
