---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213073"
---
# <span data-ttu-id="73394-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="73394-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="73394-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73394-102">SYNOPSIS</span></span>
<span data-ttu-id="73394-103">Добавьте диск для защиты уже защищенной виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="73394-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="73394-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="73394-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73394-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73394-105">DESCRIPTION</span></span>
<span data-ttu-id="73394-106">Для защиты уже защищенной виртуальной машины Azure добавляется диск для **add-AzRecoveryServicesAsrReplicationProtectedItemDisk.**</span><span class="sxs-lookup"><span data-stu-id="73394-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="73394-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="73394-107">EXAMPLES</span></span>

### <span data-ttu-id="73394-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="73394-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="73394-109">Начните операцию по добавлению указанной конфигурации диска для защиты.</span><span class="sxs-lookup"><span data-stu-id="73394-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="73394-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="73394-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="73394-111">Начните операцию по добавлению указанной конфигурации диска для защиты. Пункт, защищенный репликацией входных данных для piping.</span><span class="sxs-lookup"><span data-stu-id="73394-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="73394-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73394-112">PARAMETERS</span></span>

### <span data-ttu-id="73394-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="73394-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="73394-114">Определяет конфигурацию диска, используемую для защиты диска от Azure до сценария аварийного восстановления Azure.</span><span class="sxs-lookup"><span data-stu-id="73394-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="73394-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73394-115">-DefaultProfile</span></span>
<span data-ttu-id="73394-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73394-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73394-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73394-117">-InputObject</span></span>
<span data-ttu-id="73394-118">Объект ввода для cmdlet: объект, защищенный репликацией ASR, для которого требуется защитить новый диск.</span><span class="sxs-lookup"><span data-stu-id="73394-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

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

### <span data-ttu-id="73394-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="73394-119">-WaitForCompletion</span></span>
<span data-ttu-id="73394-120">Ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="73394-120">Wait For Completion</span></span>

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

### <span data-ttu-id="73394-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73394-121">-Confirm</span></span>
<span data-ttu-id="73394-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73394-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73394-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73394-123">-WhatIf</span></span>
<span data-ttu-id="73394-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73394-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73394-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="73394-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73394-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73394-126">CommonParameters</span></span>
<span data-ttu-id="73394-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73394-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73394-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73394-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73394-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73394-129">INPUTS</span></span>

### <span data-ttu-id="73394-130">Нет</span><span class="sxs-lookup"><span data-stu-id="73394-130">None</span></span>

## <span data-ttu-id="73394-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73394-131">OUTPUTS</span></span>

### <span data-ttu-id="73394-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="73394-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="73394-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="73394-133">NOTES</span></span>

## <span data-ttu-id="73394-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73394-134">RELATED LINKS</span></span>
