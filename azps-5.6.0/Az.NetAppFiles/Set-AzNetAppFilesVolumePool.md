---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/set-aznetAppfilesvolumepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
ms.openlocfilehash: 2b3cf6588f32fd958073ced8d3347733416037ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968179"
---
# <span data-ttu-id="ca8cd-101">Set-AzNetAppFilesVolumePool</span><span class="sxs-lookup"><span data-stu-id="ca8cd-101">Set-AzNetAppFilesVolumePool</span></span>

## <span data-ttu-id="ca8cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca8cd-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8cd-103">Изменение пула для объема файлов Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="ca8cd-103">Change pool for an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="ca8cd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ca8cd-104">SYNTAX</span></span>

### <span data-ttu-id="ca8cd-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ca8cd-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-NewPoolResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca8cd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca8cd-106">ByParentObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -Name <String> -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca8cd-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca8cd-107">ByResourceIdParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca8cd-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca8cd-108">ByObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca8cd-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca8cd-109">DESCRIPTION</span></span>
<span data-ttu-id="ca8cd-110">Для пула ANF изменяется громкость пула **Set-AzNetAppFilesVolumePool.**</span><span class="sxs-lookup"><span data-stu-id="ca8cd-110">The **Set-AzNetAppFilesVolumePool** cmdlet changes the pool of an ANF volume.</span></span>

## <span data-ttu-id="ca8cd-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ca8cd-111">EXAMPLES</span></span>

### <span data-ttu-id="ca8cd-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ca8cd-112">Example 1</span></span>
```powershell
PS C:\>Set-AzNetAppFilesVolumePool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -NewPoolResourceId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="ca8cd-113">Пул myVolume будет меняться на пул с ИД 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="ca8cd-113">This changes the pool for the volume MyVolume to one with the Id of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="ca8cd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca8cd-114">PARAMETERS</span></span>

### <span data-ttu-id="ca8cd-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ca8cd-115">-AccountName</span></span>
<span data-ttu-id="ca8cd-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="ca8cd-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="ca8cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca8cd-117">-DefaultProfile</span></span>
<span data-ttu-id="ca8cd-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca8cd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca8cd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca8cd-119">-InputObject</span></span>
<span data-ttu-id="ca8cd-120">Перемещаемый объект громкости</span><span class="sxs-lookup"><span data-stu-id="ca8cd-120">The volume object to move</span></span>

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

### <span data-ttu-id="ca8cd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ca8cd-121">-Name</span></span>
<span data-ttu-id="ca8cd-122">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="ca8cd-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="ca8cd-123">-NewPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="ca8cd-123">-NewPoolResourceId</span></span>
<span data-ttu-id="ca8cd-124">ResourceId пула емкости для перемещения.</span><span class="sxs-lookup"><span data-stu-id="ca8cd-124">ResourceId of the capacity pool to move to.</span></span>
<span data-ttu-id="ca8cd-125">UUID 4, используемый для определения пула</span><span class="sxs-lookup"><span data-stu-id="ca8cd-125">UUID v4 used to identify the pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8cd-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ca8cd-126">-PoolName</span></span>
<span data-ttu-id="ca8cd-127">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="ca8cd-127">The name of the ANF pool</span></span>

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

### <span data-ttu-id="ca8cd-128">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="ca8cd-128">-PoolObject</span></span>
<span data-ttu-id="ca8cd-129">Объект пула, содержащий громкость</span><span class="sxs-lookup"><span data-stu-id="ca8cd-129">The pool object containing the volume</span></span>

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

### <span data-ttu-id="ca8cd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca8cd-130">-ResourceGroupName</span></span>
<span data-ttu-id="ca8cd-131">Группа ресурсов для тома ANF</span><span class="sxs-lookup"><span data-stu-id="ca8cd-131">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="ca8cd-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca8cd-132">-ResourceId</span></span>
<span data-ttu-id="ca8cd-133">ИД ресурса для тома ANF</span><span class="sxs-lookup"><span data-stu-id="ca8cd-133">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="ca8cd-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca8cd-134">-Confirm</span></span>
<span data-ttu-id="ca8cd-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca8cd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca8cd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca8cd-136">-WhatIf</span></span>
<span data-ttu-id="ca8cd-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca8cd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca8cd-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ca8cd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca8cd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8cd-139">CommonParameters</span></span>
<span data-ttu-id="ca8cd-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca8cd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8cd-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca8cd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8cd-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca8cd-142">INPUTS</span></span>

### <span data-ttu-id="ca8cd-143">System.String</span><span class="sxs-lookup"><span data-stu-id="ca8cd-143">System.String</span></span>

### <span data-ttu-id="ca8cd-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ca8cd-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="ca8cd-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ca8cd-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ca8cd-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ca8cd-146">OUTPUTS</span></span>

### <span data-ttu-id="ca8cd-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ca8cd-147">System.Boolean</span></span>

## <span data-ttu-id="ca8cd-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ca8cd-148">NOTES</span></span>

## <span data-ttu-id="ca8cd-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca8cd-149">RELATED LINKS</span></span>
