---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: c871d8620e8c4507ec972f3888babfd259ede172
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074693"
---
# <span data-ttu-id="acbe5-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="acbe5-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="acbe5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="acbe5-102">SYNOPSIS</span></span>
<span data-ttu-id="acbe5-103">Создание сопоставления контейнера защиты для Azure Site Recovery путем сопоставления указанной политики репликации с указанным контейнером защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="acbe5-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

## <span data-ttu-id="acbe5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="acbe5-104">SYNTAX</span></span>

### <span data-ttu-id="acbe5-105">EnterpriseToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="acbe5-105">EnterpriseToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acbe5-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="acbe5-106">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acbe5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acbe5-107">DESCRIPTION</span></span>
<span data-ttu-id="acbe5-108">Командлет **New-AzRecoveryServicesAsrProtectionContainerMapping** создает сопоставление с помощью заданной политики репликации с заданным контейнером защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="acbe5-108">The **New-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="acbe5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="acbe5-109">EXAMPLES</span></span>

### <span data-ttu-id="acbe5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="acbe5-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

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

<span data-ttu-id="acbe5-111">Запускает создание сопоставления контейнера защиты с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="acbe5-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="acbe5-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="acbe5-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

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

<span data-ttu-id="acbe5-113">Запускает создание сопоставления контейнера защиты с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="acbe5-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="acbe5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="acbe5-114">PARAMETERS</span></span>

### <span data-ttu-id="acbe5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acbe5-115">-DefaultProfile</span></span>
<span data-ttu-id="acbe5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="acbe5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="acbe5-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="acbe5-117">-Name</span></span>
<span data-ttu-id="acbe5-118">Указывает имя сопоставления контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="acbe5-118">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="acbe5-119">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="acbe5-119">-Policy</span></span>
<span data-ttu-id="acbe5-120">Указывает объект политики репликации ASR для политики репликации, используемой в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="acbe5-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

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

### <span data-ttu-id="acbe5-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="acbe5-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="acbe5-122">Указывает объект контейнера защиты ASR для основного контейнера защиты, который будет использоваться в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="acbe5-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

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

### <span data-ttu-id="acbe5-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="acbe5-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="acbe5-124">Указывает объект контейнера защиты ASR для контейнера защиты восстановления, который будет использоваться в сопоставлении (используется при репликации в расположение для восстановления, которое не является Azure).</span><span class="sxs-lookup"><span data-stu-id="acbe5-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

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

### <span data-ttu-id="acbe5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acbe5-125">-Confirm</span></span>
<span data-ttu-id="acbe5-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="acbe5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acbe5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acbe5-127">-WhatIf</span></span>
<span data-ttu-id="acbe5-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="acbe5-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="acbe5-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="acbe5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acbe5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acbe5-130">CommonParameters</span></span>
<span data-ttu-id="acbe5-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="acbe5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acbe5-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="acbe5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acbe5-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="acbe5-133">INPUTS</span></span>

### <span data-ttu-id="acbe5-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="acbe5-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="acbe5-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="acbe5-135">OUTPUTS</span></span>

### <span data-ttu-id="acbe5-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="acbe5-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="acbe5-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="acbe5-137">NOTES</span></span>

## <span data-ttu-id="acbe5-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acbe5-138">RELATED LINKS</span></span>

[<span data-ttu-id="acbe5-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="acbe5-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="acbe5-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="acbe5-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
