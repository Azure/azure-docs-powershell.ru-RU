---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: bee3d9ff2f3e13397afba0cc85ecbb148aedc0cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953155"
---
# <span data-ttu-id="a3c3e-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="a3c3e-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="a3c3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="a3c3e-103">Удаляет диски для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="a3c3e-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="a3c3e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a3c3e-104">SYNTAX</span></span>

### <span data-ttu-id="a3c3e-105">AzureToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a3c3e-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3c3e-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a3c3e-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3c3e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3c3e-107">DESCRIPTION</span></span>
<span data-ttu-id="a3c3e-108">Для удаления диска из элемента, защищенного репликацией ASR, удаляется диск из элемента **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.**</span><span class="sxs-lookup"><span data-stu-id="a3c3e-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="a3c3e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a3c3e-109">EXAMPLES</span></span>

### <span data-ttu-id="a3c3e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a3c3e-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="a3c3e-111">Начните операцию по удалению указанного диска из VM-системы защиты неудаченного диска.</span><span class="sxs-lookup"><span data-stu-id="a3c3e-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="a3c3e-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a3c3e-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="a3c3e-113">Запустите операцию по удалению указанного диска из VM-системы защиты для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="a3c3e-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="a3c3e-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a3c3e-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="a3c3e-115">Начало операции удаления указанного диска и возврат задания asR, используемого для отслеживания операции удаления защищенного диска.</span><span class="sxs-lookup"><span data-stu-id="a3c3e-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="a3c3e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3c3e-116">PARAMETERS</span></span>

### <span data-ttu-id="a3c3e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3c3e-117">-Confirm</span></span>
<span data-ttu-id="a3c3e-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a3c3e-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c3e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3c3e-119">-DefaultProfile</span></span>
<span data-ttu-id="a3c3e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3c3e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c3e-121">-DiskId</span><span class="sxs-lookup"><span data-stu-id="a3c3e-121">-DiskId</span></span>
<span data-ttu-id="a3c3e-122">Определяет список управляемых ид дисков.</span><span class="sxs-lookup"><span data-stu-id="a3c3e-122">Specifies the list of managed disk Ids.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c3e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3c3e-123">-InputObject</span></span>
<span data-ttu-id="a3c3e-124">Объект ввода для cmdlet: объект, защищенный репликацией ASR, для которого требуется удалить диск.</span><span class="sxs-lookup"><span data-stu-id="a3c3e-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3c3e-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="a3c3e-125">-VhdUri</span></span>
<span data-ttu-id="a3c3e-126">Определяет список URI vhd.</span><span class="sxs-lookup"><span data-stu-id="a3c3e-126">Specifies the list of vhd Uri's.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c3e-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="a3c3e-127">-WaitForCompletion</span></span>
<span data-ttu-id="a3c3e-128">Ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="a3c3e-128">Wait For Completion</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c3e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3c3e-129">-WhatIf</span></span>
<span data-ttu-id="a3c3e-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3c3e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3c3e-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a3c3e-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c3e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3c3e-132">CommonParameters</span></span>
<span data-ttu-id="a3c3e-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3c3e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3c3e-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3c3e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3c3e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3c3e-135">INPUTS</span></span>

### <span data-ttu-id="a3c3e-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a3c3e-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a3c3e-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a3c3e-137">OUTPUTS</span></span>

### <span data-ttu-id="a3c3e-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="a3c3e-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a3c3e-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a3c3e-139">NOTES</span></span>

## <span data-ttu-id="a3c3e-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3c3e-140">RELATED LINKS</span></span>
