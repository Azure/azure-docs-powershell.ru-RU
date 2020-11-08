---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: 9afa4f22de142dba7608d33ed04c972758911aa9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243469"
---
# <span data-ttu-id="6fd81-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="6fd81-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="6fd81-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6fd81-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd81-103">Утверждение и авторизация подключения репликации на исходном томе</span><span class="sxs-lookup"><span data-stu-id="6fd81-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="6fd81-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6fd81-104">SYNTAX</span></span>

### <span data-ttu-id="6fd81-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6fd81-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd81-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fd81-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd81-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fd81-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fd81-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fd81-108">DESCRIPTION</span></span>
<span data-ttu-id="6fd81-109">Утверждение подключения репликации на исходном томе</span><span class="sxs-lookup"><span data-stu-id="6fd81-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="6fd81-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6fd81-110">EXAMPLES</span></span>

### <span data-ttu-id="6fd81-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6fd81-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="6fd81-112">Эта команда утверждает репликацию на MyAnfVolume.</span><span class="sxs-lookup"><span data-stu-id="6fd81-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="6fd81-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6fd81-113">PARAMETERS</span></span>

### <span data-ttu-id="6fd81-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="6fd81-114">-AccountName</span></span>
<span data-ttu-id="6fd81-115">Имя учетной записи ANF исходного тома репликации</span><span class="sxs-lookup"><span data-stu-id="6fd81-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="6fd81-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="6fd81-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="6fd81-117">Идентификатор файловой системы конечного тома защиты данных</span><span class="sxs-lookup"><span data-stu-id="6fd81-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="6fd81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd81-118">-DefaultProfile</span></span>
<span data-ttu-id="6fd81-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd81-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fd81-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fd81-120">-InputObject</span></span>
<span data-ttu-id="6fd81-121">Объект исходного тома ANF для авторизации места назначения репликации</span><span class="sxs-lookup"><span data-stu-id="6fd81-121">The ANF source volume object to authorized the replication destination</span></span>

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

### <span data-ttu-id="6fd81-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6fd81-122">-Name</span></span>
<span data-ttu-id="6fd81-123">Имя тома источника репликации ANF</span><span class="sxs-lookup"><span data-stu-id="6fd81-123">The name of the ANF replication source volume</span></span>

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

### <span data-ttu-id="6fd81-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fd81-124">-PassThru</span></span>
<span data-ttu-id="6fd81-125">Возвращает значение, указывающее, была ли выполнена авторизация репликации заданного тома.</span><span class="sxs-lookup"><span data-stu-id="6fd81-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="6fd81-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="6fd81-126">-PoolName</span></span>
<span data-ttu-id="6fd81-127">Имя пула ANF исходного тома репликации</span><span class="sxs-lookup"><span data-stu-id="6fd81-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="6fd81-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fd81-128">-ResourceGroupName</span></span>
<span data-ttu-id="6fd81-129">Группа ресурсов для тома источника репликации ANF</span><span class="sxs-lookup"><span data-stu-id="6fd81-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="6fd81-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fd81-130">-ResourceId</span></span>
<span data-ttu-id="6fd81-131">Идентификатор ресурса исходного тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="6fd81-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="6fd81-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6fd81-132">-Confirm</span></span>
<span data-ttu-id="6fd81-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6fd81-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fd81-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fd81-134">-WhatIf</span></span>
<span data-ttu-id="6fd81-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6fd81-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fd81-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6fd81-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fd81-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd81-137">CommonParameters</span></span>
<span data-ttu-id="6fd81-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6fd81-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd81-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fd81-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd81-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6fd81-140">INPUTS</span></span>

### <span data-ttu-id="6fd81-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6fd81-141">System.String</span></span>

### <span data-ttu-id="6fd81-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6fd81-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="6fd81-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fd81-143">OUTPUTS</span></span>

### <span data-ttu-id="6fd81-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6fd81-144">System.Boolean</span></span>

## <span data-ttu-id="6fd81-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="6fd81-145">NOTES</span></span>

## <span data-ttu-id="6fd81-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6fd81-146">RELATED LINKS</span></span>
