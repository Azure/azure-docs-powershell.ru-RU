---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078958"
---
# <span data-ttu-id="6b857-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="6b857-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="6b857-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b857-102">SYNOPSIS</span></span>
<span data-ttu-id="6b857-103">Возобновите или синхронизируйте подключение на целевом томе.</span><span class="sxs-lookup"><span data-stu-id="6b857-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="6b857-104">Если операция выполняется на исходном томе, будет выполнена обратная синхронизация подключения и синхронизация из источника в конечную точку.</span><span class="sxs-lookup"><span data-stu-id="6b857-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="6b857-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b857-105">SYNTAX</span></span>

### <span data-ttu-id="6b857-106">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6b857-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b857-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b857-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b857-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b857-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b857-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b857-109">DESCRIPTION</span></span>
<span data-ttu-id="6b857-110">Возобновление или повторная синхронизация подключения на целевом томе</span><span class="sxs-lookup"><span data-stu-id="6b857-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="6b857-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b857-111">EXAMPLES</span></span>

### <span data-ttu-id="6b857-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6b857-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="6b857-113">Эта команда возобновляет подключение репликации ANF на томе "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="6b857-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="6b857-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b857-114">PARAMETERS</span></span>

### <span data-ttu-id="6b857-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="6b857-115">-AccountName</span></span>
<span data-ttu-id="6b857-116">Имя учетной записи ANF на томе репликации.</span><span class="sxs-lookup"><span data-stu-id="6b857-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="6b857-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b857-117">-DefaultProfile</span></span>
<span data-ttu-id="6b857-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b857-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b857-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b857-119">-InputObject</span></span>
<span data-ttu-id="6b857-120">Объект целевого тома репликации ANF для повторной синхронизации</span><span class="sxs-lookup"><span data-stu-id="6b857-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="6b857-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6b857-121">-Name</span></span>
<span data-ttu-id="6b857-122">Имя тома назначения репликации ANF</span><span class="sxs-lookup"><span data-stu-id="6b857-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="6b857-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b857-123">-PassThru</span></span>
<span data-ttu-id="6b857-124">Возвращает значение, указывающее, была ли выполнена повторная синхронизация указанного тома репликации</span><span class="sxs-lookup"><span data-stu-id="6b857-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="6b857-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="6b857-125">-PoolName</span></span>
<span data-ttu-id="6b857-126">Имя пула ANF на томе репликации</span><span class="sxs-lookup"><span data-stu-id="6b857-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="6b857-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b857-127">-ResourceGroupName</span></span>
<span data-ttu-id="6b857-128">Группа ресурсов целевого тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="6b857-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="6b857-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b857-129">-ResourceId</span></span>
<span data-ttu-id="6b857-130">Идентификатор ресурса целевого тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="6b857-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="6b857-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b857-131">-Confirm</span></span>
<span data-ttu-id="6b857-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6b857-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b857-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b857-133">-WhatIf</span></span>
<span data-ttu-id="6b857-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6b857-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b857-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6b857-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b857-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b857-136">CommonParameters</span></span>
<span data-ttu-id="6b857-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b857-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b857-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b857-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b857-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b857-139">INPUTS</span></span>

### <span data-ttu-id="6b857-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6b857-140">System.String</span></span>

### <span data-ttu-id="6b857-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6b857-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="6b857-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b857-142">OUTPUTS</span></span>

### <span data-ttu-id="6b857-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b857-143">System.Boolean</span></span>

## <span data-ttu-id="6b857-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b857-144">NOTES</span></span>

## <span data-ttu-id="6b857-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b857-145">RELATED LINKS</span></span>
