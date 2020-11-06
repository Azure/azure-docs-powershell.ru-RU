---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 539a0471ae27adc80b67360fc47955fdb4b50bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558344"
---
# <span data-ttu-id="6b60d-101">Update-AzureRmRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="6b60d-101">Update-AzureRmRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="6b60d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b60d-102">SYNOPSIS</span></span>
<span data-ttu-id="6b60d-103">Отправка обновлений агента службы Mobility Service на защищенные компьютеры.</span><span class="sxs-lookup"><span data-stu-id="6b60d-103">Push mobility service agent updates to protected machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b60d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b60d-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b60d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b60d-105">DESCRIPTION</span></span>
<span data-ttu-id="6b60d-106">Командлет **Update-AzureRmRecoveryServicesAsrMobilityService** пытается отправить обновления агента службы Mobility Service на защищенные компьютеры (если доступно обновление).</span><span class="sxs-lookup"><span data-stu-id="6b60d-106">The **Update-AzureRmRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="6b60d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b60d-107">EXAMPLES</span></span>

### <span data-ttu-id="6b60d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6b60d-108">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="6b60d-109">Задание для отслеживания агента обслуживания Moblility Service, защищенного службой репликации обновлений.</span><span class="sxs-lookup"><span data-stu-id="6b60d-109">Job to track Update Replication Protected Item's Moblility Service Agent.</span></span>

## <span data-ttu-id="6b60d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b60d-110">PARAMETERS</span></span>

### <span data-ttu-id="6b60d-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6b60d-111">-Account</span></span>
<span data-ttu-id="6b60d-112">Идентификатор учетной записи запуска от имени, который будет использоваться для отправки обновления.</span><span class="sxs-lookup"><span data-stu-id="6b60d-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="6b60d-113">Должен быть один из списка учетных записей запуска от имени в структуре ASR, соответствующей обновляемому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="6b60d-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

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

### <span data-ttu-id="6b60d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b60d-114">-DefaultProfile</span></span>
<span data-ttu-id="6b60d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b60d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b60d-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6b60d-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="6b60d-117">Защищенный элемент репликации Azure Site Recovery, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="6b60d-117">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="6b60d-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b60d-118">-Confirm</span></span>
<span data-ttu-id="6b60d-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6b60d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b60d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b60d-120">-WhatIf</span></span>
<span data-ttu-id="6b60d-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6b60d-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b60d-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6b60d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b60d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b60d-123">CommonParameters</span></span>
<span data-ttu-id="6b60d-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b60d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b60d-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b60d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b60d-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b60d-126">INPUTS</span></span>

### <span data-ttu-id="6b60d-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6b60d-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="6b60d-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b60d-128">OUTPUTS</span></span>

### <span data-ttu-id="6b60d-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6b60d-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6b60d-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b60d-130">NOTES</span></span>

## <span data-ttu-id="6b60d-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b60d-131">RELATED LINKS</span></span>
