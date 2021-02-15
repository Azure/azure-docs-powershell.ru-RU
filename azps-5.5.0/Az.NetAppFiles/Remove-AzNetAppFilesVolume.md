---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: 9400efa61a98b6eb80b975d4999e03eb872e3b28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221337"
---
# <span data-ttu-id="62bb8-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="62bb8-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="62bb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62bb8-102">SYNOPSIS</span></span>
<span data-ttu-id="62bb8-103">Удаляет громкость файлов Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="62bb8-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="62bb8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="62bb8-104">SYNTAX</span></span>

### <span data-ttu-id="62bb8-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62bb8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62bb8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62bb8-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62bb8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62bb8-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62bb8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62bb8-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62bb8-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62bb8-109">DESCRIPTION</span></span>
<span data-ttu-id="62bb8-110">Для удаления тома ANF удаляется **cmdlet Remove-AzNetAppFilesVolume.**</span><span class="sxs-lookup"><span data-stu-id="62bb8-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="62bb8-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="62bb8-111">EXAMPLES</span></span>

### <span data-ttu-id="62bb8-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62bb8-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="62bb8-113">Эта команда удаляет том ANF "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="62bb8-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="62bb8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62bb8-114">PARAMETERS</span></span>

### <span data-ttu-id="62bb8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="62bb8-115">-AccountName</span></span>
<span data-ttu-id="62bb8-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="62bb8-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="62bb8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62bb8-117">-DefaultProfile</span></span>
<span data-ttu-id="62bb8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62bb8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62bb8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62bb8-119">-InputObject</span></span>
<span data-ttu-id="62bb8-120">Удаляемый объект громкости</span><span class="sxs-lookup"><span data-stu-id="62bb8-120">The volume object to remove</span></span>

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

### <span data-ttu-id="62bb8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="62bb8-121">-Name</span></span>
<span data-ttu-id="62bb8-122">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="62bb8-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="62bb8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62bb8-123">-PassThru</span></span>
<span data-ttu-id="62bb8-124">Возврат, была ли указанная громкость успешно удалена</span><span class="sxs-lookup"><span data-stu-id="62bb8-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="62bb8-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="62bb8-125">-PoolName</span></span>
<span data-ttu-id="62bb8-126">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="62bb8-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="62bb8-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="62bb8-127">-PoolObject</span></span>
<span data-ttu-id="62bb8-128">Объект пула, содержащий удаляемую громкость</span><span class="sxs-lookup"><span data-stu-id="62bb8-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="62bb8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62bb8-129">-ResourceGroupName</span></span>
<span data-ttu-id="62bb8-130">Группа ресурсов тома ANF</span><span class="sxs-lookup"><span data-stu-id="62bb8-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="62bb8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62bb8-131">-ResourceId</span></span>
<span data-ttu-id="62bb8-132">ИД ресурса для тома ANF</span><span class="sxs-lookup"><span data-stu-id="62bb8-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="62bb8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62bb8-133">-Confirm</span></span>
<span data-ttu-id="62bb8-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62bb8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62bb8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62bb8-135">-WhatIf</span></span>
<span data-ttu-id="62bb8-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62bb8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62bb8-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="62bb8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62bb8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62bb8-138">CommonParameters</span></span>
<span data-ttu-id="62bb8-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62bb8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62bb8-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62bb8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62bb8-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62bb8-141">INPUTS</span></span>

### <span data-ttu-id="62bb8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="62bb8-142">System.String</span></span>

### <span data-ttu-id="62bb8-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="62bb8-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="62bb8-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="62bb8-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="62bb8-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62bb8-145">OUTPUTS</span></span>

### <span data-ttu-id="62bb8-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="62bb8-146">System.Boolean</span></span>

## <span data-ttu-id="62bb8-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="62bb8-147">NOTES</span></span>

## <span data-ttu-id="62bb8-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62bb8-148">RELATED LINKS</span></span>
