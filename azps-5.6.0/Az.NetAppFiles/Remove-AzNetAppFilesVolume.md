---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: f53ca76da23620a37020a14877059aae4f4c9808
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968264"
---
# <span data-ttu-id="b0e1a-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b0e1a-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="b0e1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e1a-103">Удаляет громкость файлов Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="b0e1a-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="b0e1a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b0e1a-104">SYNTAX</span></span>

### <span data-ttu-id="b0e1a-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b0e1a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e1a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0e1a-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e1a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0e1a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e1a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0e1a-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0e1a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0e1a-109">DESCRIPTION</span></span>
<span data-ttu-id="b0e1a-110">Для удаления тома ANF удаляется **cmdlet Remove-AzNetAppFilesVolume.**</span><span class="sxs-lookup"><span data-stu-id="b0e1a-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="b0e1a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b0e1a-111">EXAMPLES</span></span>

### <span data-ttu-id="b0e1a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b0e1a-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="b0e1a-113">Эта команда удаляет том ANF "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="b0e1a-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="b0e1a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0e1a-114">PARAMETERS</span></span>

### <span data-ttu-id="b0e1a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b0e1a-115">-AccountName</span></span>
<span data-ttu-id="b0e1a-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="b0e1a-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="b0e1a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e1a-117">-DefaultProfile</span></span>
<span data-ttu-id="b0e1a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0e1a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0e1a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0e1a-119">-InputObject</span></span>
<span data-ttu-id="b0e1a-120">Удаляемый объект громкости</span><span class="sxs-lookup"><span data-stu-id="b0e1a-120">The volume object to remove</span></span>

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

### <span data-ttu-id="b0e1a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b0e1a-121">-Name</span></span>
<span data-ttu-id="b0e1a-122">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="b0e1a-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="b0e1a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0e1a-123">-PassThru</span></span>
<span data-ttu-id="b0e1a-124">Возврат, была ли указанная громкость успешно удалена</span><span class="sxs-lookup"><span data-stu-id="b0e1a-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="b0e1a-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="b0e1a-125">-PoolName</span></span>
<span data-ttu-id="b0e1a-126">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="b0e1a-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="b0e1a-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="b0e1a-127">-PoolObject</span></span>
<span data-ttu-id="b0e1a-128">Объект пула, содержащий удаляемую громкость</span><span class="sxs-lookup"><span data-stu-id="b0e1a-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="b0e1a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0e1a-129">-ResourceGroupName</span></span>
<span data-ttu-id="b0e1a-130">Группа ресурсов тома ANF</span><span class="sxs-lookup"><span data-stu-id="b0e1a-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="b0e1a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0e1a-131">-ResourceId</span></span>
<span data-ttu-id="b0e1a-132">ИД ресурса для тома ANF</span><span class="sxs-lookup"><span data-stu-id="b0e1a-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="b0e1a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0e1a-133">-Confirm</span></span>
<span data-ttu-id="b0e1a-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0e1a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0e1a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0e1a-135">-WhatIf</span></span>
<span data-ttu-id="b0e1a-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0e1a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0e1a-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b0e1a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0e1a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e1a-138">CommonParameters</span></span>
<span data-ttu-id="b0e1a-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0e1a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e1a-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0e1a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e1a-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0e1a-141">INPUTS</span></span>

### <span data-ttu-id="b0e1a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b0e1a-142">System.String</span></span>

### <span data-ttu-id="b0e1a-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="b0e1a-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="b0e1a-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b0e1a-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b0e1a-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0e1a-145">OUTPUTS</span></span>

### <span data-ttu-id="b0e1a-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b0e1a-146">System.Boolean</span></span>

## <span data-ttu-id="b0e1a-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b0e1a-147">NOTES</span></span>

## <span data-ttu-id="b0e1a-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0e1a-148">RELATED LINKS</span></span>
