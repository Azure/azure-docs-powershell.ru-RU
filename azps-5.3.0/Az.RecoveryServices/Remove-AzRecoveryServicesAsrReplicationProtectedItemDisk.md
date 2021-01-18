---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: a5ac137692c8945ba58e848ccca530bd4bc99ed2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519789"
---
# <span data-ttu-id="26510-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="26510-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="26510-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26510-102">SYNOPSIS</span></span>
<span data-ttu-id="26510-103">Удаляет диски для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="26510-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="26510-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="26510-104">SYNTAX</span></span>

### <span data-ttu-id="26510-105">AzureToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26510-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26510-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="26510-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26510-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26510-107">DESCRIPTION</span></span>
<span data-ttu-id="26510-108">Для удаления диска из элемента, защищенного репликацией ASR, удаляется диск из элемента **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.**</span><span class="sxs-lookup"><span data-stu-id="26510-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="26510-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="26510-109">EXAMPLES</span></span>

### <span data-ttu-id="26510-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26510-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="26510-111">Запустите операцию по удалению указанного диска из системы защиты VM для неудаченного диска.</span><span class="sxs-lookup"><span data-stu-id="26510-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="26510-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="26510-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="26510-113">Запустите операцию по удалению указанного диска из VM-системы защиты для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="26510-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="26510-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="26510-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="26510-115">Начало операции удаления указанного диска и возврат задания asR, используемого для отслеживания операции удаления защищенного диска.</span><span class="sxs-lookup"><span data-stu-id="26510-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="26510-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26510-116">PARAMETERS</span></span>

### <span data-ttu-id="26510-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26510-117">-Confirm</span></span>
<span data-ttu-id="26510-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26510-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26510-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26510-119">-DefaultProfile</span></span>
<span data-ttu-id="26510-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26510-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26510-121">-DiskId</span><span class="sxs-lookup"><span data-stu-id="26510-121">-DiskId</span></span>
<span data-ttu-id="26510-122">Определяет список управляемых дисков.</span><span class="sxs-lookup"><span data-stu-id="26510-122">Specifies the list of managed disk Ids.</span></span>

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

### <span data-ttu-id="26510-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26510-123">-InputObject</span></span>
<span data-ttu-id="26510-124">Объект ввода для cmdlet: объект, защищенный репликацией ASR, для которого требуется удалить диск.</span><span class="sxs-lookup"><span data-stu-id="26510-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

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

### <span data-ttu-id="26510-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="26510-125">-VhdUri</span></span>
<span data-ttu-id="26510-126">Определяет список URI vhd.</span><span class="sxs-lookup"><span data-stu-id="26510-126">Specifies the list of vhd Uri's.</span></span>

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

### <span data-ttu-id="26510-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="26510-127">-WaitForCompletion</span></span>
<span data-ttu-id="26510-128">Ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="26510-128">Wait For Completion</span></span>

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

### <span data-ttu-id="26510-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26510-129">-WhatIf</span></span>
<span data-ttu-id="26510-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26510-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26510-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="26510-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26510-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26510-132">CommonParameters</span></span>
<span data-ttu-id="26510-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26510-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26510-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26510-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26510-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26510-135">INPUTS</span></span>

### <span data-ttu-id="26510-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="26510-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="26510-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="26510-137">OUTPUTS</span></span>

### <span data-ttu-id="26510-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="26510-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="26510-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="26510-139">NOTES</span></span>

## <span data-ttu-id="26510-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26510-140">RELATED LINKS</span></span>
