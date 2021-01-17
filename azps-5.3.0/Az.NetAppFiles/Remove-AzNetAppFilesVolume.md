---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: 9400efa61a98b6eb80b975d4999e03eb872e3b28
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422535"
---
# <span data-ttu-id="49f6c-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="49f6c-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="49f6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="49f6c-103">Удаляет громкость файлов Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="49f6c-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="49f6c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="49f6c-104">SYNTAX</span></span>

### <span data-ttu-id="49f6c-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49f6c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49f6c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49f6c-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49f6c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49f6c-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49f6c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49f6c-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49f6c-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49f6c-109">DESCRIPTION</span></span>
<span data-ttu-id="49f6c-110">Для удаления тома ANF удаляется **cmdlet Remove-AzNetAppFilesVolume.**</span><span class="sxs-lookup"><span data-stu-id="49f6c-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="49f6c-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="49f6c-111">EXAMPLES</span></span>

### <span data-ttu-id="49f6c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="49f6c-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="49f6c-113">Эта команда удаляет том ANF "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="49f6c-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="49f6c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49f6c-114">PARAMETERS</span></span>

### <span data-ttu-id="49f6c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="49f6c-115">-AccountName</span></span>
<span data-ttu-id="49f6c-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="49f6c-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="49f6c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f6c-117">-DefaultProfile</span></span>
<span data-ttu-id="49f6c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49f6c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49f6c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49f6c-119">-InputObject</span></span>
<span data-ttu-id="49f6c-120">Удаляемый объект громкости</span><span class="sxs-lookup"><span data-stu-id="49f6c-120">The volume object to remove</span></span>

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

### <span data-ttu-id="49f6c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="49f6c-121">-Name</span></span>
<span data-ttu-id="49f6c-122">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="49f6c-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="49f6c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49f6c-123">-PassThru</span></span>
<span data-ttu-id="49f6c-124">Возвращает, была ли удалена указанная громкость.</span><span class="sxs-lookup"><span data-stu-id="49f6c-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="49f6c-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="49f6c-125">-PoolName</span></span>
<span data-ttu-id="49f6c-126">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="49f6c-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="49f6c-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="49f6c-127">-PoolObject</span></span>
<span data-ttu-id="49f6c-128">Объект пула, содержащий удаляемую громкость</span><span class="sxs-lookup"><span data-stu-id="49f6c-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="49f6c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49f6c-129">-ResourceGroupName</span></span>
<span data-ttu-id="49f6c-130">Группа ресурсов для тома ANF</span><span class="sxs-lookup"><span data-stu-id="49f6c-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="49f6c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49f6c-131">-ResourceId</span></span>
<span data-ttu-id="49f6c-132">ИД ресурса для тома ANF</span><span class="sxs-lookup"><span data-stu-id="49f6c-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="49f6c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49f6c-133">-Confirm</span></span>
<span data-ttu-id="49f6c-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="49f6c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49f6c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49f6c-135">-WhatIf</span></span>
<span data-ttu-id="49f6c-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49f6c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49f6c-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="49f6c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49f6c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f6c-138">CommonParameters</span></span>
<span data-ttu-id="49f6c-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49f6c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f6c-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49f6c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f6c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49f6c-141">INPUTS</span></span>

### <span data-ttu-id="49f6c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="49f6c-142">System.String</span></span>

### <span data-ttu-id="49f6c-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="49f6c-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="49f6c-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="49f6c-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="49f6c-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49f6c-145">OUTPUTS</span></span>

### <span data-ttu-id="49f6c-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49f6c-146">System.Boolean</span></span>

## <span data-ttu-id="49f6c-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="49f6c-147">NOTES</span></span>

## <span data-ttu-id="49f6c-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49f6c-148">RELATED LINKS</span></span>
