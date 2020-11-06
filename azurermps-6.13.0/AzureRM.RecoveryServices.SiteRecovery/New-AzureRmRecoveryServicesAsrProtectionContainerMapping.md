---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 35e338d5e6fd9dccbee1a099bc4dabf234cd8e70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556544"
---
# <span data-ttu-id="f5adc-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f5adc-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="f5adc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5adc-102">SYNOPSIS</span></span>
<span data-ttu-id="f5adc-103">Создание сопоставления контейнера защиты для Azure Site Recovery путем сопоставления указанной политики репликации с указанным контейнером защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="f5adc-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5adc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5adc-104">SYNTAX</span></span>

### <span data-ttu-id="f5adc-105">EnterpriseToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f5adc-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5adc-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="f5adc-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5adc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5adc-107">DESCRIPTION</span></span>
<span data-ttu-id="f5adc-108">Командлет **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** создает сопоставление с помощью заданной политики репликации с заданным контейнером защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f5adc-108">The **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="f5adc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5adc-109">EXAMPLES</span></span>

### <span data-ttu-id="f5adc-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f5adc-110">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="f5adc-111">Запускает создание сопоставления контейнера защиты с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="f5adc-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f5adc-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f5adc-112">Example 2</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="f5adc-113">Запускает создание сопоставления контейнера защиты с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="f5adc-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f5adc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5adc-114">PARAMETERS</span></span>

### <span data-ttu-id="f5adc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5adc-115">-DefaultProfile</span></span>
<span data-ttu-id="f5adc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5adc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f5adc-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f5adc-117">-Name</span></span>
<span data-ttu-id="f5adc-118">Указывает имя сопоставления контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="f5adc-118">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="f5adc-119">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="f5adc-119">-Policy</span></span>
<span data-ttu-id="f5adc-120">Указывает объект политики репликации ASR для политики репликации, используемой в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="f5adc-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5adc-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f5adc-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="f5adc-122">Указывает объект контейнера защиты ASR для основного контейнера защиты, который будет использоваться в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="f5adc-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5adc-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f5adc-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="f5adc-124">Указывает объект контейнера защиты ASR для контейнера защиты восстановления, который будет использоваться в сопоставлении (используется при репликации в расположение для восстановления, которое не является Azure).</span><span class="sxs-lookup"><span data-stu-id="f5adc-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5adc-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5adc-125">-Confirm</span></span>
<span data-ttu-id="f5adc-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f5adc-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5adc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5adc-127">-WhatIf</span></span>
<span data-ttu-id="f5adc-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f5adc-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5adc-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f5adc-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5adc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5adc-130">CommonParameters</span></span>
<span data-ttu-id="f5adc-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5adc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5adc-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5adc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5adc-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5adc-133">INPUTS</span></span>

### <span data-ttu-id="f5adc-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="f5adc-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="f5adc-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5adc-135">OUTPUTS</span></span>

### <span data-ttu-id="f5adc-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f5adc-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f5adc-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5adc-137">NOTES</span></span>

## <span data-ttu-id="f5adc-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5adc-138">RELATED LINKS</span></span>

[<span data-ttu-id="f5adc-139">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f5adc-139">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="f5adc-140">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f5adc-140">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
