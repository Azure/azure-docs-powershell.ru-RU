---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 9c336602aebdb82e4860ee744fb99f3a6fbf5a98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558875"
---
# <span data-ttu-id="8738f-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="8738f-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="8738f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8738f-102">SYNOPSIS</span></span>
<span data-ttu-id="8738f-103">Запуск повторной синхронизации репликации.</span><span class="sxs-lookup"><span data-stu-id="8738f-103">Starts replication resynchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8738f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8738f-104">SYNTAX</span></span>

### <span data-ttu-id="8738f-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8738f-105">Default (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8738f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8738f-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8738f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8738f-107">DESCRIPTION</span></span>
<span data-ttu-id="8738f-108">Командлет **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** запускает повторную синхронизацию репликации для указанного защищенного элемента, если он находится в состоянии "требуется повторная синхронизация".</span><span class="sxs-lookup"><span data-stu-id="8738f-108">The **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="8738f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8738f-109">EXAMPLES</span></span>

### <span data-ttu-id="8738f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8738f-110">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="8738f-111">Запускает задание для повторной синхронизации репликации при успешном элементе, защищенном репликацией.</span><span class="sxs-lookup"><span data-stu-id="8738f-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="8738f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8738f-112">PARAMETERS</span></span>

### <span data-ttu-id="8738f-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8738f-113">-Confirm</span></span>
<span data-ttu-id="8738f-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8738f-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8738f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8738f-115">-DefaultProfile</span></span>
<span data-ttu-id="8738f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8738f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8738f-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8738f-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8738f-118">Защищенный элемент репликации ASR для повторной синхронизации репликации.</span><span class="sxs-lookup"><span data-stu-id="8738f-118">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8738f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8738f-119">-ResourceId</span></span>
<span data-ttu-id="8738f-120">Идентификатор ресурса защищенного элемента репликации для повторной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8738f-120">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8738f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8738f-121">-WhatIf</span></span>
<span data-ttu-id="8738f-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8738f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8738f-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8738f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8738f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8738f-124">CommonParameters</span></span>
<span data-ttu-id="8738f-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8738f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8738f-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8738f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8738f-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8738f-127">INPUTS</span></span>

### <span data-ttu-id="8738f-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8738f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8738f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8738f-129">OUTPUTS</span></span>

### <span data-ttu-id="8738f-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8738f-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8738f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="8738f-131">NOTES</span></span>

## <span data-ttu-id="8738f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8738f-132">RELATED LINKS</span></span>
