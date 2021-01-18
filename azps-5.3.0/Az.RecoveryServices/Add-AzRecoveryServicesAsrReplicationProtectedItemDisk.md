---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505428"
---
# <span data-ttu-id="cc11e-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="cc11e-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="cc11e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc11e-102">SYNOPSIS</span></span>
<span data-ttu-id="cc11e-103">Добавьте диск для защиты уже защищенной виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="cc11e-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="cc11e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cc11e-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc11e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc11e-105">DESCRIPTION</span></span>
<span data-ttu-id="cc11e-106">Для защиты уже защищенной виртуальной машины Azure можно добавить диск с cmdlet **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.**</span><span class="sxs-lookup"><span data-stu-id="cc11e-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="cc11e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cc11e-107">EXAMPLES</span></span>

### <span data-ttu-id="cc11e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cc11e-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="cc11e-109">Начните операцию по добавлению указанной конфигурации диска для защиты.</span><span class="sxs-lookup"><span data-stu-id="cc11e-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="cc11e-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cc11e-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="cc11e-111">Начните операцию по добавлению указанной конфигурации диска для защиты. Пункт, защищенный репликацией входных данных в piping.</span><span class="sxs-lookup"><span data-stu-id="cc11e-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="cc11e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc11e-112">PARAMETERS</span></span>

### <span data-ttu-id="cc11e-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc11e-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="cc11e-114">Определяет конфигурацию диска, используемую для защиты диска от Azure до сценария аварийного восстановления Azure.</span><span class="sxs-lookup"><span data-stu-id="cc11e-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc11e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc11e-115">-DefaultProfile</span></span>
<span data-ttu-id="cc11e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc11e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc11e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc11e-117">-InputObject</span></span>
<span data-ttu-id="cc11e-118">Объект ввода для cmdlet: объект, защищенный репликацией ASR, для которого требуется защитить новый диск.</span><span class="sxs-lookup"><span data-stu-id="cc11e-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc11e-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="cc11e-119">-WaitForCompletion</span></span>
<span data-ttu-id="cc11e-120">Ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="cc11e-120">Wait For Completion</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc11e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc11e-121">-Confirm</span></span>
<span data-ttu-id="cc11e-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc11e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc11e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc11e-123">-WhatIf</span></span>
<span data-ttu-id="cc11e-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc11e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc11e-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cc11e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc11e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc11e-126">CommonParameters</span></span>
<span data-ttu-id="cc11e-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc11e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc11e-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc11e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc11e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc11e-129">INPUTS</span></span>

### <span data-ttu-id="cc11e-130">Нет</span><span class="sxs-lookup"><span data-stu-id="cc11e-130">None</span></span>

## <span data-ttu-id="cc11e-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc11e-131">OUTPUTS</span></span>

### <span data-ttu-id="cc11e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="cc11e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cc11e-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cc11e-133">NOTES</span></span>

## <span data-ttu-id="cc11e-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc11e-134">RELATED LINKS</span></span>
