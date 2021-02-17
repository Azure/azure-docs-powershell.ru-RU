---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1d28420e9457826f7c851eb0d3013f36de9edbc2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218892"
---
# <span data-ttu-id="691ff-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="691ff-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="691ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="691ff-102">SYNOPSIS</span></span>
<span data-ttu-id="691ff-103">Удаляет моментальный снимок файла в Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="691ff-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="691ff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="691ff-104">SYNTAX</span></span>

### <span data-ttu-id="691ff-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="691ff-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="691ff-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="691ff-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="691ff-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="691ff-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="691ff-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="691ff-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="691ff-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="691ff-109">DESCRIPTION</span></span>
<span data-ttu-id="691ff-110">При наступлении на нее снимка anF удаляется **cmdlet Remove-AzNetAppFilesSnapshot.**</span><span class="sxs-lookup"><span data-stu-id="691ff-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="691ff-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="691ff-111">EXAMPLES</span></span>

### <span data-ttu-id="691ff-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="691ff-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="691ff-113">Эта команда удаляет снимок ANF "MyAnfSnapshot".</span><span class="sxs-lookup"><span data-stu-id="691ff-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="691ff-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="691ff-114">PARAMETERS</span></span>

### <span data-ttu-id="691ff-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="691ff-115">-AccountName</span></span>
<span data-ttu-id="691ff-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="691ff-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="691ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="691ff-117">-DefaultProfile</span></span>
<span data-ttu-id="691ff-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="691ff-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="691ff-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="691ff-119">-InputObject</span></span>
<span data-ttu-id="691ff-120">Снимок объекта, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="691ff-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="691ff-121">-Name</span><span class="sxs-lookup"><span data-stu-id="691ff-121">-Name</span></span>
<span data-ttu-id="691ff-122">Имя моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="691ff-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ff-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="691ff-123">-PassThru</span></span>
<span data-ttu-id="691ff-124">Возвращает, была ли удалена указанная громкость.</span><span class="sxs-lookup"><span data-stu-id="691ff-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="691ff-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="691ff-125">-PoolName</span></span>
<span data-ttu-id="691ff-126">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="691ff-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="691ff-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="691ff-127">-ResourceGroupName</span></span>
<span data-ttu-id="691ff-128">Группа ресурсов моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="691ff-128">The resource group of the ANF snapshot</span></span>

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

### <span data-ttu-id="691ff-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="691ff-129">-ResourceId</span></span>
<span data-ttu-id="691ff-130">ИД ресурса моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="691ff-130">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="691ff-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="691ff-131">-VolumeName</span></span>
<span data-ttu-id="691ff-132">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="691ff-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="691ff-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="691ff-133">-VolumeObject</span></span>
<span data-ttu-id="691ff-134">Объект громкости, содержащий моментальный снимок, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="691ff-134">The volume object containing the snapshot to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="691ff-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="691ff-135">-Confirm</span></span>
<span data-ttu-id="691ff-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="691ff-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="691ff-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="691ff-137">-WhatIf</span></span>
<span data-ttu-id="691ff-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="691ff-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="691ff-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="691ff-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="691ff-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="691ff-140">CommonParameters</span></span>
<span data-ttu-id="691ff-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="691ff-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="691ff-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="691ff-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="691ff-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="691ff-143">INPUTS</span></span>

### <span data-ttu-id="691ff-144">System.String</span><span class="sxs-lookup"><span data-stu-id="691ff-144">System.String</span></span>

### <span data-ttu-id="691ff-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="691ff-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="691ff-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="691ff-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="691ff-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="691ff-147">OUTPUTS</span></span>

### <span data-ttu-id="691ff-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="691ff-148">System.Boolean</span></span>

## <span data-ttu-id="691ff-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="691ff-149">NOTES</span></span>

## <span data-ttu-id="691ff-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="691ff-150">RELATED LINKS</span></span>
