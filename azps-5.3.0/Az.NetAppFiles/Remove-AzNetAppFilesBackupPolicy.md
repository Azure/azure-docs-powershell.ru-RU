---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 975e451854a935034dc4ed508770f48e126807e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506557"
---
# <span data-ttu-id="8c4eb-101">Remove-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="8c4eb-101">Remove-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="8c4eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="8c4eb-103">Удаляет политику резервного копирования файлов Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="8c4eb-103">Deletes an Azure NetApp Files (ANF) backup policy.</span></span>

## <span data-ttu-id="8c4eb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8c4eb-104">SYNTAX</span></span>

### <span data-ttu-id="8c4eb-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8c4eb-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c4eb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c4eb-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c4eb-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c4eb-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c4eb-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c4eb-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -InputObject <PSNetAppFilesBackupPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c4eb-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c4eb-109">DESCRIPTION</span></span>
<span data-ttu-id="8c4eb-110">Для удаления политики резервного копирования ANF будет удалена политика **Remove-AzNetAppFilesBackupPolicy.**</span><span class="sxs-lookup"><span data-stu-id="8c4eb-110">The **Remove-AzNetAppFilesBackupPolicy** cmdlet deletes an ANF backup policy.</span></span>

## <span data-ttu-id="8c4eb-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8c4eb-111">EXAMPLES</span></span>

### <span data-ttu-id="8c4eb-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8c4eb-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="8c4eb-113">Эта команда удаляет новую политику резервного копирования ANF с именем MyBackupPolicy для учетной записи MyAccount.</span><span class="sxs-lookup"><span data-stu-id="8c4eb-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="8c4eb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c4eb-114">PARAMETERS</span></span>

### <span data-ttu-id="8c4eb-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8c4eb-115">-AccountName</span></span>
<span data-ttu-id="8c4eb-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="8c4eb-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="8c4eb-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="8c4eb-117">-AccountObject</span></span>
<span data-ttu-id="8c4eb-118">Объект Account, содержащий политику резервного копирования, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="8c4eb-118">The Account object containing the Backup Policy to remove</span></span>

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

### <span data-ttu-id="8c4eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c4eb-119">-DefaultProfile</span></span>
<span data-ttu-id="8c4eb-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c4eb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c4eb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c4eb-121">-InputObject</span></span>
<span data-ttu-id="8c4eb-122">Объект BackupPolicy, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="8c4eb-122">The BackupPolicy object to remove</span></span>

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

### <span data-ttu-id="8c4eb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8c4eb-123">-Name</span></span>
<span data-ttu-id="8c4eb-124">Имя политики резервного копирования ANF</span><span class="sxs-lookup"><span data-stu-id="8c4eb-124">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="8c4eb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c4eb-125">-PassThru</span></span>
<span data-ttu-id="8c4eb-126">Возвращает, была ли удалена указанная политика резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="8c4eb-126">Return whether the specified backup policy was successfully removed</span></span>

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

### <span data-ttu-id="8c4eb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c4eb-127">-ResourceGroupName</span></span>
<span data-ttu-id="8c4eb-128">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="8c4eb-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8c4eb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c4eb-129">-ResourceId</span></span>
<span data-ttu-id="8c4eb-130">Код ресурса политики резервного копирования ANF</span><span class="sxs-lookup"><span data-stu-id="8c4eb-130">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="8c4eb-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c4eb-131">-Confirm</span></span>
<span data-ttu-id="8c4eb-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8c4eb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c4eb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c4eb-133">-WhatIf</span></span>
<span data-ttu-id="8c4eb-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c4eb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c4eb-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8c4eb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c4eb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c4eb-136">CommonParameters</span></span>
<span data-ttu-id="8c4eb-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c4eb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c4eb-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c4eb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c4eb-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c4eb-139">INPUTS</span></span>

### <span data-ttu-id="8c4eb-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8c4eb-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="8c4eb-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8c4eb-141">System.String</span></span>

### <span data-ttu-id="8c4eb-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="8c4eb-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="8c4eb-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8c4eb-143">OUTPUTS</span></span>

### <span data-ttu-id="8c4eb-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="8c4eb-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="8c4eb-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8c4eb-145">NOTES</span></span>

## <span data-ttu-id="8c4eb-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c4eb-146">RELATED LINKS</span></span>
