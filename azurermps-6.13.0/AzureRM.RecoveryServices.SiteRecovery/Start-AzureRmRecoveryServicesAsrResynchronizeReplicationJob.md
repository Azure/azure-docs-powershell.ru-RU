---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 6ee25231b7bb8861a1294537e2f42a0bf914b994
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732100"
---
# <span data-ttu-id="66e3f-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="66e3f-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="66e3f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="66e3f-103">Запуск повторной синхронизации репликации.</span><span class="sxs-lookup"><span data-stu-id="66e3f-103">Starts replication resynchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66e3f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66e3f-104">SYNTAX</span></span>

### <span data-ttu-id="66e3f-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="66e3f-105">Default (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66e3f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="66e3f-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66e3f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66e3f-107">DESCRIPTION</span></span>
<span data-ttu-id="66e3f-108">Командлет **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** запускает повторную синхронизацию репликации для указанного защищенного элемента, если он находится в состоянии "требуется повторная синхронизация".</span><span class="sxs-lookup"><span data-stu-id="66e3f-108">The **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="66e3f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66e3f-109">EXAMPLES</span></span>

### <span data-ttu-id="66e3f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="66e3f-110">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="66e3f-111">Запускает задание для повторной синхронизации репликации при успешном элементе, защищенном репликацией.</span><span class="sxs-lookup"><span data-stu-id="66e3f-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="66e3f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66e3f-112">PARAMETERS</span></span>

### <span data-ttu-id="66e3f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66e3f-113">-DefaultProfile</span></span>
<span data-ttu-id="66e3f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66e3f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66e3f-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="66e3f-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="66e3f-116">Защищенный элемент репликации ASR для повторной синхронизации репликации.</span><span class="sxs-lookup"><span data-stu-id="66e3f-116">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66e3f-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66e3f-117">-ResourceId</span></span>
<span data-ttu-id="66e3f-118">Идентификатор ресурса защищенного элемента репликации для повторной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="66e3f-118">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e3f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66e3f-119">-Confirm</span></span>
<span data-ttu-id="66e3f-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="66e3f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66e3f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66e3f-121">-WhatIf</span></span>
<span data-ttu-id="66e3f-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="66e3f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66e3f-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="66e3f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66e3f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66e3f-124">CommonParameters</span></span>
<span data-ttu-id="66e3f-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66e3f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66e3f-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66e3f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66e3f-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66e3f-127">INPUTS</span></span>

### <span data-ttu-id="66e3f-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="66e3f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="66e3f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66e3f-129">OUTPUTS</span></span>

### <span data-ttu-id="66e3f-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="66e3f-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="66e3f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="66e3f-131">NOTES</span></span>

## <span data-ttu-id="66e3f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66e3f-132">RELATED LINKS</span></span>
