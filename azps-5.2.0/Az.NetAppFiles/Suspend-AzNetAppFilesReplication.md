---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: ab4d79b4770f438b233e5bfcc740e79364955ea6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398719"
---
# <span data-ttu-id="2d338-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="2d338-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="2d338-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d338-102">SYNOPSIS</span></span>
<span data-ttu-id="2d338-103">Приостановка/разрыв соединения репликации на томе назначения</span><span class="sxs-lookup"><span data-stu-id="2d338-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="2d338-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2d338-104">SYNTAX</span></span>

### <span data-ttu-id="2d338-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d338-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-ForceBreak] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d338-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d338-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d338-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d338-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d338-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d338-108">DESCRIPTION</span></span>
<span data-ttu-id="2d338-109">Приостановка/разрыв соединения репликации на томе назначения</span><span class="sxs-lookup"><span data-stu-id="2d338-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="2d338-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2d338-110">EXAMPLES</span></span>

### <span data-ttu-id="2d338-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2d338-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="2d338-112">Эта команда приостанавливать подключение репликации ANF для тома "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="2d338-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="2d338-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d338-113">PARAMETERS</span></span>

### <span data-ttu-id="2d338-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2d338-114">-AccountName</span></span>
<span data-ttu-id="2d338-115">Имя учетной записи ANF тома репликации</span><span class="sxs-lookup"><span data-stu-id="2d338-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="2d338-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d338-116">-DefaultProfile</span></span>
<span data-ttu-id="2d338-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d338-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d338-118">-ForceBreak</span><span class="sxs-lookup"><span data-stu-id="2d338-118">-ForceBreak</span></span>
<span data-ttu-id="2d338-119">Если репликация находится в состоянии и вы хотите принудительно нарушить репликацию, установите для этого истина.</span><span class="sxs-lookup"><span data-stu-id="2d338-119">If replication is in status transferring and you want to force break the replication, set to true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d338-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d338-120">-InputObject</span></span>
<span data-ttu-id="2d338-121">Объект назначения тома ANF с разрывом репликации</span><span class="sxs-lookup"><span data-stu-id="2d338-121">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="2d338-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2d338-122">-Name</span></span>
<span data-ttu-id="2d338-123">Имя конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="2d338-123">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="2d338-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d338-124">-PassThru</span></span>
<span data-ttu-id="2d338-125">Возвращает, был ли выполнен разрыв указанной репликации громкости.</span><span class="sxs-lookup"><span data-stu-id="2d338-125">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="2d338-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="2d338-126">-PoolName</span></span>
<span data-ttu-id="2d338-127">Имя пула ANF тома репликации</span><span class="sxs-lookup"><span data-stu-id="2d338-127">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="2d338-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d338-128">-ResourceGroupName</span></span>
<span data-ttu-id="2d338-129">Группа ресурсов для конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="2d338-129">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="2d338-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d338-130">-ResourceId</span></span>
<span data-ttu-id="2d338-131">ИД ресурса конечного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="2d338-131">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="2d338-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d338-132">-Confirm</span></span>
<span data-ttu-id="2d338-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2d338-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d338-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d338-134">-WhatIf</span></span>
<span data-ttu-id="2d338-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d338-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d338-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2d338-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d338-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d338-137">CommonParameters</span></span>
<span data-ttu-id="2d338-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d338-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d338-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d338-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d338-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d338-140">INPUTS</span></span>

### <span data-ttu-id="2d338-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2d338-141">System.String</span></span>

### <span data-ttu-id="2d338-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2d338-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="2d338-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2d338-143">OUTPUTS</span></span>

### <span data-ttu-id="2d338-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2d338-144">System.Boolean</span></span>

## <span data-ttu-id="2d338-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2d338-145">NOTES</span></span>

## <span data-ttu-id="2d338-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d338-146">RELATED LINKS</span></span>
