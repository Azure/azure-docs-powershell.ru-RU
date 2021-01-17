---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: ce49a011ba7e6c746c97e4b1aca6273d7d8b650d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410748"
---
# <span data-ttu-id="dd962-101">New-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="dd962-101">New-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="dd962-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd962-102">SYNOPSIS</span></span>
<span data-ttu-id="dd962-103">Создает политику резервного копирования файлов Azure NetApp Files (ANF) для учетной записи ANF.</span><span class="sxs-lookup"><span data-stu-id="dd962-103">Creates a new Azure NetApp Files (ANF) backup policy for an ANF account.</span></span>

## <span data-ttu-id="dd962-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dd962-104">SYNTAX</span></span>

### <span data-ttu-id="dd962-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd962-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd962-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd962-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackupPolicy -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>]
 [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd962-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd962-107">DESCRIPTION</span></span>
<span data-ttu-id="dd962-108">Для учетной записи ANF создается новая политика резервного копирования Для учетной записи **AzNetAppFilesActiveDirectory.**</span><span class="sxs-lookup"><span data-stu-id="dd962-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new backup policy for an ANF account.</span></span>

## <span data-ttu-id="dd962-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dd962-109">EXAMPLES</span></span>

### <span data-ttu-id="dd962-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dd962-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyBackupPolicy" -Tag @{"tag1" = "tagValue"} -Enabled -DailyBackupsToKeep 1 -WeeklyBackupsToKeep 2 -MonthlyBackupsToKeep 2 -YearlyBackupsToKeep 1
```

<span data-ttu-id="dd962-111">Эта команда создает новую политику резервного копирования ANF для учетной записи ANF с именем "MyAccount".</span><span class="sxs-lookup"><span data-stu-id="dd962-111">This command creates the new ANF backup policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="dd962-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd962-112">PARAMETERS</span></span>

### <span data-ttu-id="dd962-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dd962-113">-AccountName</span></span>
<span data-ttu-id="dd962-114">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="dd962-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="dd962-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="dd962-115">-AccountObject</span></span>
<span data-ttu-id="dd962-116">Объект Account для новой политики резервного копирования</span><span class="sxs-lookup"><span data-stu-id="dd962-116">The Account object for the new Backup Policy</span></span>

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

### <span data-ttu-id="dd962-117">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="dd962-117">-DailyBackupsToKeep</span></span>
<span data-ttu-id="dd962-118">Ежедневное количество резервных копий для сохраняемой информации</span><span class="sxs-lookup"><span data-stu-id="dd962-118">Daily backups count to keep</span></span>

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

### <span data-ttu-id="dd962-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd962-119">-DefaultProfile</span></span>
<span data-ttu-id="dd962-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd962-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd962-121">-Enabled</span><span class="sxs-lookup"><span data-stu-id="dd962-121">-Enabled</span></span>
<span data-ttu-id="dd962-122">Свойство, для решаемого политики: включено или не включено</span><span class="sxs-lookup"><span data-stu-id="dd962-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="dd962-123">-Location</span><span class="sxs-lookup"><span data-stu-id="dd962-123">-Location</span></span>
<span data-ttu-id="dd962-124">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="dd962-124">The location of the resource</span></span>

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

### <span data-ttu-id="dd962-125">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="dd962-125">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="dd962-126">Количество ежемесячных резервных копий для сохраняемого</span><span class="sxs-lookup"><span data-stu-id="dd962-126">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="dd962-127">-Name</span><span class="sxs-lookup"><span data-stu-id="dd962-127">-Name</span></span>
<span data-ttu-id="dd962-128">Имя политики резервного копирования ANF</span><span class="sxs-lookup"><span data-stu-id="dd962-128">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd962-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd962-129">-ResourceGroupName</span></span>
<span data-ttu-id="dd962-130">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="dd962-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="dd962-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="dd962-131">-Tag</span></span>
<span data-ttu-id="dd962-132">A hashtable array which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="dd962-132">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="dd962-133">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="dd962-133">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="dd962-134">Количество резервных копий за неделю, количество сохраняемой информации</span><span class="sxs-lookup"><span data-stu-id="dd962-134">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="dd962-135">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="dd962-135">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="dd962-136">Количество резервных копий за год, необходимое для сохраняемой архивации</span><span class="sxs-lookup"><span data-stu-id="dd962-136">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="dd962-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd962-137">-Confirm</span></span>
<span data-ttu-id="dd962-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd962-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd962-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd962-139">-WhatIf</span></span>
<span data-ttu-id="dd962-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd962-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd962-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dd962-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd962-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd962-142">CommonParameters</span></span>
<span data-ttu-id="dd962-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd962-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd962-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd962-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd962-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd962-145">INPUTS</span></span>

### <span data-ttu-id="dd962-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="dd962-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="dd962-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dd962-147">OUTPUTS</span></span>

### <span data-ttu-id="dd962-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="dd962-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="dd962-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dd962-149">NOTES</span></span>

## <span data-ttu-id="dd962-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd962-150">RELATED LINKS</span></span>
