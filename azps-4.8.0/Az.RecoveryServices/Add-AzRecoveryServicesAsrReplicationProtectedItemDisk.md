---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078088"
---
# <span data-ttu-id="565cf-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="565cf-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="565cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="565cf-102">SYNOPSIS</span></span>
<span data-ttu-id="565cf-103">Добавьте диск для защиты для уже защищенной виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="565cf-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="565cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="565cf-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="565cf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="565cf-105">DESCRIPTION</span></span>
<span data-ttu-id="565cf-106">Командлет **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** добавьте диск для защиты для уже защищенной виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="565cf-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="565cf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="565cf-107">EXAMPLES</span></span>

### <span data-ttu-id="565cf-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="565cf-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="565cf-109">Начните операцию, чтобы добавить указанную конфигурацию диска для защиты.</span><span class="sxs-lookup"><span data-stu-id="565cf-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="565cf-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="565cf-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="565cf-111">Начните операцию, чтобы добавить указанную конфигурацию диска для защиты. Элемент, защищенный входной репликацией трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="565cf-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="565cf-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="565cf-112">PARAMETERS</span></span>

### <span data-ttu-id="565cf-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="565cf-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="565cf-114">Указывает конфигурацию диска, используемую в сценарии аварийного восстановления с помощью Azure to Azure.</span><span class="sxs-lookup"><span data-stu-id="565cf-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="565cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="565cf-115">-DefaultProfile</span></span>
<span data-ttu-id="565cf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="565cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="565cf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="565cf-117">-InputObject</span></span>
<span data-ttu-id="565cf-118">Входной объект для командлета: объект элемента, защищенного репликацией ASR, соответствующий необходимо защитить новый диск.</span><span class="sxs-lookup"><span data-stu-id="565cf-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

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

### <span data-ttu-id="565cf-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="565cf-119">-WaitForCompletion</span></span>
<span data-ttu-id="565cf-120">Ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="565cf-120">Wait For Completion</span></span>

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

### <span data-ttu-id="565cf-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="565cf-121">-Confirm</span></span>
<span data-ttu-id="565cf-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="565cf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="565cf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="565cf-123">-WhatIf</span></span>
<span data-ttu-id="565cf-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="565cf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="565cf-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="565cf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="565cf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="565cf-126">CommonParameters</span></span>
<span data-ttu-id="565cf-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="565cf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="565cf-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="565cf-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="565cf-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="565cf-129">INPUTS</span></span>

### <span data-ttu-id="565cf-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="565cf-130">None</span></span>

## <span data-ttu-id="565cf-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="565cf-131">OUTPUTS</span></span>

### <span data-ttu-id="565cf-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="565cf-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="565cf-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="565cf-133">NOTES</span></span>

## <span data-ttu-id="565cf-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="565cf-134">RELATED LINKS</span></span>
