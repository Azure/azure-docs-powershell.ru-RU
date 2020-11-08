---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 3374ba9cbc1db05b80da6b0b6dd5c5d89212ad51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079357"
---
# <span data-ttu-id="983aa-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="983aa-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="983aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="983aa-102">SYNOPSIS</span></span>
<span data-ttu-id="983aa-103">Отправка обновлений агента службы Mobility Service на защищенные компьютеры.</span><span class="sxs-lookup"><span data-stu-id="983aa-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="983aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="983aa-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="983aa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="983aa-105">DESCRIPTION</span></span>
<span data-ttu-id="983aa-106">Командлет **Update-AzRecoveryServicesAsrMobilityService** пытается отправить обновления агента службы Mobility Service на защищенные компьютеры (если доступно обновление).</span><span class="sxs-lookup"><span data-stu-id="983aa-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="983aa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="983aa-107">EXAMPLES</span></span>

### <span data-ttu-id="983aa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="983aa-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="983aa-109">Задание для отслеживания агента обслуживания служб Mobility Service, защищенного с репликацией обновлений.</span><span class="sxs-lookup"><span data-stu-id="983aa-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="983aa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="983aa-110">PARAMETERS</span></span>

### <span data-ttu-id="983aa-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="983aa-111">-Account</span></span>
<span data-ttu-id="983aa-112">Идентификатор учетной записи запуска от имени, который будет использоваться для отправки обновления.</span><span class="sxs-lookup"><span data-stu-id="983aa-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="983aa-113">Должен быть один из списка учетных записей запуска от имени в структуре ASR, соответствующей обновляемому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="983aa-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

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

### <span data-ttu-id="983aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="983aa-114">-DefaultProfile</span></span>
<span data-ttu-id="983aa-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="983aa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="983aa-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="983aa-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="983aa-117">Защищенный элемент репликации Azure Site Recovery, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="983aa-117">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="983aa-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="983aa-118">-Confirm</span></span>
<span data-ttu-id="983aa-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="983aa-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="983aa-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="983aa-120">-WhatIf</span></span>
<span data-ttu-id="983aa-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="983aa-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="983aa-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="983aa-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="983aa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="983aa-123">CommonParameters</span></span>
<span data-ttu-id="983aa-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="983aa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="983aa-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="983aa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="983aa-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="983aa-126">INPUTS</span></span>

### <span data-ttu-id="983aa-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="983aa-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="983aa-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="983aa-128">OUTPUTS</span></span>

### <span data-ttu-id="983aa-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="983aa-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="983aa-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="983aa-130">NOTES</span></span>

## <span data-ttu-id="983aa-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="983aa-131">RELATED LINKS</span></span>
