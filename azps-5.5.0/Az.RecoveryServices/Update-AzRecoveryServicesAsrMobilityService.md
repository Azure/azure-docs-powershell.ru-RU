---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 3374ba9cbc1db05b80da6b0b6dd5c5d89212ad51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217932"
---
# <span data-ttu-id="1f5ec-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="1f5ec-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="1f5ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="1f5ec-103">Push-агент мобильного обслуживания обновляет защищенные компьютеры.</span><span class="sxs-lookup"><span data-stu-id="1f5ec-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="1f5ec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1f5ec-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f5ec-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f5ec-105">DESCRIPTION</span></span>
<span data-ttu-id="1f5ec-106">Чтобы обновить данные агента мобильной службы на защищенных компьютерах( если доступно обновление), с его можно ознакомиться с cmdlet **Update-AzRecoveryServicesAsrMobilityService.**</span><span class="sxs-lookup"><span data-stu-id="1f5ec-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="1f5ec-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1f5ec-107">EXAMPLES</span></span>

### <span data-ttu-id="1f5ec-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1f5ec-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="1f5ec-109">Задание для отслеживания агента мобильной копии, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="1f5ec-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="1f5ec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f5ec-110">PARAMETERS</span></span>

### <span data-ttu-id="1f5ec-111">-Account</span><span class="sxs-lookup"><span data-stu-id="1f5ec-111">-Account</span></span>
<span data-ttu-id="1f5ec-112">Запуск в качестве ИД учетной записи, который будет использоваться для push-обновления.</span><span class="sxs-lookup"><span data-stu-id="1f5ec-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="1f5ec-113">Должен быть один из списков запуска в качестве учетных записей в материале ASR, который соответствует обновляемой машине.</span><span class="sxs-lookup"><span data-stu-id="1f5ec-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

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

### <span data-ttu-id="1f5ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f5ec-114">-DefaultProfile</span></span>
<span data-ttu-id="1f5ec-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f5ec-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f5ec-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1f5ec-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1f5ec-117">Элемент, защищенный репликацией сайтов Azure, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="1f5ec-117">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="1f5ec-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f5ec-118">-Confirm</span></span>
<span data-ttu-id="1f5ec-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f5ec-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f5ec-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f5ec-120">-WhatIf</span></span>
<span data-ttu-id="1f5ec-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f5ec-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f5ec-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1f5ec-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f5ec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f5ec-123">CommonParameters</span></span>
<span data-ttu-id="1f5ec-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f5ec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f5ec-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f5ec-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f5ec-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f5ec-126">INPUTS</span></span>

### <span data-ttu-id="1f5ec-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1f5ec-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1f5ec-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1f5ec-128">OUTPUTS</span></span>

### <span data-ttu-id="1f5ec-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="1f5ec-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1f5ec-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1f5ec-130">NOTES</span></span>

## <span data-ttu-id="1f5ec-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f5ec-131">RELATED LINKS</span></span>
