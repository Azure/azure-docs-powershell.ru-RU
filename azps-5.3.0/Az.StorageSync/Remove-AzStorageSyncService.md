---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: f64c085f742eeabea235660d4af7ba6bd5970fdf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517010"
---
# <span data-ttu-id="3e230-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3e230-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="3e230-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e230-102">SYNOPSIS</span></span>
<span data-ttu-id="3e230-103">Эта команда удалит указанную службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="3e230-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="3e230-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3e230-104">SYNTAX</span></span>

### <span data-ttu-id="3e230-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e230-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e230-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e230-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e230-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e230-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e230-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e230-108">DESCRIPTION</span></span>
<span data-ttu-id="3e230-109">Эта команда удалит указанную службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="3e230-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="3e230-110">Службу синхронизации хранилища можно удалить только в том случае, если сначала удаляются все содержащиеся в ней группы синхронизации и зарегистрированные серверы.</span><span class="sxs-lookup"><span data-stu-id="3e230-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="3e230-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3e230-111">EXAMPLES</span></span>

### <span data-ttu-id="3e230-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3e230-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="3e230-113">Эта команда удалит службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="3e230-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="3e230-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e230-114">PARAMETERS</span></span>

### <span data-ttu-id="3e230-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e230-115">-AsJob</span></span>
<span data-ttu-id="3e230-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3e230-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e230-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e230-117">-DefaultProfile</span></span>
<span data-ttu-id="3e230-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e230-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e230-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3e230-119">-Force</span></span>
<span data-ttu-id="3e230-120">Необходимо пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="3e230-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e230-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e230-121">-InputObject</span></span>
<span data-ttu-id="3e230-122">Объект ввода StorageSyncService, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="3e230-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e230-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3e230-123">-Name</span></span>
<span data-ttu-id="3e230-124">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="3e230-124">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e230-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e230-125">-PassThru</span></span>
<span data-ttu-id="3e230-126">В обычном выполнении этот cmdlet не возвращает никакого значения для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="3e230-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="3e230-127">Если задан параметр PassThru, то после успешного выполнения cmdlet напишет значение в конвейер.</span><span class="sxs-lookup"><span data-stu-id="3e230-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="3e230-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e230-128">-ResourceGroupName</span></span>
<span data-ttu-id="3e230-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3e230-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e230-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e230-130">-ResourceId</span></span>
<span data-ttu-id="3e230-131">ИД ресурса StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3e230-131">StorageSyncService Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e230-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e230-132">-Confirm</span></span>
<span data-ttu-id="3e230-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e230-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e230-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e230-134">-WhatIf</span></span>
<span data-ttu-id="3e230-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e230-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e230-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3e230-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e230-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e230-137">CommonParameters</span></span>
<span data-ttu-id="3e230-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e230-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e230-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e230-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e230-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e230-140">INPUTS</span></span>

### <span data-ttu-id="3e230-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3e230-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="3e230-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3e230-142">System.String</span></span>

### <span data-ttu-id="3e230-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3e230-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3e230-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3e230-144">OUTPUTS</span></span>

### <span data-ttu-id="3e230-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="3e230-145">System.Object</span></span>
## <span data-ttu-id="3e230-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3e230-146">NOTES</span></span>

## <span data-ttu-id="3e230-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e230-147">RELATED LINKS</span></span>
