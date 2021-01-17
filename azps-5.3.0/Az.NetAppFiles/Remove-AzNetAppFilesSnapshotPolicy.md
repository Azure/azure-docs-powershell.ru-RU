---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 6ea65189969e38359bb6d4345ea4c47963f9eddf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422551"
---
# <span data-ttu-id="8b8c1-101">Remove-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="8b8c1-101">Remove-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="8b8c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b8c1-102">SYNOPSIS</span></span>
<span data-ttu-id="8b8c1-103">Удаляет политику моментального снимка в azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="8b8c1-103">Deletes an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="8b8c1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b8c1-104">SYNTAX</span></span>

### <span data-ttu-id="8b8c1-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b8c1-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b8c1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b8c1-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b8c1-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b8c1-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b8c1-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b8c1-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -InputObject <PSNetAppFilesSnapshotPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b8c1-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b8c1-109">DESCRIPTION</span></span>
<span data-ttu-id="8b8c1-110">Для удаления политики моментального снимка anF будет удалена политика **Remove-AzNetAppFilesSnapshotPolicy.**</span><span class="sxs-lookup"><span data-stu-id="8b8c1-110">The **Remove-AzNetAppFilesSnapshotPolicy** cmdlet deletes an ANF snapshot policy.</span></span>

## <span data-ttu-id="8b8c1-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b8c1-111">EXAMPLES</span></span>

### <span data-ttu-id="8b8c1-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b8c1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="8b8c1-113">Эта команда удаляет новую политику резервного копирования ANF с именем MyBackupPolicy для учетной записи MyAccount.</span><span class="sxs-lookup"><span data-stu-id="8b8c1-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="8b8c1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b8c1-114">PARAMETERS</span></span>

### <span data-ttu-id="8b8c1-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8b8c1-115">-AccountName</span></span>
<span data-ttu-id="8b8c1-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="8b8c1-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="8b8c1-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="8b8c1-117">-AccountObject</span></span>
<span data-ttu-id="8b8c1-118">Учетная запись для нового объекта политики моментального снимка</span><span class="sxs-lookup"><span data-stu-id="8b8c1-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="8b8c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b8c1-119">-DefaultProfile</span></span>
<span data-ttu-id="8b8c1-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b8c1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b8c1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b8c1-121">-InputObject</span></span>
<span data-ttu-id="8b8c1-122">Удаляемый объект SnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="8b8c1-122">The SnapshotPolicy object to remove</span></span>

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

### <span data-ttu-id="8b8c1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8b8c1-123">-Name</span></span>
<span data-ttu-id="8b8c1-124">Имя политики моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="8b8c1-124">The name of the ANF snapshot policy</span></span>

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

### <span data-ttu-id="8b8c1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b8c1-125">-PassThru</span></span>
<span data-ttu-id="8b8c1-126">Возврат, была ли указанная учетная запись успешно удалена</span><span class="sxs-lookup"><span data-stu-id="8b8c1-126">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="8b8c1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b8c1-127">-ResourceGroupName</span></span>
<span data-ttu-id="8b8c1-128">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="8b8c1-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8b8c1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b8c1-129">-ResourceId</span></span>
<span data-ttu-id="8b8c1-130">ИД ресурса политики моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="8b8c1-130">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="8b8c1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b8c1-131">-Confirm</span></span>
<span data-ttu-id="8b8c1-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b8c1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b8c1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b8c1-133">-WhatIf</span></span>
<span data-ttu-id="8b8c1-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b8c1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b8c1-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8b8c1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b8c1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b8c1-136">CommonParameters</span></span>
<span data-ttu-id="8b8c1-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b8c1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b8c1-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b8c1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b8c1-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b8c1-139">INPUTS</span></span>

### <span data-ttu-id="8b8c1-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8b8c1-140">System.String</span></span>

### <span data-ttu-id="8b8c1-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8b8c1-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="8b8c1-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="8b8c1-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="8b8c1-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b8c1-143">OUTPUTS</span></span>

### <span data-ttu-id="8b8c1-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="8b8c1-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="8b8c1-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b8c1-145">NOTES</span></span>

## <span data-ttu-id="8b8c1-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b8c1-146">RELATED LINKS</span></span>
