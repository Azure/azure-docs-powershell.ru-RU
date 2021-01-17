---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 04ad7f188a2280dcdf84e8b5c1f45e20edf4d07b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410671"
---
# <span data-ttu-id="ed086-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="ed086-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="ed086-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed086-102">SYNOPSIS</span></span>
<span data-ttu-id="ed086-103">Удаление или удаление подключения репликации для назначения тома и отправка выпуска в исходный реплиц.</span><span class="sxs-lookup"><span data-stu-id="ed086-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="ed086-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ed086-104">SYNTAX</span></span>

### <span data-ttu-id="ed086-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed086-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed086-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed086-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed086-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed086-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed086-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed086-108">DESCRIPTION</span></span>
<span data-ttu-id="ed086-109">Удаление или удаление соединения репликации для назначения тома и отправка выпуска в исходный реплиц.</span><span class="sxs-lookup"><span data-stu-id="ed086-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="ed086-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ed086-110">EXAMPLES</span></span>

### <span data-ttu-id="ed086-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ed086-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="ed086-112">Эта команда удаляет подключение репликации ANF для тома "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="ed086-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="ed086-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed086-113">PARAMETERS</span></span>

### <span data-ttu-id="ed086-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed086-114">-AccountName</span></span>
<span data-ttu-id="ed086-115">Имя учетной записи ANF тома репликации</span><span class="sxs-lookup"><span data-stu-id="ed086-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="ed086-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed086-116">-DefaultProfile</span></span>
<span data-ttu-id="ed086-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed086-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed086-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed086-118">-InputObject</span></span>
<span data-ttu-id="ed086-119">Том назначения ANF с удаляемой репликацией</span><span class="sxs-lookup"><span data-stu-id="ed086-119">The ANF destination volume with the replication to remove</span></span>

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

### <span data-ttu-id="ed086-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ed086-120">-Name</span></span>
<span data-ttu-id="ed086-121">Имя конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="ed086-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ed086-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed086-122">-PassThru</span></span>
<span data-ttu-id="ed086-123">Возвращает, была ли удалена указанная репликация ANF.</span><span class="sxs-lookup"><span data-stu-id="ed086-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="ed086-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ed086-124">-PoolName</span></span>
<span data-ttu-id="ed086-125">Имя пула ANF тома репликации</span><span class="sxs-lookup"><span data-stu-id="ed086-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="ed086-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed086-126">-ResourceGroupName</span></span>
<span data-ttu-id="ed086-127">Группа ресурсов для конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="ed086-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ed086-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed086-128">-ResourceId</span></span>
<span data-ttu-id="ed086-129">ИД ресурса конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="ed086-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ed086-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed086-130">-Confirm</span></span>
<span data-ttu-id="ed086-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ed086-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed086-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed086-132">-WhatIf</span></span>
<span data-ttu-id="ed086-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed086-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed086-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ed086-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed086-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed086-135">CommonParameters</span></span>
<span data-ttu-id="ed086-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed086-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed086-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed086-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed086-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed086-138">INPUTS</span></span>

### <span data-ttu-id="ed086-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ed086-139">System.String</span></span>

### <span data-ttu-id="ed086-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ed086-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ed086-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ed086-141">OUTPUTS</span></span>

### <span data-ttu-id="ed086-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ed086-142">System.Boolean</span></span>

## <span data-ttu-id="ed086-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ed086-143">NOTES</span></span>

## <span data-ttu-id="ed086-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed086-144">RELATED LINKS</span></span>
