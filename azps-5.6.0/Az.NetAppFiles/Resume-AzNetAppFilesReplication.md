---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 5f5dac2f2028de9b90941ef91c38361c4357fc8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968232"
---
# <span data-ttu-id="b7e00-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="b7e00-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="b7e00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7e00-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e00-103">Возобновление/resync соединение на томе назначения.</span><span class="sxs-lookup"><span data-stu-id="b7e00-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="b7e00-104">Если операция будет происходить с исходным томом, подключение и синхронизация будут отменены.</span><span class="sxs-lookup"><span data-stu-id="b7e00-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="b7e00-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b7e00-105">SYNTAX</span></span>

### <span data-ttu-id="b7e00-106">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b7e00-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7e00-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7e00-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7e00-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7e00-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7e00-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7e00-109">DESCRIPTION</span></span>
<span data-ttu-id="b7e00-110">Возобновление/resync подключение к громкости назначения</span><span class="sxs-lookup"><span data-stu-id="b7e00-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="b7e00-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b7e00-111">EXAMPLES</span></span>

### <span data-ttu-id="b7e00-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b7e00-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="b7e00-113">Эта команда возобновляет подключение репликации ANF к громкости "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="b7e00-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="b7e00-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7e00-114">PARAMETERS</span></span>

### <span data-ttu-id="b7e00-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b7e00-115">-AccountName</span></span>
<span data-ttu-id="b7e00-116">Имя учетной записи ANF тома репликации</span><span class="sxs-lookup"><span data-stu-id="b7e00-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="b7e00-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7e00-117">-DefaultProfile</span></span>
<span data-ttu-id="b7e00-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7e00-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7e00-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7e00-119">-InputObject</span></span>
<span data-ttu-id="b7e00-120">Объект тома назначения репликации ANF для повторного перенаправления</span><span class="sxs-lookup"><span data-stu-id="b7e00-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="b7e00-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b7e00-121">-Name</span></span>
<span data-ttu-id="b7e00-122">Имя конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="b7e00-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="b7e00-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7e00-123">-PassThru</span></span>
<span data-ttu-id="b7e00-124">Возвращает, выполняется ли повторение указанного тома репликации.</span><span class="sxs-lookup"><span data-stu-id="b7e00-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="b7e00-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="b7e00-125">-PoolName</span></span>
<span data-ttu-id="b7e00-126">Имя пула ANF для тома репликации</span><span class="sxs-lookup"><span data-stu-id="b7e00-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="b7e00-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7e00-127">-ResourceGroupName</span></span>
<span data-ttu-id="b7e00-128">Группа ресурсов для конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="b7e00-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="b7e00-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7e00-129">-ResourceId</span></span>
<span data-ttu-id="b7e00-130">ИД ресурса конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="b7e00-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="b7e00-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7e00-131">-Confirm</span></span>
<span data-ttu-id="b7e00-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7e00-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7e00-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7e00-133">-WhatIf</span></span>
<span data-ttu-id="b7e00-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7e00-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7e00-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b7e00-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7e00-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e00-136">CommonParameters</span></span>
<span data-ttu-id="b7e00-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7e00-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e00-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7e00-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e00-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7e00-139">INPUTS</span></span>

### <span data-ttu-id="b7e00-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b7e00-140">System.String</span></span>

### <span data-ttu-id="b7e00-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b7e00-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b7e00-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b7e00-142">OUTPUTS</span></span>

### <span data-ttu-id="b7e00-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b7e00-143">System.Boolean</span></span>

## <span data-ttu-id="b7e00-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b7e00-144">NOTES</span></span>

## <span data-ttu-id="b7e00-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7e00-145">RELATED LINKS</span></span>
