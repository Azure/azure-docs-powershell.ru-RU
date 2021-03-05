---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 06bdb5246cc0830ef78baa81d418f1fe6e51e935
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968291"
---
# <span data-ttu-id="cf9d3-101">Remove-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="cf9d3-101">Remove-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="cf9d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="cf9d3-103">Удаляет политику моментального снимка в azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="cf9d3-103">Deletes an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="cf9d3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cf9d3-104">SYNTAX</span></span>

### <span data-ttu-id="cf9d3-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf9d3-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf9d3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf9d3-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf9d3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf9d3-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf9d3-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf9d3-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -InputObject <PSNetAppFilesSnapshotPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf9d3-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf9d3-109">DESCRIPTION</span></span>
<span data-ttu-id="cf9d3-110">Для удаления политики моментального снимка anF будет удалена политика **Remove-AzNetAppFilesSnapshotPolicy.**</span><span class="sxs-lookup"><span data-stu-id="cf9d3-110">The **Remove-AzNetAppFilesSnapshotPolicy** cmdlet deletes an ANF snapshot policy.</span></span>

## <span data-ttu-id="cf9d3-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cf9d3-111">EXAMPLES</span></span>

### <span data-ttu-id="cf9d3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cf9d3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="cf9d3-113">Эта команда удаляет новую политику резервного копирования ANF с именем MyBackupPolicy для учетной записи MyAccount.</span><span class="sxs-lookup"><span data-stu-id="cf9d3-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="cf9d3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf9d3-114">PARAMETERS</span></span>

### <span data-ttu-id="cf9d3-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cf9d3-115">-AccountName</span></span>
<span data-ttu-id="cf9d3-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="cf9d3-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="cf9d3-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="cf9d3-117">-AccountObject</span></span>
<span data-ttu-id="cf9d3-118">Учетная запись для нового объекта политики моментального снимка</span><span class="sxs-lookup"><span data-stu-id="cf9d3-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="cf9d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf9d3-119">-DefaultProfile</span></span>
<span data-ttu-id="cf9d3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf9d3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf9d3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf9d3-121">-InputObject</span></span>
<span data-ttu-id="cf9d3-122">Удаляемый объект SnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="cf9d3-122">The SnapshotPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf9d3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cf9d3-123">-Name</span></span>
<span data-ttu-id="cf9d3-124">Имя политики моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="cf9d3-124">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf9d3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf9d3-125">-PassThru</span></span>
<span data-ttu-id="cf9d3-126">Возврат, была ли указанная учетная запись успешно удалена</span><span class="sxs-lookup"><span data-stu-id="cf9d3-126">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="cf9d3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf9d3-127">-ResourceGroupName</span></span>
<span data-ttu-id="cf9d3-128">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="cf9d3-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="cf9d3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf9d3-129">-ResourceId</span></span>
<span data-ttu-id="cf9d3-130">ИД ресурса политики моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="cf9d3-130">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="cf9d3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf9d3-131">-Confirm</span></span>
<span data-ttu-id="cf9d3-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cf9d3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf9d3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf9d3-133">-WhatIf</span></span>
<span data-ttu-id="cf9d3-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf9d3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf9d3-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cf9d3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf9d3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf9d3-136">CommonParameters</span></span>
<span data-ttu-id="cf9d3-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf9d3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf9d3-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf9d3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf9d3-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf9d3-139">INPUTS</span></span>

### <span data-ttu-id="cf9d3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="cf9d3-140">System.String</span></span>

### <span data-ttu-id="cf9d3-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="cf9d3-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="cf9d3-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="cf9d3-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="cf9d3-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cf9d3-143">OUTPUTS</span></span>

### <span data-ttu-id="cf9d3-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="cf9d3-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="cf9d3-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cf9d3-145">NOTES</span></span>

## <span data-ttu-id="cf9d3-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf9d3-146">RELATED LINKS</span></span>
