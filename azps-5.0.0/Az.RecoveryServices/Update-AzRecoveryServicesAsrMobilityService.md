---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 3374ba9cbc1db05b80da6b0b6dd5c5d89212ad51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246842"
---
# <span data-ttu-id="b4b0c-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="b4b0c-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="b4b0c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b0c-103">Отправка обновлений агента службы Mobility Service на защищенные компьютеры.</span><span class="sxs-lookup"><span data-stu-id="b4b0c-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="b4b0c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4b0c-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4b0c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4b0c-105">DESCRIPTION</span></span>
<span data-ttu-id="b4b0c-106">Командлет **Update-AzRecoveryServicesAsrMobilityService** пытается отправить обновления агента службы Mobility Service на защищенные компьютеры (если доступно обновление).</span><span class="sxs-lookup"><span data-stu-id="b4b0c-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="b4b0c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4b0c-107">EXAMPLES</span></span>

### <span data-ttu-id="b4b0c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4b0c-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="b4b0c-109">Задание для отслеживания агента обслуживания служб Mobility Service, защищенного с репликацией обновлений.</span><span class="sxs-lookup"><span data-stu-id="b4b0c-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="b4b0c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4b0c-110">PARAMETERS</span></span>

### <span data-ttu-id="b4b0c-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b4b0c-111">-Account</span></span>
<span data-ttu-id="b4b0c-112">Идентификатор учетной записи запуска от имени, который будет использоваться для отправки обновления.</span><span class="sxs-lookup"><span data-stu-id="b4b0c-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="b4b0c-113">Должен быть один из списка учетных записей запуска от имени в структуре ASR, соответствующей обновляемому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="b4b0c-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4b0c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b0c-114">-DefaultProfile</span></span>
<span data-ttu-id="b4b0c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b0c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4b0c-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b4b0c-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b4b0c-117">Защищенный элемент репликации Azure Site Recovery, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="b4b0c-117">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="b4b0c-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4b0c-118">-Confirm</span></span>
<span data-ttu-id="b4b0c-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b4b0c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4b0c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4b0c-120">-WhatIf</span></span>
<span data-ttu-id="b4b0c-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b4b0c-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4b0c-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b4b0c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4b0c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b0c-123">CommonParameters</span></span>
<span data-ttu-id="b4b0c-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4b0c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b0c-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4b0c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b0c-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4b0c-126">INPUTS</span></span>

### <span data-ttu-id="b4b0c-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b4b0c-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="b4b0c-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4b0c-128">OUTPUTS</span></span>

### <span data-ttu-id="b4b0c-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b4b0c-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b4b0c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4b0c-130">NOTES</span></span>

## <span data-ttu-id="b4b0c-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4b0c-131">RELATED LINKS</span></span>
