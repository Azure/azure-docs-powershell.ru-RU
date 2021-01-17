---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetAppfilesvolumepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
ms.openlocfilehash: 30d525ebcb7d80a24e11080ee265eb509f575ff6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418055"
---
# <span data-ttu-id="9f903-101">Set-AzNetAppFilesVolumePool</span><span class="sxs-lookup"><span data-stu-id="9f903-101">Set-AzNetAppFilesVolumePool</span></span>

## <span data-ttu-id="9f903-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f903-102">SYNOPSIS</span></span>
<span data-ttu-id="9f903-103">Изменение пула для объема файлов Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="9f903-103">Change pool for an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="9f903-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9f903-104">SYNTAX</span></span>

### <span data-ttu-id="9f903-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f903-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-NewPoolResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f903-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f903-106">ByParentObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -Name <String> -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f903-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f903-107">ByResourceIdParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f903-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f903-108">ByObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f903-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f903-109">DESCRIPTION</span></span>
<span data-ttu-id="9f903-110">При наступлении на нее громкости пула ANF изменяется с его наступлении **cmdlet Set-AzNetAppFilesVolumePool.**</span><span class="sxs-lookup"><span data-stu-id="9f903-110">The **Set-AzNetAppFilesVolumePool** cmdlet changes the pool of an ANF volume.</span></span>

## <span data-ttu-id="9f903-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9f903-111">EXAMPLES</span></span>

### <span data-ttu-id="9f903-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f903-112">Example 1</span></span>
```powershell
PS C:\>Set-AzNetAppFilesVolumePool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -NewPoolResourceId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="9f903-113">Пул MyVolume будет меняться на один с ИД 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="9f903-113">This changes the pool for the volume MyVolume to one with the Id of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="9f903-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f903-114">PARAMETERS</span></span>

### <span data-ttu-id="9f903-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9f903-115">-AccountName</span></span>
<span data-ttu-id="9f903-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="9f903-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="9f903-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f903-117">-DefaultProfile</span></span>
<span data-ttu-id="9f903-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f903-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f903-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f903-119">-InputObject</span></span>
<span data-ttu-id="9f903-120">Перемещаемый объект громкости</span><span class="sxs-lookup"><span data-stu-id="9f903-120">The volume object to move</span></span>

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

### <span data-ttu-id="9f903-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9f903-121">-Name</span></span>
<span data-ttu-id="9f903-122">Название тома ANF</span><span class="sxs-lookup"><span data-stu-id="9f903-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="9f903-123">-NewPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="9f903-123">-NewPoolResourceId</span></span>
<span data-ttu-id="9f903-124">ResourceId пула емкости для перемещения.</span><span class="sxs-lookup"><span data-stu-id="9f903-124">ResourceId of the capacity pool to move to.</span></span>
<span data-ttu-id="9f903-125">UUID 4, используемый для определения пула</span><span class="sxs-lookup"><span data-stu-id="9f903-125">UUID v4 used to identify the pool</span></span>

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

### <span data-ttu-id="9f903-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="9f903-126">-PoolName</span></span>
<span data-ttu-id="9f903-127">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="9f903-127">The name of the ANF pool</span></span>

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

### <span data-ttu-id="9f903-128">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="9f903-128">-PoolObject</span></span>
<span data-ttu-id="9f903-129">Объект пула, содержащий громкость</span><span class="sxs-lookup"><span data-stu-id="9f903-129">The pool object containing the volume</span></span>

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

### <span data-ttu-id="9f903-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f903-130">-ResourceGroupName</span></span>
<span data-ttu-id="9f903-131">Группа ресурсов для тома ANF</span><span class="sxs-lookup"><span data-stu-id="9f903-131">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="9f903-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f903-132">-ResourceId</span></span>
<span data-ttu-id="9f903-133">ИД ресурса для тома ANF</span><span class="sxs-lookup"><span data-stu-id="9f903-133">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="9f903-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f903-134">-Confirm</span></span>
<span data-ttu-id="9f903-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9f903-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f903-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f903-136">-WhatIf</span></span>
<span data-ttu-id="9f903-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f903-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f903-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9f903-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f903-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f903-139">CommonParameters</span></span>
<span data-ttu-id="9f903-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f903-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f903-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f903-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f903-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f903-142">INPUTS</span></span>

### <span data-ttu-id="9f903-143">System.String</span><span class="sxs-lookup"><span data-stu-id="9f903-143">System.String</span></span>

### <span data-ttu-id="9f903-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="9f903-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="9f903-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9f903-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="9f903-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f903-146">OUTPUTS</span></span>

### <span data-ttu-id="9f903-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9f903-147">System.Boolean</span></span>

## <span data-ttu-id="9f903-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9f903-148">NOTES</span></span>

## <span data-ttu-id="9f903-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f903-149">RELATED LINKS</span></span>
