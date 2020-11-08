---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065471"
---
# <span data-ttu-id="af3fa-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="af3fa-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="af3fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af3fa-102">SYNOPSIS</span></span>
<span data-ttu-id="af3fa-103">Добавьте диск для защиты для уже защищенной виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="af3fa-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="af3fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af3fa-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af3fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af3fa-105">DESCRIPTION</span></span>
<span data-ttu-id="af3fa-106">Командлет **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** добавьте диск для защиты для уже защищенной виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="af3fa-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="af3fa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af3fa-107">EXAMPLES</span></span>

### <span data-ttu-id="af3fa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="af3fa-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="af3fa-109">Начните операцию, чтобы добавить указанную конфигурацию диска для защиты.</span><span class="sxs-lookup"><span data-stu-id="af3fa-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="af3fa-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="af3fa-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="af3fa-111">Начните операцию, чтобы добавить указанную конфигурацию диска для защиты. Элемент, защищенный входной репликацией трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="af3fa-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="af3fa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af3fa-112">PARAMETERS</span></span>

### <span data-ttu-id="af3fa-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="af3fa-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="af3fa-114">Указывает конфигурацию диска, используемую в сценарии аварийного восстановления с помощью Azure to Azure.</span><span class="sxs-lookup"><span data-stu-id="af3fa-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="af3fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af3fa-115">-DefaultProfile</span></span>
<span data-ttu-id="af3fa-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af3fa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af3fa-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af3fa-117">-InputObject</span></span>
<span data-ttu-id="af3fa-118">Входной объект для командлета: объект элемента, защищенного репликацией ASR, соответствующий необходимо защитить новый диск.</span><span class="sxs-lookup"><span data-stu-id="af3fa-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

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

### <span data-ttu-id="af3fa-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="af3fa-119">-WaitForCompletion</span></span>
<span data-ttu-id="af3fa-120">Ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="af3fa-120">Wait For Completion</span></span>

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

### <span data-ttu-id="af3fa-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af3fa-121">-Confirm</span></span>
<span data-ttu-id="af3fa-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="af3fa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af3fa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af3fa-123">-WhatIf</span></span>
<span data-ttu-id="af3fa-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="af3fa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af3fa-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="af3fa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af3fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af3fa-126">CommonParameters</span></span>
<span data-ttu-id="af3fa-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af3fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af3fa-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af3fa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af3fa-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af3fa-129">INPUTS</span></span>

### <span data-ttu-id="af3fa-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="af3fa-130">None</span></span>

## <span data-ttu-id="af3fa-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af3fa-131">OUTPUTS</span></span>

### <span data-ttu-id="af3fa-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="af3fa-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="af3fa-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="af3fa-133">NOTES</span></span>

## <span data-ttu-id="af3fa-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af3fa-134">RELATED LINKS</span></span>
