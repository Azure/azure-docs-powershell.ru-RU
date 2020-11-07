---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: 4f926b88214a60cc05b6eb9666e10fa8ed7bf3ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729597"
---
# <span data-ttu-id="e9321-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="e9321-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="e9321-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9321-102">SYNOPSIS</span></span>
<span data-ttu-id="e9321-103">Переключить репликацию с одного сервера обработки на другой для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e9321-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="e9321-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9321-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9321-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9321-105">DESCRIPTION</span></span>
<span data-ttu-id="e9321-106">Параметр **Start-AzRecoveryServicesAsrSwitchProcessServerJob** переключает перемещение данных репликации для указанных виртуальных машин или указанного сервера обработки на указанный целевой сервер обработки.</span><span class="sxs-lookup"><span data-stu-id="e9321-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="e9321-107">Используется для балансировки нагрузки и переключения репликации между серверами обработки.</span><span class="sxs-lookup"><span data-stu-id="e9321-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="e9321-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9321-108">EXAMPLES</span></span>

### <span data-ttu-id="e9321-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e9321-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="e9321-110">Задание, отслеживающее переключение сервера обработки для всех элементов, защищенных репликацией, из источника на целевой сервер обработки.</span><span class="sxs-lookup"><span data-stu-id="e9321-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="e9321-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e9321-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="e9321-112">Задание, отслеживающее переключение сервера обработки для элемента, защищенного из источника, на целевой сервер обработки.</span><span class="sxs-lookup"><span data-stu-id="e9321-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="e9321-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9321-113">PARAMETERS</span></span>

### <span data-ttu-id="e9321-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9321-114">-DefaultProfile</span></span>
<span data-ttu-id="e9321-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9321-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9321-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="e9321-116">-Fabric</span></span>
<span data-ttu-id="e9321-117">Структура восстановления сайта, соответствующая серверу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e9321-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9321-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e9321-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e9321-119">Список элементов, защищенных репликацией, для которых должен быть переключен сервер обработки.</span><span class="sxs-lookup"><span data-stu-id="e9321-119">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9321-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="e9321-120">-SourceProcessServer</span></span>
<span data-ttu-id="e9321-121">Сервер обработки, с которого нужно переключить репликацию.</span><span class="sxs-lookup"><span data-stu-id="e9321-121">The Process server to switch replication out from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9321-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="e9321-122">-TargetProcessServer</span></span>
<span data-ttu-id="e9321-123">Сервер обработки, на который нужно переключить репликацию.</span><span class="sxs-lookup"><span data-stu-id="e9321-123">The Process server to switch replication to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9321-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9321-124">-Confirm</span></span>
<span data-ttu-id="e9321-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e9321-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9321-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9321-126">-WhatIf</span></span>
<span data-ttu-id="e9321-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e9321-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9321-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e9321-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9321-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9321-129">CommonParameters</span></span>
<span data-ttu-id="e9321-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e9321-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9321-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9321-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9321-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9321-132">INPUTS</span></span>

### <span data-ttu-id="e9321-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="e9321-133">None</span></span>

## <span data-ttu-id="e9321-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9321-134">OUTPUTS</span></span>

### <span data-ttu-id="e9321-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e9321-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e9321-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9321-136">NOTES</span></span>

## <span data-ttu-id="e9321-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9321-137">RELATED LINKS</span></span>
