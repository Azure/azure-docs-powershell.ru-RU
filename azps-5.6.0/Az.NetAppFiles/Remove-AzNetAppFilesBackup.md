---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
ms.openlocfilehash: f2f930a3223b8955c7165cadab04d1fe82b2bc3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968339"
---
# <span data-ttu-id="98450-101">Remove-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="98450-101">Remove-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="98450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98450-102">SYNOPSIS</span></span>
<span data-ttu-id="98450-103">Удаляет резервную копию файлов Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="98450-103">Deletes an Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="98450-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="98450-104">SYNTAX</span></span>

### <span data-ttu-id="98450-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98450-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackup -ResourceGroupName <String> [-AccountName <String>] -PoolName <String>
 [-VolumeName <String>] -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98450-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98450-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -Name <String> -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98450-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98450-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98450-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98450-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -InputObject <PSNetAppFilesBackup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98450-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98450-109">DESCRIPTION</span></span>
<span data-ttu-id="98450-110">Для удаления учетной записи ANF будет удалена учетная запись **Remove-AzNetAppFilesBackup.**</span><span class="sxs-lookup"><span data-stu-id="98450-110">The **Remove-AzNetAppFilesBackup** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="98450-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="98450-111">EXAMPLES</span></span>

### <span data-ttu-id="98450-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98450-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="98450-113">Эта команда удаляет новую резервную копию ANF с именем MyBackup для тома "MyVolume".</span><span class="sxs-lookup"><span data-stu-id="98450-113">This command deletes the new ANF backup with a the name "MyBackup" for volume "MyVolume".</span></span>

## <span data-ttu-id="98450-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98450-114">PARAMETERS</span></span>

### <span data-ttu-id="98450-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="98450-115">-AccountName</span></span>
<span data-ttu-id="98450-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="98450-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="98450-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98450-117">-DefaultProfile</span></span>
<span data-ttu-id="98450-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98450-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98450-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98450-119">-InputObject</span></span>
<span data-ttu-id="98450-120">Снимок объекта, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="98450-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98450-121">-Name</span><span class="sxs-lookup"><span data-stu-id="98450-121">-Name</span></span>
<span data-ttu-id="98450-122">Имя резервной копии ANF</span><span class="sxs-lookup"><span data-stu-id="98450-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98450-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98450-123">-PassThru</span></span>
<span data-ttu-id="98450-124">Возвращает, была ли указанная резервная копия успешно удалена.</span><span class="sxs-lookup"><span data-stu-id="98450-124">Return whether the specified backup was successfully removed</span></span>

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

### <span data-ttu-id="98450-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="98450-125">-PoolName</span></span>
<span data-ttu-id="98450-126">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="98450-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="98450-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98450-127">-ResourceGroupName</span></span>
<span data-ttu-id="98450-128">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="98450-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="98450-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98450-129">-ResourceId</span></span>
<span data-ttu-id="98450-130">Код ресурса резервной копии ANF</span><span class="sxs-lookup"><span data-stu-id="98450-130">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="98450-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="98450-131">-VolumeName</span></span>
<span data-ttu-id="98450-132">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="98450-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="98450-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="98450-133">-VolumeObject</span></span>
<span data-ttu-id="98450-134">Объект тома, содержащий резервную копию, возвращаемую</span><span class="sxs-lookup"><span data-stu-id="98450-134">The volume object containing the backup to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98450-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98450-135">-Confirm</span></span>
<span data-ttu-id="98450-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98450-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98450-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98450-137">-WhatIf</span></span>
<span data-ttu-id="98450-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98450-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98450-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="98450-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98450-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98450-140">CommonParameters</span></span>
<span data-ttu-id="98450-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98450-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98450-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98450-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98450-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98450-143">INPUTS</span></span>

### <span data-ttu-id="98450-144">System.String</span><span class="sxs-lookup"><span data-stu-id="98450-144">System.String</span></span>

### <span data-ttu-id="98450-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="98450-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="98450-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="98450-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="98450-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="98450-147">OUTPUTS</span></span>

### <span data-ttu-id="98450-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="98450-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="98450-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="98450-149">NOTES</span></span>

## <span data-ttu-id="98450-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98450-150">RELATED LINKS</span></span>
