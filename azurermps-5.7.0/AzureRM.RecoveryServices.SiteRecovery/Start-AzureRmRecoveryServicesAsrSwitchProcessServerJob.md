---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: be16ff2145a4442861fd985dfbb55da63f010e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558864"
---
# <span data-ttu-id="6caf6-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="6caf6-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="6caf6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6caf6-102">SYNOPSIS</span></span>
<span data-ttu-id="6caf6-103">Переключить репликацию с одного сервера обработки на другой для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6caf6-103">Switch replication from one Process server to another for load balancing.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6caf6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6caf6-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric>
 -SourceProcessServer <ASRProcessServer> -TargetProcessServer <ASRProcessServer>
 [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6caf6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6caf6-105">DESCRIPTION</span></span>
<span data-ttu-id="6caf6-106">Параметр **Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob** переключает перемещение данных репликации для указанных виртуальных машин или указанного сервера обработки на указанный целевой сервер обработки.</span><span class="sxs-lookup"><span data-stu-id="6caf6-106">The **Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="6caf6-107">Используется для балансировки нагрузки и переключения репликации между серверами обработки.</span><span class="sxs-lookup"><span data-stu-id="6caf6-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="6caf6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6caf6-108">EXAMPLES</span></span>

### <span data-ttu-id="6caf6-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6caf6-109">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="6caf6-110">Задание, отслеживающее переключение сервера обработки для всех элементов, защищенных репликацией, из источника на целевой сервер обработки.</span><span class="sxs-lookup"><span data-stu-id="6caf6-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="6caf6-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6caf6-111">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="6caf6-112">Задание, отслеживающее переключение сервера обработки для элемента, защищенного из источника, на целевой сервер обработки.</span><span class="sxs-lookup"><span data-stu-id="6caf6-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="6caf6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6caf6-113">PARAMETERS</span></span>

### <span data-ttu-id="6caf6-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6caf6-114">-Confirm</span></span>
<span data-ttu-id="6caf6-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6caf6-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6caf6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6caf6-116">-DefaultProfile</span></span>
<span data-ttu-id="6caf6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6caf6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6caf6-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="6caf6-118">-Fabric</span></span>
<span data-ttu-id="6caf6-119">Структура восстановления сайта, соответствующая серверу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6caf6-119">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6caf6-120">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6caf6-120">-ReplicationProtectedItem</span></span>
<span data-ttu-id="6caf6-121">Список элементов, защищенных репликацией, для которых должен быть переключен сервер обработки.</span><span class="sxs-lookup"><span data-stu-id="6caf6-121">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6caf6-122">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="6caf6-122">-SourceProcessServer</span></span>
<span data-ttu-id="6caf6-123">Сервер обработки, с которого нужно переключить репликацию.</span><span class="sxs-lookup"><span data-stu-id="6caf6-123">The Process server to switch replication out from.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6caf6-124">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="6caf6-124">-TargetProcessServer</span></span>
<span data-ttu-id="6caf6-125">Сервер обработки, на который нужно переключить репликацию.</span><span class="sxs-lookup"><span data-stu-id="6caf6-125">The Process server to switch replication to.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6caf6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6caf6-126">-WhatIf</span></span>
<span data-ttu-id="6caf6-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6caf6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6caf6-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6caf6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6caf6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6caf6-129">CommonParameters</span></span>
<span data-ttu-id="6caf6-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6caf6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6caf6-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6caf6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6caf6-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6caf6-132">INPUTS</span></span>

### <span data-ttu-id="6caf6-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="6caf6-133">None</span></span>

## <span data-ttu-id="6caf6-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6caf6-134">OUTPUTS</span></span>

### <span data-ttu-id="6caf6-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6caf6-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6caf6-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="6caf6-136">NOTES</span></span>

## <span data-ttu-id="6caf6-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6caf6-137">RELATED LINKS</span></span>
