---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: 9afa4f22de142dba7608d33ed04c972758911aa9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410911"
---
# <span data-ttu-id="aa733-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="aa733-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="aa733-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa733-102">SYNOPSIS</span></span>
<span data-ttu-id="aa733-103">Подключение утверждения и авторизации к исходным томам</span><span class="sxs-lookup"><span data-stu-id="aa733-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="aa733-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aa733-104">SYNTAX</span></span>

### <span data-ttu-id="aa733-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa733-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa733-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa733-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa733-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa733-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa733-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa733-108">DESCRIPTION</span></span>
<span data-ttu-id="aa733-109">Утверждение подключения репликации к исходным томам</span><span class="sxs-lookup"><span data-stu-id="aa733-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="aa733-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aa733-110">EXAMPLES</span></span>

### <span data-ttu-id="aa733-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aa733-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="aa733-112">Эта команда утверждает репликацию на MyAnfVolume.</span><span class="sxs-lookup"><span data-stu-id="aa733-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="aa733-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa733-113">PARAMETERS</span></span>

### <span data-ttu-id="aa733-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aa733-114">-AccountName</span></span>
<span data-ttu-id="aa733-115">Имя учетной записи ANF источника репликации</span><span class="sxs-lookup"><span data-stu-id="aa733-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="aa733-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="aa733-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="aa733-117">The file system id of the destination data protection volume</span><span class="sxs-lookup"><span data-stu-id="aa733-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="aa733-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa733-118">-DefaultProfile</span></span>
<span data-ttu-id="aa733-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa733-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa733-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa733-120">-InputObject</span></span>
<span data-ttu-id="aa733-121">Объект тома источника ANF, авторизованный объект репликации</span><span class="sxs-lookup"><span data-stu-id="aa733-121">The ANF source volume object to authorized the replication destination</span></span>

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

### <span data-ttu-id="aa733-122">-Name</span><span class="sxs-lookup"><span data-stu-id="aa733-122">-Name</span></span>
<span data-ttu-id="aa733-123">Имя источника громкости репликации ANF</span><span class="sxs-lookup"><span data-stu-id="aa733-123">The name of the ANF replication source volume</span></span>

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

### <span data-ttu-id="aa733-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa733-124">-PassThru</span></span>
<span data-ttu-id="aa733-125">Возвращает, была ли выполнена авторизация репликации указанного тома.</span><span class="sxs-lookup"><span data-stu-id="aa733-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="aa733-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="aa733-126">-PoolName</span></span>
<span data-ttu-id="aa733-127">Имя пула ANF источника репликации</span><span class="sxs-lookup"><span data-stu-id="aa733-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="aa733-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa733-128">-ResourceGroupName</span></span>
<span data-ttu-id="aa733-129">Группа ресурсов для источника репликации ANF</span><span class="sxs-lookup"><span data-stu-id="aa733-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="aa733-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa733-130">-ResourceId</span></span>
<span data-ttu-id="aa733-131">Код ресурса для источника репликации ANF</span><span class="sxs-lookup"><span data-stu-id="aa733-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="aa733-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa733-132">-Confirm</span></span>
<span data-ttu-id="aa733-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa733-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa733-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa733-134">-WhatIf</span></span>
<span data-ttu-id="aa733-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa733-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa733-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aa733-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa733-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa733-137">CommonParameters</span></span>
<span data-ttu-id="aa733-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa733-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa733-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa733-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa733-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa733-140">INPUTS</span></span>

### <span data-ttu-id="aa733-141">System.String</span><span class="sxs-lookup"><span data-stu-id="aa733-141">System.String</span></span>

### <span data-ttu-id="aa733-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="aa733-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="aa733-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aa733-143">OUTPUTS</span></span>

### <span data-ttu-id="aa733-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aa733-144">System.Boolean</span></span>

## <span data-ttu-id="aa733-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aa733-145">NOTES</span></span>

## <span data-ttu-id="aa733-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa733-146">RELATED LINKS</span></span>
