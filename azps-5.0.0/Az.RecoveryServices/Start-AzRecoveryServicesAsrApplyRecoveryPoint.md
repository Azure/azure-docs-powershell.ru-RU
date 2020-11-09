---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 893298c3349d2d7ceaa998a1f147ce8dd590f101
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245699"
---
# <span data-ttu-id="99934-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="99934-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="99934-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99934-102">SYNOPSIS</span></span>
<span data-ttu-id="99934-103">Изменяет точку восстановления для отработки отказа для защищенного элемента, прежде чем приступать к переходу.</span><span class="sxs-lookup"><span data-stu-id="99934-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="99934-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99934-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99934-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99934-105">DESCRIPTION</span></span>
<span data-ttu-id="99934-106">**Start-AzRecoveryServicesAsrApplyRecoveryPoint** изменяет точку восстановления для отработки отказа для защищенного элемента, прежде чем она зафиксирует операцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="99934-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="99934-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99934-107">EXAMPLES</span></span>

### <span data-ttu-id="99934-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="99934-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="99934-109">Начинает применять указанную точку восстановления к элементу, защищенному репликацией, и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="99934-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="99934-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99934-110">PARAMETERS</span></span>

### <span data-ttu-id="99934-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="99934-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="99934-112">Задает основной файл сертификата при использовании шифрования данных.</span><span class="sxs-lookup"><span data-stu-id="99934-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="99934-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="99934-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="99934-114">Указывает вторичный файл сертификата, если используется шифрование данных.</span><span class="sxs-lookup"><span data-stu-id="99934-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="99934-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99934-115">-DefaultProfile</span></span>
<span data-ttu-id="99934-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99934-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="99934-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="99934-117">-RecoveryPoint</span></span>
<span data-ttu-id="99934-118">Указывает объект точки восстановления, соответствующий применяемой точке восстановления.</span><span class="sxs-lookup"><span data-stu-id="99934-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

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

### <span data-ttu-id="99934-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="99934-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="99934-120">Указывает объект защищенного элемента репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="99934-120">Specifies the ASR replication protected item object.</span></span>

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

### <span data-ttu-id="99934-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99934-121">-Confirm</span></span>
<span data-ttu-id="99934-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="99934-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99934-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99934-123">-WhatIf</span></span>
<span data-ttu-id="99934-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="99934-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99934-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="99934-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99934-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99934-126">CommonParameters</span></span>
<span data-ttu-id="99934-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99934-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99934-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99934-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99934-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99934-129">INPUTS</span></span>

### <span data-ttu-id="99934-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="99934-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="99934-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99934-131">OUTPUTS</span></span>

### <span data-ttu-id="99934-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="99934-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="99934-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="99934-133">NOTES</span></span>

## <span data-ttu-id="99934-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99934-134">RELATED LINKS</span></span>

[<span data-ttu-id="99934-135">Командлеты Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="99934-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)