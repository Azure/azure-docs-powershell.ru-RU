---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: eb695da1dc1fea238a57ea1c98bec42899e8f28f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318632"
---
# <span data-ttu-id="95da5-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="95da5-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="95da5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95da5-102">SYNOPSIS</span></span>
<span data-ttu-id="95da5-103">Приостановка и прерывание подключения репликации на целевом томе</span><span class="sxs-lookup"><span data-stu-id="95da5-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="95da5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95da5-104">SYNTAX</span></span>

### <span data-ttu-id="95da5-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95da5-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95da5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95da5-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95da5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95da5-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95da5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95da5-108">DESCRIPTION</span></span>
<span data-ttu-id="95da5-109">Приостановка и прерывание подключения репликации на целевом томе</span><span class="sxs-lookup"><span data-stu-id="95da5-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="95da5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95da5-110">EXAMPLES</span></span>

### <span data-ttu-id="95da5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="95da5-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="95da5-112">Эта команда приостанавливает подключение репликации ANF на томе "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="95da5-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="95da5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95da5-113">PARAMETERS</span></span>

### <span data-ttu-id="95da5-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="95da5-114">-AccountName</span></span>
<span data-ttu-id="95da5-115">Имя учетной записи ANF на томе репликации.</span><span class="sxs-lookup"><span data-stu-id="95da5-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="95da5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95da5-116">-DefaultProfile</span></span>
<span data-ttu-id="95da5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95da5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95da5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95da5-118">-InputObject</span></span>
<span data-ttu-id="95da5-119">Объект целевого тома ANF с репликацией, которую нужно прервать</span><span class="sxs-lookup"><span data-stu-id="95da5-119">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="95da5-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="95da5-120">-Name</span></span>
<span data-ttu-id="95da5-121">Имя тома назначения репликации ANF</span><span class="sxs-lookup"><span data-stu-id="95da5-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="95da5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95da5-122">-PassThru</span></span>
<span data-ttu-id="95da5-123">Возвращает значение, указывающее, был ли выполнен перерыв для указанной репликации тома.</span><span class="sxs-lookup"><span data-stu-id="95da5-123">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="95da5-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="95da5-124">-PoolName</span></span>
<span data-ttu-id="95da5-125">Имя пула ANF на томе репликации</span><span class="sxs-lookup"><span data-stu-id="95da5-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="95da5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95da5-126">-ResourceGroupName</span></span>
<span data-ttu-id="95da5-127">Группа ресурсов целевого тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="95da5-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="95da5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95da5-128">-ResourceId</span></span>
<span data-ttu-id="95da5-129">Идентификатор ресурса целевого тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="95da5-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="95da5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95da5-130">-Confirm</span></span>
<span data-ttu-id="95da5-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="95da5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95da5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95da5-132">-WhatIf</span></span>
<span data-ttu-id="95da5-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="95da5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95da5-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="95da5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95da5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95da5-135">CommonParameters</span></span>
<span data-ttu-id="95da5-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95da5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95da5-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95da5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95da5-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95da5-138">INPUTS</span></span>

### <span data-ttu-id="95da5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="95da5-139">System.String</span></span>

### <span data-ttu-id="95da5-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="95da5-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="95da5-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95da5-141">OUTPUTS</span></span>

### <span data-ttu-id="95da5-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95da5-142">System.Boolean</span></span>

## <span data-ttu-id="95da5-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="95da5-143">NOTES</span></span>

## <span data-ttu-id="95da5-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95da5-144">RELATED LINKS</span></span>
