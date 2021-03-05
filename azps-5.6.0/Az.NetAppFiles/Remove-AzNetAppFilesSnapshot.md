---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 340adf5b3114750212ad1e2458159f48a9dae91f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968280"
---
# <span data-ttu-id="6c8d9-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="6c8d9-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="6c8d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c8d9-102">SYNOPSIS</span></span>
<span data-ttu-id="6c8d9-103">Удаляет моментальный снимок файла в Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="6c8d9-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="6c8d9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6c8d9-104">SYNTAX</span></span>

### <span data-ttu-id="6c8d9-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6c8d9-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c8d9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c8d9-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c8d9-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c8d9-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c8d9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c8d9-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c8d9-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c8d9-109">DESCRIPTION</span></span>
<span data-ttu-id="6c8d9-110">При наступлении на нее снимка ANF удаляется **cmdlet Remove-AzNetAppFilesSnapshot.**</span><span class="sxs-lookup"><span data-stu-id="6c8d9-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="6c8d9-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6c8d9-111">EXAMPLES</span></span>

### <span data-ttu-id="6c8d9-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6c8d9-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="6c8d9-113">Эта команда удаляет снимок ANF "MyAnfSnapshot".</span><span class="sxs-lookup"><span data-stu-id="6c8d9-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="6c8d9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c8d9-114">PARAMETERS</span></span>

### <span data-ttu-id="6c8d9-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6c8d9-115">-AccountName</span></span>
<span data-ttu-id="6c8d9-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="6c8d9-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="6c8d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c8d9-117">-DefaultProfile</span></span>
<span data-ttu-id="6c8d9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c8d9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c8d9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c8d9-119">-InputObject</span></span>
<span data-ttu-id="6c8d9-120">Снимок объекта, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="6c8d9-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="6c8d9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6c8d9-121">-Name</span></span>
<span data-ttu-id="6c8d9-122">Имя моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="6c8d9-122">The name of the ANF snapshot</span></span>

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

### <span data-ttu-id="6c8d9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c8d9-123">-PassThru</span></span>
<span data-ttu-id="6c8d9-124">Возврат, была ли указанная громкость успешно удалена</span><span class="sxs-lookup"><span data-stu-id="6c8d9-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="6c8d9-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="6c8d9-125">-PoolName</span></span>
<span data-ttu-id="6c8d9-126">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="6c8d9-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="6c8d9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c8d9-127">-ResourceGroupName</span></span>
<span data-ttu-id="6c8d9-128">Группа ресурсов моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="6c8d9-128">The resource group of the ANF snapshot</span></span>

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

### <span data-ttu-id="6c8d9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c8d9-129">-ResourceId</span></span>
<span data-ttu-id="6c8d9-130">ИД ресурса моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="6c8d9-130">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="6c8d9-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="6c8d9-131">-VolumeName</span></span>
<span data-ttu-id="6c8d9-132">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="6c8d9-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="6c8d9-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="6c8d9-133">-VolumeObject</span></span>
<span data-ttu-id="6c8d9-134">Объект громкости, содержащий моментальный снимок, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="6c8d9-134">The volume object containing the snapshot to remove</span></span>

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

### <span data-ttu-id="6c8d9-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c8d9-135">-Confirm</span></span>
<span data-ttu-id="6c8d9-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c8d9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c8d9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c8d9-137">-WhatIf</span></span>
<span data-ttu-id="6c8d9-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c8d9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c8d9-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6c8d9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c8d9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c8d9-140">CommonParameters</span></span>
<span data-ttu-id="6c8d9-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c8d9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c8d9-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c8d9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c8d9-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c8d9-143">INPUTS</span></span>

### <span data-ttu-id="6c8d9-144">System.String</span><span class="sxs-lookup"><span data-stu-id="6c8d9-144">System.String</span></span>

### <span data-ttu-id="6c8d9-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6c8d9-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="6c8d9-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="6c8d9-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="6c8d9-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6c8d9-147">OUTPUTS</span></span>

### <span data-ttu-id="6c8d9-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6c8d9-148">System.Boolean</span></span>

## <span data-ttu-id="6c8d9-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6c8d9-149">NOTES</span></span>

## <span data-ttu-id="6c8d9-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c8d9-150">RELATED LINKS</span></span>
