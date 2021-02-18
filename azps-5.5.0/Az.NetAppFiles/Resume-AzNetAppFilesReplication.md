---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241136"
---
# <span data-ttu-id="8d469-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="8d469-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="8d469-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d469-102">SYNOPSIS</span></span>
<span data-ttu-id="8d469-103">Возобновление/resync соединение на томе назначения.</span><span class="sxs-lookup"><span data-stu-id="8d469-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="8d469-104">Если операция будет происходить с исходным томом, подключение и синхронизация будут отменены.</span><span class="sxs-lookup"><span data-stu-id="8d469-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="8d469-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8d469-105">SYNTAX</span></span>

### <span data-ttu-id="8d469-106">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d469-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d469-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d469-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d469-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d469-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d469-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d469-109">DESCRIPTION</span></span>
<span data-ttu-id="8d469-110">Возобновление/resync подключение к громкости назначения</span><span class="sxs-lookup"><span data-stu-id="8d469-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="8d469-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8d469-111">EXAMPLES</span></span>

### <span data-ttu-id="8d469-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8d469-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="8d469-113">Эта команда возобновляет подключение репликации ANF для тома "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="8d469-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="8d469-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d469-114">PARAMETERS</span></span>

### <span data-ttu-id="8d469-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8d469-115">-AccountName</span></span>
<span data-ttu-id="8d469-116">Имя учетной записи ANF тома репликации</span><span class="sxs-lookup"><span data-stu-id="8d469-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="8d469-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d469-117">-DefaultProfile</span></span>
<span data-ttu-id="8d469-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d469-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d469-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d469-119">-InputObject</span></span>
<span data-ttu-id="8d469-120">Объект тома назначения репликации ANF для повторного перенаправления</span><span class="sxs-lookup"><span data-stu-id="8d469-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="8d469-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8d469-121">-Name</span></span>
<span data-ttu-id="8d469-122">Имя конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="8d469-122">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d469-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d469-123">-PassThru</span></span>
<span data-ttu-id="8d469-124">Возвращает, выполняется ли повторение указанного тома репликации.</span><span class="sxs-lookup"><span data-stu-id="8d469-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="8d469-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="8d469-125">-PoolName</span></span>
<span data-ttu-id="8d469-126">Имя пула ANF для тома репликации</span><span class="sxs-lookup"><span data-stu-id="8d469-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="8d469-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d469-127">-ResourceGroupName</span></span>
<span data-ttu-id="8d469-128">Группа ресурсов для конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="8d469-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="8d469-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d469-129">-ResourceId</span></span>
<span data-ttu-id="8d469-130">ИД ресурса конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="8d469-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="8d469-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d469-131">-Confirm</span></span>
<span data-ttu-id="8d469-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8d469-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d469-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d469-133">-WhatIf</span></span>
<span data-ttu-id="8d469-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d469-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d469-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8d469-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d469-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d469-136">CommonParameters</span></span>
<span data-ttu-id="8d469-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d469-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d469-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d469-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d469-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d469-139">INPUTS</span></span>

### <span data-ttu-id="8d469-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8d469-140">System.String</span></span>

### <span data-ttu-id="8d469-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8d469-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="8d469-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8d469-142">OUTPUTS</span></span>

### <span data-ttu-id="8d469-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8d469-143">System.Boolean</span></span>

## <span data-ttu-id="8d469-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8d469-144">NOTES</span></span>

## <span data-ttu-id="8d469-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d469-145">RELATED LINKS</span></span>
