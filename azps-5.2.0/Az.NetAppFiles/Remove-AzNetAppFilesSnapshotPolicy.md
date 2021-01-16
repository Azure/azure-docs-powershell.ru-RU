---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 6ea65189969e38359bb6d4345ea4c47963f9eddf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325923"
---
# <span data-ttu-id="0ce37-101">Remove-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="0ce37-101">Remove-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="0ce37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ce37-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce37-103">Удаляет политику моментального снимка в azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="0ce37-103">Deletes an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="0ce37-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0ce37-104">SYNTAX</span></span>

### <span data-ttu-id="0ce37-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ce37-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ce37-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ce37-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ce37-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ce37-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ce37-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ce37-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -InputObject <PSNetAppFilesSnapshotPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ce37-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ce37-109">DESCRIPTION</span></span>
<span data-ttu-id="0ce37-110">Для удаления политики моментального снимка anF будет удалена политика **Remove-AzNetAppFilesSnapshotPolicy.**</span><span class="sxs-lookup"><span data-stu-id="0ce37-110">The **Remove-AzNetAppFilesSnapshotPolicy** cmdlet deletes an ANF snapshot policy.</span></span>

## <span data-ttu-id="0ce37-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0ce37-111">EXAMPLES</span></span>

### <span data-ttu-id="0ce37-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0ce37-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="0ce37-113">Эта команда удаляет новую политику резервного копирования ANF с именем MyBackupPolicy для учетной записи MyAccount.</span><span class="sxs-lookup"><span data-stu-id="0ce37-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="0ce37-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ce37-114">PARAMETERS</span></span>

### <span data-ttu-id="0ce37-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0ce37-115">-AccountName</span></span>
<span data-ttu-id="0ce37-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="0ce37-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="0ce37-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="0ce37-117">-AccountObject</span></span>
<span data-ttu-id="0ce37-118">Учетная запись для нового объекта политики моментального снимка</span><span class="sxs-lookup"><span data-stu-id="0ce37-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="0ce37-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce37-119">-DefaultProfile</span></span>
<span data-ttu-id="0ce37-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ce37-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ce37-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ce37-121">-InputObject</span></span>
<span data-ttu-id="0ce37-122">Удаляемый объект SnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="0ce37-122">The SnapshotPolicy object to remove</span></span>

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

### <span data-ttu-id="0ce37-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0ce37-123">-Name</span></span>
<span data-ttu-id="0ce37-124">Имя политики моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="0ce37-124">The name of the ANF snapshot policy</span></span>

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

### <span data-ttu-id="0ce37-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ce37-125">-PassThru</span></span>
<span data-ttu-id="0ce37-126">Возврат, была ли указанная учетная запись успешно удалена</span><span class="sxs-lookup"><span data-stu-id="0ce37-126">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="0ce37-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ce37-127">-ResourceGroupName</span></span>
<span data-ttu-id="0ce37-128">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="0ce37-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="0ce37-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ce37-129">-ResourceId</span></span>
<span data-ttu-id="0ce37-130">ИД ресурса политики моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="0ce37-130">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="0ce37-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ce37-131">-Confirm</span></span>
<span data-ttu-id="0ce37-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ce37-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ce37-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ce37-133">-WhatIf</span></span>
<span data-ttu-id="0ce37-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ce37-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ce37-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0ce37-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ce37-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce37-136">CommonParameters</span></span>
<span data-ttu-id="0ce37-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ce37-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce37-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ce37-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce37-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ce37-139">INPUTS</span></span>

### <span data-ttu-id="0ce37-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0ce37-140">System.String</span></span>

### <span data-ttu-id="0ce37-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="0ce37-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="0ce37-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="0ce37-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="0ce37-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0ce37-143">OUTPUTS</span></span>

### <span data-ttu-id="0ce37-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="0ce37-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="0ce37-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0ce37-145">NOTES</span></span>

## <span data-ttu-id="0ce37-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ce37-146">RELATED LINKS</span></span>
