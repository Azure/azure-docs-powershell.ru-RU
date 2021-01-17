---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
ms.openlocfilehash: a2cab03bb88d5b642a95142030eb646b2a5abef4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394655"
---
# <span data-ttu-id="2ba01-101">Update-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="2ba01-101">Update-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="2ba01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ba01-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba01-103">Обновляет резервную копию файлов Azure NetApp Files (ANF) с помощью необязательных модификаторов.</span><span class="sxs-lookup"><span data-stu-id="2ba01-103">Updates an Azure NetApp Files (ANF) backup to the optional modifiers provided.</span></span>

## <span data-ttu-id="2ba01-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2ba01-104">SYNTAX</span></span>

### <span data-ttu-id="2ba01-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ba01-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolName <String> -VolumeName <String> [-Label <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ba01-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ba01-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup -Name <String> [-Label <String>] [-Tag <Hashtable>]
 -VolumeObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ba01-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ba01-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ba01-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ba01-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesBackup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ba01-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ba01-109">DESCRIPTION</span></span>
<span data-ttu-id="2ba01-110">Для резервной копии ANF будет обновлена **cmdlet Update-AzNetAppFilesBackup.**</span><span class="sxs-lookup"><span data-stu-id="2ba01-110">The **Update-AzNetAppFilesBackup** cmdlet modifies an ANF backup.</span></span>

## <span data-ttu-id="2ba01-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2ba01-111">EXAMPLES</span></span>

### <span data-ttu-id="2ba01-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2ba01-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName $accName1 -Name $backupPolicyObject -Label "updatedLabel"
```

<span data-ttu-id="2ba01-113">Эта команда выполняет обновление заданной резервной копии, внося изменения в имя пользователя в предоставленном резервном копировании.</span><span class="sxs-lookup"><span data-stu-id="2ba01-113">This command performs an update on the given backup modifying the username to that provided.</span></span>

## <span data-ttu-id="2ba01-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ba01-114">PARAMETERS</span></span>

### <span data-ttu-id="2ba01-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2ba01-115">-AccountName</span></span>
<span data-ttu-id="2ba01-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="2ba01-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="2ba01-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba01-117">-DefaultProfile</span></span>
<span data-ttu-id="2ba01-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba01-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ba01-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ba01-119">-InputObject</span></span>
<span data-ttu-id="2ba01-120">Снимок объекта, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="2ba01-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="2ba01-121">-Label</span><span class="sxs-lookup"><span data-stu-id="2ba01-121">-Label</span></span>
<span data-ttu-id="2ba01-122">Метка для резервного копирования</span><span class="sxs-lookup"><span data-stu-id="2ba01-122">Label for backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba01-123">-Location</span><span class="sxs-lookup"><span data-stu-id="2ba01-123">-Location</span></span>
<span data-ttu-id="2ba01-124">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="2ba01-124">The location of the resource</span></span>

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

### <span data-ttu-id="2ba01-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2ba01-125">-Name</span></span>
<span data-ttu-id="2ba01-126">Имя политики резервного копирования ANF</span><span class="sxs-lookup"><span data-stu-id="2ba01-126">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba01-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="2ba01-127">-PoolName</span></span>
<span data-ttu-id="2ba01-128">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="2ba01-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="2ba01-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ba01-129">-ResourceGroupName</span></span>
<span data-ttu-id="2ba01-130">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="2ba01-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="2ba01-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ba01-131">-ResourceId</span></span>
<span data-ttu-id="2ba01-132">Код ресурса резервной копии ANF</span><span class="sxs-lookup"><span data-stu-id="2ba01-132">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="2ba01-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="2ba01-133">-Tag</span></span>
<span data-ttu-id="2ba01-134">A hashtable which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="2ba01-134">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba01-135">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="2ba01-135">-VolumeName</span></span>
<span data-ttu-id="2ba01-136">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="2ba01-136">The name of the ANF volume</span></span>

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

### <span data-ttu-id="2ba01-137">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="2ba01-137">-VolumeObject</span></span>
<span data-ttu-id="2ba01-138">Объект громкости, содержащий резервную копию, возвращаемую</span><span class="sxs-lookup"><span data-stu-id="2ba01-138">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="2ba01-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ba01-139">-Confirm</span></span>
<span data-ttu-id="2ba01-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2ba01-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ba01-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ba01-141">-WhatIf</span></span>
<span data-ttu-id="2ba01-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ba01-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ba01-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2ba01-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ba01-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba01-144">CommonParameters</span></span>
<span data-ttu-id="2ba01-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ba01-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba01-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ba01-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba01-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ba01-147">INPUTS</span></span>

### <span data-ttu-id="2ba01-148">System.String</span><span class="sxs-lookup"><span data-stu-id="2ba01-148">System.String</span></span>

### <span data-ttu-id="2ba01-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2ba01-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="2ba01-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="2ba01-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="2ba01-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2ba01-151">OUTPUTS</span></span>

### <span data-ttu-id="2ba01-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="2ba01-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="2ba01-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2ba01-153">NOTES</span></span>

## <span data-ttu-id="2ba01-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ba01-154">RELATED LINKS</span></span>
