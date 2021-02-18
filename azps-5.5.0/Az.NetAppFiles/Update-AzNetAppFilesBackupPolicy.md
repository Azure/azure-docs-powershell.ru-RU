---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 0cebe34948984e36c9ad2fbe30de8da3a0e0ca92
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241133"
---
# <span data-ttu-id="9acc8-101">Update-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9acc8-101">Update-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="9acc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9acc8-102">SYNOPSIS</span></span>
<span data-ttu-id="9acc8-103">Обновляет политику резервного копирования файлов Azure NetApp Files (ANF) с помощью необязательных модификаторов.</span><span class="sxs-lookup"><span data-stu-id="9acc8-103">Updates an Azure NetApp Files (ANF) backup policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="9acc8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9acc8-104">SYNTAX</span></span>

### <span data-ttu-id="9acc8-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9acc8-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>]
 [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9acc8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9acc8-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9acc8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9acc8-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9acc8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9acc8-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesBackupPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9acc8-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9acc8-109">DESCRIPTION</span></span>
<span data-ttu-id="9acc8-110">Для **обновления-AzNetAppFilesBackupPolicy** будет модименовна политика резервного копирования ANF.</span><span class="sxs-lookup"><span data-stu-id="9acc8-110">The **Update-AzNetAppFilesBackupPolicy** cmdlet modifies an ANF backup policy .</span></span>

## <span data-ttu-id="9acc8-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9acc8-111">EXAMPLES</span></span>

### <span data-ttu-id="9acc8-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9acc8-112">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy" -DailyBackupsToKeep 2
```

<span data-ttu-id="9acc8-113">Эта команда изменяет политику резервного копирования ANF "MyBackupPolicy" на заданный DailyBackupsToKeep.</span><span class="sxs-lookup"><span data-stu-id="9acc8-113">This command changes the ANF backup policy "MyBackupPolicy" to have the given DailyBackupsToKeep.</span></span>

## <span data-ttu-id="9acc8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9acc8-114">PARAMETERS</span></span>

### <span data-ttu-id="9acc8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9acc8-115">-AccountName</span></span>
<span data-ttu-id="9acc8-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="9acc8-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="9acc8-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="9acc8-117">-AccountObject</span></span>
<span data-ttu-id="9acc8-118">Объект Account, содержащий политику резервного копирования для обновления</span><span class="sxs-lookup"><span data-stu-id="9acc8-118">The Account object containing the Backup Policy to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9acc8-119">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="9acc8-119">-DailyBackupsToKeep</span></span>
<span data-ttu-id="9acc8-120">Ежедневное количество резервных копий для сохраняемой информации</span><span class="sxs-lookup"><span data-stu-id="9acc8-120">Daily backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9acc8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9acc8-121">-DefaultProfile</span></span>
<span data-ttu-id="9acc8-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9acc8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9acc8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9acc8-123">-InputObject</span></span>
<span data-ttu-id="9acc8-124">Объект BackupPolicy, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="9acc8-124">The BackupPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9acc8-125">-Location</span><span class="sxs-lookup"><span data-stu-id="9acc8-125">-Location</span></span>
<span data-ttu-id="9acc8-126">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="9acc8-126">The location of the resource</span></span>

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

### <span data-ttu-id="9acc8-127">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="9acc8-127">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="9acc8-128">Количество ежемесячных резервных копий для сохраняемого</span><span class="sxs-lookup"><span data-stu-id="9acc8-128">Monthly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9acc8-129">-Name</span><span class="sxs-lookup"><span data-stu-id="9acc8-129">-Name</span></span>
<span data-ttu-id="9acc8-130">Имя политики резервного копирования ANF</span><span class="sxs-lookup"><span data-stu-id="9acc8-130">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="9acc8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9acc8-131">-ResourceGroupName</span></span>
<span data-ttu-id="9acc8-132">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="9acc8-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="9acc8-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9acc8-133">-ResourceId</span></span>
<span data-ttu-id="9acc8-134">Код ресурса политики резервного копирования ANF</span><span class="sxs-lookup"><span data-stu-id="9acc8-134">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="9acc8-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="9acc8-135">-Tag</span></span>
<span data-ttu-id="9acc8-136">A hashtable array which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="9acc8-136">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="9acc8-137">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="9acc8-137">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="9acc8-138">Количество резервных копий за неделю, количество сохраняемой информации</span><span class="sxs-lookup"><span data-stu-id="9acc8-138">Weekly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9acc8-139">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="9acc8-139">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="9acc8-140">Количество резервных копий за год, необходимое для сохраняемой архивации</span><span class="sxs-lookup"><span data-stu-id="9acc8-140">Yearly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9acc8-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9acc8-141">-Confirm</span></span>
<span data-ttu-id="9acc8-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9acc8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9acc8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9acc8-143">-WhatIf</span></span>
<span data-ttu-id="9acc8-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9acc8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9acc8-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9acc8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9acc8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9acc8-146">CommonParameters</span></span>
<span data-ttu-id="9acc8-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9acc8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9acc8-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9acc8-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9acc8-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9acc8-149">INPUTS</span></span>

### <span data-ttu-id="9acc8-150">System.String</span><span class="sxs-lookup"><span data-stu-id="9acc8-150">System.String</span></span>

### <span data-ttu-id="9acc8-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="9acc8-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="9acc8-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9acc8-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="9acc8-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9acc8-153">OUTPUTS</span></span>

### <span data-ttu-id="9acc8-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9acc8-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="9acc8-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9acc8-155">NOTES</span></span>

## <span data-ttu-id="9acc8-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9acc8-156">RELATED LINKS</span></span>
