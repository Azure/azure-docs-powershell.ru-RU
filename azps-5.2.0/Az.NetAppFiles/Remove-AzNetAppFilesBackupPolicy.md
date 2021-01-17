---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 975e451854a935034dc4ed508770f48e126807e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410684"
---
# <span data-ttu-id="321b2-101">Remove-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="321b2-101">Remove-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="321b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="321b2-102">SYNOPSIS</span></span>
<span data-ttu-id="321b2-103">Удаляет политику резервного копирования файлов Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="321b2-103">Deletes an Azure NetApp Files (ANF) backup policy.</span></span>

## <span data-ttu-id="321b2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="321b2-104">SYNTAX</span></span>

### <span data-ttu-id="321b2-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="321b2-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="321b2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="321b2-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="321b2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="321b2-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="321b2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="321b2-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -InputObject <PSNetAppFilesBackupPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="321b2-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="321b2-109">DESCRIPTION</span></span>
<span data-ttu-id="321b2-110">Для удаления политики резервного копирования ANF будет удалена политика **Remove-AzNetAppFilesBackupPolicy.**</span><span class="sxs-lookup"><span data-stu-id="321b2-110">The **Remove-AzNetAppFilesBackupPolicy** cmdlet deletes an ANF backup policy.</span></span>

## <span data-ttu-id="321b2-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="321b2-111">EXAMPLES</span></span>

### <span data-ttu-id="321b2-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="321b2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="321b2-113">Эта команда удаляет новую политику резервного копирования ANF с именем MyBackupPolicy для учетной записи MyAccount.</span><span class="sxs-lookup"><span data-stu-id="321b2-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="321b2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="321b2-114">PARAMETERS</span></span>

### <span data-ttu-id="321b2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="321b2-115">-AccountName</span></span>
<span data-ttu-id="321b2-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="321b2-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="321b2-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="321b2-117">-AccountObject</span></span>
<span data-ttu-id="321b2-118">Объект Account, содержащий политику резервного копирования, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="321b2-118">The Account object containing the Backup Policy to remove</span></span>

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

### <span data-ttu-id="321b2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="321b2-119">-DefaultProfile</span></span>
<span data-ttu-id="321b2-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="321b2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="321b2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="321b2-121">-InputObject</span></span>
<span data-ttu-id="321b2-122">Объект BackupPolicy, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="321b2-122">The BackupPolicy object to remove</span></span>

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

### <span data-ttu-id="321b2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="321b2-123">-Name</span></span>
<span data-ttu-id="321b2-124">Имя политики резервного копирования ANF</span><span class="sxs-lookup"><span data-stu-id="321b2-124">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="321b2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="321b2-125">-PassThru</span></span>
<span data-ttu-id="321b2-126">Возвращает, была ли удалена указанная политика резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="321b2-126">Return whether the specified backup policy was successfully removed</span></span>

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

### <span data-ttu-id="321b2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="321b2-127">-ResourceGroupName</span></span>
<span data-ttu-id="321b2-128">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="321b2-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="321b2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="321b2-129">-ResourceId</span></span>
<span data-ttu-id="321b2-130">Код ресурса политики резервного копирования ANF</span><span class="sxs-lookup"><span data-stu-id="321b2-130">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="321b2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="321b2-131">-Confirm</span></span>
<span data-ttu-id="321b2-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="321b2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="321b2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="321b2-133">-WhatIf</span></span>
<span data-ttu-id="321b2-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="321b2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="321b2-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="321b2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="321b2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="321b2-136">CommonParameters</span></span>
<span data-ttu-id="321b2-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="321b2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="321b2-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="321b2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="321b2-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="321b2-139">INPUTS</span></span>

### <span data-ttu-id="321b2-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="321b2-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="321b2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="321b2-141">System.String</span></span>

### <span data-ttu-id="321b2-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="321b2-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="321b2-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="321b2-143">OUTPUTS</span></span>

### <span data-ttu-id="321b2-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="321b2-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="321b2-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="321b2-145">NOTES</span></span>

## <span data-ttu-id="321b2-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="321b2-146">RELATED LINKS</span></span>
