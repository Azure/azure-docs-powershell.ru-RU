---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 8c07b375214ef78f281bdfab2b31a94e0504b30e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968243"
---
# <span data-ttu-id="011b2-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="011b2-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="011b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="011b2-102">SYNOPSIS</span></span>
<span data-ttu-id="011b2-103">Восстановление или восстановление громкости одним из моментальных снимков</span><span class="sxs-lookup"><span data-stu-id="011b2-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="011b2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="011b2-104">SYNTAX</span></span>

### <span data-ttu-id="011b2-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="011b2-105">ByFieldsParameterSet (Default)</span></span>
```
Restore-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="011b2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="011b2-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="011b2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="011b2-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="011b2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="011b2-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="011b2-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="011b2-109">DESCRIPTION</span></span>
<span data-ttu-id="011b2-110">Восстановление или восстановление громкости для моментального снимка, указанного в параметре SnapshotId</span><span class="sxs-lookup"><span data-stu-id="011b2-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="011b2-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="011b2-111">EXAMPLES</span></span>

### <span data-ttu-id="011b2-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="011b2-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="011b2-113">Эта команда восстанавливает/возвращает громкость MyVolume к одному из моментальных снимков со снимкомId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="011b2-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="011b2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="011b2-114">PARAMETERS</span></span>

### <span data-ttu-id="011b2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="011b2-115">-AccountName</span></span>
<span data-ttu-id="011b2-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="011b2-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="011b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="011b2-117">-DefaultProfile</span></span>
<span data-ttu-id="011b2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="011b2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="011b2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="011b2-119">-InputObject</span></span>
<span data-ttu-id="011b2-120">Удаляемый объект громкости</span><span class="sxs-lookup"><span data-stu-id="011b2-120">The volume object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="011b2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="011b2-121">-Name</span></span>
<span data-ttu-id="011b2-122">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="011b2-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="011b2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="011b2-123">-PassThru</span></span>
<span data-ttu-id="011b2-124">Возвращает, была ли указанная громкость успешно восстановлена или восстановлена.</span><span class="sxs-lookup"><span data-stu-id="011b2-124">Return whether the specified volume was successfully restored/reverted</span></span>

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

### <span data-ttu-id="011b2-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="011b2-125">-PoolName</span></span>
<span data-ttu-id="011b2-126">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="011b2-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="011b2-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="011b2-127">-PoolObject</span></span>
<span data-ttu-id="011b2-128">Объект пула, содержащий удаляемую громкость</span><span class="sxs-lookup"><span data-stu-id="011b2-128">The pool object containing the volume to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="011b2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="011b2-129">-ResourceGroupName</span></span>
<span data-ttu-id="011b2-130">Группа ресурсов для тома ANF</span><span class="sxs-lookup"><span data-stu-id="011b2-130">The resource group of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="011b2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="011b2-131">-ResourceId</span></span>
<span data-ttu-id="011b2-132">ИД ресурса для тома ANF</span><span class="sxs-lookup"><span data-stu-id="011b2-132">The resource id of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="011b2-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="011b2-133">-SnapshotId</span></span>
<span data-ttu-id="011b2-134">SnapshotId моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="011b2-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="011b2-135">UUID версия 4, используемая для определения моментального снимка</span><span class="sxs-lookup"><span data-stu-id="011b2-135">UUID v4 used to identify the Snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="011b2-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="011b2-136">-Confirm</span></span>
<span data-ttu-id="011b2-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="011b2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="011b2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="011b2-138">-WhatIf</span></span>
<span data-ttu-id="011b2-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="011b2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="011b2-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="011b2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="011b2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="011b2-141">CommonParameters</span></span>
<span data-ttu-id="011b2-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="011b2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="011b2-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="011b2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="011b2-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="011b2-144">INPUTS</span></span>

### <span data-ttu-id="011b2-145">System.String</span><span class="sxs-lookup"><span data-stu-id="011b2-145">System.String</span></span>

### <span data-ttu-id="011b2-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="011b2-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="011b2-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="011b2-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="011b2-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="011b2-148">OUTPUTS</span></span>

### <span data-ttu-id="011b2-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="011b2-149">System.Boolean</span></span>

## <span data-ttu-id="011b2-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="011b2-150">NOTES</span></span>

## <span data-ttu-id="011b2-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="011b2-151">RELATED LINKS</span></span>
