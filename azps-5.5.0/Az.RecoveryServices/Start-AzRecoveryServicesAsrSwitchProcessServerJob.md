---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: d5f65479fb52eb52b91b82d7af2318576825eada
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226900"
---
# <span data-ttu-id="f1ce6-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="f1ce6-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="f1ce6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="f1ce6-103">Переключение репликации с одного сервера процессов на другой для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f1ce6-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="f1ce6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f1ce6-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1ce6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1ce6-105">DESCRIPTION</span></span>
<span data-ttu-id="f1ce6-106">**Start-AzRecoveryServicesAsrSwserviceProcessServerJob** переключает перемещение данных репликации для указанных виртуальных машин или указанного сервера процесса на указанный сервер целевого процесса.</span><span class="sxs-lookup"><span data-stu-id="f1ce6-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="f1ce6-107">Используется для балансировки нагрузки или переключения репликации между серверами process.</span><span class="sxs-lookup"><span data-stu-id="f1ce6-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="f1ce6-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f1ce6-108">EXAMPLES</span></span>

### <span data-ttu-id="f1ce6-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f1ce6-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="f1ce6-110">Задание для отслеживания сервера переключения для всех элементов, защищенных репликацией, с сервера исходных на целевой.</span><span class="sxs-lookup"><span data-stu-id="f1ce6-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="f1ce6-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f1ce6-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="f1ce6-112">Задание для отслеживания сервера переключения для защищенного элемента с репликацией из источника в целевой сервер процесса.</span><span class="sxs-lookup"><span data-stu-id="f1ce6-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="f1ce6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1ce6-113">PARAMETERS</span></span>

### <span data-ttu-id="f1ce6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1ce6-114">-DefaultProfile</span></span>
<span data-ttu-id="f1ce6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1ce6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1ce6-116">-Ткань</span><span class="sxs-lookup"><span data-stu-id="f1ce6-116">-Fabric</span></span>
<span data-ttu-id="f1ce6-117">Ткань восстановления сайта, соответствующая серверу Configuration Server.</span><span class="sxs-lookup"><span data-stu-id="f1ce6-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

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

### <span data-ttu-id="f1ce6-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f1ce6-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f1ce6-119">Список защищенных репликацией элементов, сервер процессов которых нужно переключить.</span><span class="sxs-lookup"><span data-stu-id="f1ce6-119">List of replication protected item whose process server to be switched.</span></span>

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

### <span data-ttu-id="f1ce6-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="f1ce6-120">-SourceProcessServer</span></span>
<span data-ttu-id="f1ce6-121">Сервер процесса, с который нужно переключиться репликации.</span><span class="sxs-lookup"><span data-stu-id="f1ce6-121">The Process server to switch replication out from.</span></span>

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

### <span data-ttu-id="f1ce6-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="f1ce6-122">-TargetProcessServer</span></span>
<span data-ttu-id="f1ce6-123">Сервер процесса, на который нужно переключиться репликация.</span><span class="sxs-lookup"><span data-stu-id="f1ce6-123">The Process server to switch replication to.</span></span>

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

### <span data-ttu-id="f1ce6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1ce6-124">-Confirm</span></span>
<span data-ttu-id="f1ce6-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f1ce6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1ce6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1ce6-126">-WhatIf</span></span>
<span data-ttu-id="f1ce6-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1ce6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1ce6-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f1ce6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1ce6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1ce6-129">CommonParameters</span></span>
<span data-ttu-id="f1ce6-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1ce6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1ce6-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1ce6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1ce6-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1ce6-132">INPUTS</span></span>

### <span data-ttu-id="f1ce6-133">Нет</span><span class="sxs-lookup"><span data-stu-id="f1ce6-133">None</span></span>

## <span data-ttu-id="f1ce6-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f1ce6-134">OUTPUTS</span></span>

### <span data-ttu-id="f1ce6-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="f1ce6-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f1ce6-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f1ce6-136">NOTES</span></span>

## <span data-ttu-id="f1ce6-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1ce6-137">RELATED LINKS</span></span>
