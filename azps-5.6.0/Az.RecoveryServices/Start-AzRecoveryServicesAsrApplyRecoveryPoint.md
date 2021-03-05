---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 748278cd6096a8ab67538df77aa3b81cc54d3ace
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960243"
---
# <span data-ttu-id="1ac02-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1ac02-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="1ac02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ac02-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac02-103">Изменяет точку восстановления для сбойного над защищенным элементом перед тем, как она была зафиксирована.</span><span class="sxs-lookup"><span data-stu-id="1ac02-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="1ac02-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1ac02-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ac02-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ac02-105">DESCRIPTION</span></span>
<span data-ttu-id="1ac02-106">**Start-AzRecoveryServicesAsrApplyRecoveryPoint** изменяет точку восстановления для сбойного над защищенным элементом перед его совершением.</span><span class="sxs-lookup"><span data-stu-id="1ac02-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="1ac02-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1ac02-107">EXAMPLES</span></span>

### <span data-ttu-id="1ac02-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1ac02-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="1ac02-109">Начало применения указанной точки восстановления к элементу, защищенного репликацией, и возврат задания ASR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="1ac02-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1ac02-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ac02-110">PARAMETERS</span></span>

### <span data-ttu-id="1ac02-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1ac02-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="1ac02-112">Указывает основной файл сертификата, если используется шифрование данных.</span><span class="sxs-lookup"><span data-stu-id="1ac02-112">Specifies the primary certificate file if data encryption is being used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac02-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1ac02-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="1ac02-114">Определяет дополнительный файл сертификата, если используется шифрование данных.</span><span class="sxs-lookup"><span data-stu-id="1ac02-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac02-115">-DefaultProfile</span></span>
<span data-ttu-id="1ac02-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac02-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1ac02-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1ac02-117">-RecoveryPoint</span></span>
<span data-ttu-id="1ac02-118">Указывает объект точки восстановления, соответствующий точке восстановления, которая будет применена.</span><span class="sxs-lookup"><span data-stu-id="1ac02-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac02-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ac02-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1ac02-120">Определяет объект, защищенный репликацией asR.</span><span class="sxs-lookup"><span data-stu-id="1ac02-120">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac02-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ac02-121">-Confirm</span></span>
<span data-ttu-id="1ac02-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ac02-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ac02-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ac02-123">-WhatIf</span></span>
<span data-ttu-id="1ac02-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ac02-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ac02-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1ac02-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ac02-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac02-126">CommonParameters</span></span>
<span data-ttu-id="1ac02-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ac02-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac02-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ac02-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac02-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ac02-129">INPUTS</span></span>

### <span data-ttu-id="1ac02-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ac02-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1ac02-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1ac02-131">OUTPUTS</span></span>

### <span data-ttu-id="1ac02-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="1ac02-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1ac02-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1ac02-133">NOTES</span></span>

## <span data-ttu-id="1ac02-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ac02-134">RELATED LINKS</span></span>

[<span data-ttu-id="1ac02-135">Cmdlets для восстановления сайта Azure</span><span class="sxs-lookup"><span data-stu-id="1ac02-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)
