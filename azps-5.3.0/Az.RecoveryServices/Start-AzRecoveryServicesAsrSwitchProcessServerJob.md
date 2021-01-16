---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: d5f65479fb52eb52b91b82d7af2318576825eada
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506737"
---
# <span data-ttu-id="399ce-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="399ce-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="399ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="399ce-102">SYNOPSIS</span></span>
<span data-ttu-id="399ce-103">Переключение репликации с одного сервера процессов на другой для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="399ce-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="399ce-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="399ce-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="399ce-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="399ce-105">DESCRIPTION</span></span>
<span data-ttu-id="399ce-106">**Start-AzRecoveryServicesAsrSwserviceProcessServerJob** переключает перемещение данных репликации для указанных виртуальных машин или указанного сервера процесса на указанный сервер целевого процесса.</span><span class="sxs-lookup"><span data-stu-id="399ce-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="399ce-107">Используется для балансировки нагрузки или переключения репликации между серверами process.</span><span class="sxs-lookup"><span data-stu-id="399ce-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="399ce-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="399ce-108">EXAMPLES</span></span>

### <span data-ttu-id="399ce-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="399ce-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="399ce-110">Задание для отслеживания сервера переключения для всех элементов, защищенных репликацией, из источника в целевой сервер процесса.</span><span class="sxs-lookup"><span data-stu-id="399ce-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="399ce-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="399ce-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="399ce-112">Задание для отслеживания переключения сервера процесса для переданного элемента, защищенного репликацией, из источника в целевой сервер процесса.</span><span class="sxs-lookup"><span data-stu-id="399ce-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="399ce-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="399ce-113">PARAMETERS</span></span>

### <span data-ttu-id="399ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="399ce-114">-DefaultProfile</span></span>
<span data-ttu-id="399ce-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="399ce-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="399ce-116">-Ткань</span><span class="sxs-lookup"><span data-stu-id="399ce-116">-Fabric</span></span>
<span data-ttu-id="399ce-117">Ткань восстановления сайта, соответствующая серверу Configuration Server.</span><span class="sxs-lookup"><span data-stu-id="399ce-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

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

### <span data-ttu-id="399ce-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="399ce-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="399ce-119">Список защищенных репликацией элементов, сервер процессов которых нужно переключить.</span><span class="sxs-lookup"><span data-stu-id="399ce-119">List of replication protected item whose process server to be switched.</span></span>

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

### <span data-ttu-id="399ce-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="399ce-120">-SourceProcessServer</span></span>
<span data-ttu-id="399ce-121">Сервер процесса, с который нужно переключиться репликации.</span><span class="sxs-lookup"><span data-stu-id="399ce-121">The Process server to switch replication out from.</span></span>

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

### <span data-ttu-id="399ce-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="399ce-122">-TargetProcessServer</span></span>
<span data-ttu-id="399ce-123">Сервер процесса, на который нужно переключиться репликация.</span><span class="sxs-lookup"><span data-stu-id="399ce-123">The Process server to switch replication to.</span></span>

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

### <span data-ttu-id="399ce-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="399ce-124">-Confirm</span></span>
<span data-ttu-id="399ce-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="399ce-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="399ce-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="399ce-126">-WhatIf</span></span>
<span data-ttu-id="399ce-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="399ce-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="399ce-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="399ce-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="399ce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="399ce-129">CommonParameters</span></span>
<span data-ttu-id="399ce-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="399ce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="399ce-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="399ce-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="399ce-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="399ce-132">INPUTS</span></span>

### <span data-ttu-id="399ce-133">Нет</span><span class="sxs-lookup"><span data-stu-id="399ce-133">None</span></span>

## <span data-ttu-id="399ce-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="399ce-134">OUTPUTS</span></span>

### <span data-ttu-id="399ce-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="399ce-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="399ce-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="399ce-136">NOTES</span></span>

## <span data-ttu-id="399ce-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="399ce-137">RELATED LINKS</span></span>
