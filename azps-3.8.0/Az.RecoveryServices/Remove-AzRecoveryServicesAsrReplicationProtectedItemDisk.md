---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: a5ac137692c8945ba58e848ccca530bd4bc99ed2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072635"
---
# <span data-ttu-id="bbf21-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="bbf21-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="bbf21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bbf21-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf21-103">Удаляет диски из элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="bbf21-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="bbf21-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bbf21-104">SYNTAX</span></span>

### <span data-ttu-id="bbf21-105">AzureToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bbf21-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbf21-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="bbf21-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bbf21-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbf21-107">DESCRIPTION</span></span>
<span data-ttu-id="bbf21-108">Командлет **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** удаляет диск из защищенного элемента репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="bbf21-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="bbf21-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bbf21-109">EXAMPLES</span></span>

### <span data-ttu-id="bbf21-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bbf21-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="bbf21-111">Начните операцию, чтобы удалить указанный диск из виртуальной машины защиты для неуправляемого диска.</span><span class="sxs-lookup"><span data-stu-id="bbf21-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="bbf21-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bbf21-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="bbf21-113">Начните операцию, чтобы удалить указанный диск из виртуальной машины для защиты на управляемом диске.</span><span class="sxs-lookup"><span data-stu-id="bbf21-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="bbf21-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bbf21-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="bbf21-115">Запускает операцию для удаления указанного диска и возвращает задание ASR, используемое для отслеживания операции удаления защищенного диска.</span><span class="sxs-lookup"><span data-stu-id="bbf21-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="bbf21-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bbf21-116">PARAMETERS</span></span>

### <span data-ttu-id="bbf21-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbf21-117">-Confirm</span></span>
<span data-ttu-id="bbf21-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bbf21-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbf21-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf21-119">-DefaultProfile</span></span>
<span data-ttu-id="bbf21-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf21-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbf21-121">-DiskId</span><span class="sxs-lookup"><span data-stu-id="bbf21-121">-DiskId</span></span>
<span data-ttu-id="bbf21-122">Указывает список управляемых идентификаторов дисков.</span><span class="sxs-lookup"><span data-stu-id="bbf21-122">Specifies the list of managed disk Ids.</span></span>

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

### <span data-ttu-id="bbf21-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbf21-123">-InputObject</span></span>
<span data-ttu-id="bbf21-124">Входной объект командлета: объект элемента, защищенного репликацией ASR, соответствующий диску, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="bbf21-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

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

### <span data-ttu-id="bbf21-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="bbf21-125">-VhdUri</span></span>
<span data-ttu-id="bbf21-126">Указывает список URI-кодов VHD.</span><span class="sxs-lookup"><span data-stu-id="bbf21-126">Specifies the list of vhd Uri's.</span></span>

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

### <span data-ttu-id="bbf21-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="bbf21-127">-WaitForCompletion</span></span>
<span data-ttu-id="bbf21-128">Ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="bbf21-128">Wait For Completion</span></span>

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

### <span data-ttu-id="bbf21-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbf21-129">-WhatIf</span></span>
<span data-ttu-id="bbf21-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bbf21-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbf21-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bbf21-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbf21-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf21-132">CommonParameters</span></span>
<span data-ttu-id="bbf21-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bbf21-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf21-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbf21-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf21-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bbf21-135">INPUTS</span></span>

### <span data-ttu-id="bbf21-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bbf21-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="bbf21-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbf21-137">OUTPUTS</span></span>

### <span data-ttu-id="bbf21-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bbf21-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bbf21-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="bbf21-139">NOTES</span></span>

## <span data-ttu-id="bbf21-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbf21-140">RELATED LINKS</span></span>
