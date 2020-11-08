---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: eb695da1dc1fea238a57ea1c98bec42899e8f28f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236085"
---
# <span data-ttu-id="ff68a-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="ff68a-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="ff68a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff68a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff68a-103">Приостановка и прерывание подключения репликации на целевом томе</span><span class="sxs-lookup"><span data-stu-id="ff68a-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="ff68a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff68a-104">SYNTAX</span></span>

### <span data-ttu-id="ff68a-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff68a-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff68a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff68a-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff68a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff68a-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff68a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff68a-108">DESCRIPTION</span></span>
<span data-ttu-id="ff68a-109">Приостановка и прерывание подключения репликации на целевом томе</span><span class="sxs-lookup"><span data-stu-id="ff68a-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="ff68a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff68a-110">EXAMPLES</span></span>

### <span data-ttu-id="ff68a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ff68a-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="ff68a-112">Эта команда приостанавливает подключение репликации ANF на томе "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="ff68a-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="ff68a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff68a-113">PARAMETERS</span></span>

### <span data-ttu-id="ff68a-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="ff68a-114">-AccountName</span></span>
<span data-ttu-id="ff68a-115">Имя учетной записи ANF на томе репликации.</span><span class="sxs-lookup"><span data-stu-id="ff68a-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="ff68a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff68a-116">-DefaultProfile</span></span>
<span data-ttu-id="ff68a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff68a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff68a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff68a-118">-InputObject</span></span>
<span data-ttu-id="ff68a-119">Объект целевого тома ANF с репликацией, которую нужно прервать</span><span class="sxs-lookup"><span data-stu-id="ff68a-119">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="ff68a-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ff68a-120">-Name</span></span>
<span data-ttu-id="ff68a-121">Имя тома назначения репликации ANF</span><span class="sxs-lookup"><span data-stu-id="ff68a-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ff68a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff68a-122">-PassThru</span></span>
<span data-ttu-id="ff68a-123">Возвращает значение, указывающее, был ли выполнен перерыв для указанной репликации тома.</span><span class="sxs-lookup"><span data-stu-id="ff68a-123">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="ff68a-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ff68a-124">-PoolName</span></span>
<span data-ttu-id="ff68a-125">Имя пула ANF на томе репликации</span><span class="sxs-lookup"><span data-stu-id="ff68a-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="ff68a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff68a-126">-ResourceGroupName</span></span>
<span data-ttu-id="ff68a-127">Группа ресурсов целевого тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="ff68a-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ff68a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff68a-128">-ResourceId</span></span>
<span data-ttu-id="ff68a-129">Идентификатор ресурса целевого тома репликации ANF</span><span class="sxs-lookup"><span data-stu-id="ff68a-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ff68a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff68a-130">-Confirm</span></span>
<span data-ttu-id="ff68a-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ff68a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff68a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff68a-132">-WhatIf</span></span>
<span data-ttu-id="ff68a-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ff68a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff68a-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ff68a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff68a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff68a-135">CommonParameters</span></span>
<span data-ttu-id="ff68a-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff68a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff68a-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff68a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff68a-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff68a-138">INPUTS</span></span>

### <span data-ttu-id="ff68a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ff68a-139">System.String</span></span>

### <span data-ttu-id="ff68a-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ff68a-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ff68a-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff68a-141">OUTPUTS</span></span>

### <span data-ttu-id="ff68a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff68a-142">System.Boolean</span></span>

## <span data-ttu-id="ff68a-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff68a-143">NOTES</span></span>

## <span data-ttu-id="ff68a-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff68a-144">RELATED LINKS</span></span>
