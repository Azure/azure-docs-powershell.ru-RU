---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: 648ef711d030f7600863d286df24cfdf1d2f7927
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974019"
---
# <span data-ttu-id="f005a-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f005a-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="f005a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f005a-102">SYNOPSIS</span></span>
<span data-ttu-id="f005a-103">Эта команда удалит указанную службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="f005a-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="f005a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f005a-104">SYNTAX</span></span>

### <span data-ttu-id="f005a-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f005a-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f005a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f005a-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f005a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f005a-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f005a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f005a-108">DESCRIPTION</span></span>
<span data-ttu-id="f005a-109">Эта команда удалит указанную службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="f005a-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="f005a-110">Службу синхронизации хранилища можно удалить только в том случае, если сначала удаляются все содержащиеся в ней группы синхронизации и зарегистрированные серверы.</span><span class="sxs-lookup"><span data-stu-id="f005a-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="f005a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f005a-111">EXAMPLES</span></span>

### <span data-ttu-id="f005a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f005a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="f005a-113">Эта команда удалит службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="f005a-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="f005a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f005a-114">PARAMETERS</span></span>

### <span data-ttu-id="f005a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f005a-115">-AsJob</span></span>
<span data-ttu-id="f005a-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f005a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f005a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f005a-117">-DefaultProfile</span></span>
<span data-ttu-id="f005a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f005a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f005a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f005a-119">-Force</span></span>
<span data-ttu-id="f005a-120">Необходимо пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="f005a-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="f005a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f005a-121">-InputObject</span></span>
<span data-ttu-id="f005a-122">Объект ввода StorageSyncService, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="f005a-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="f005a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f005a-123">-Name</span></span>
<span data-ttu-id="f005a-124">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="f005a-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="f005a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f005a-125">-PassThru</span></span>
<span data-ttu-id="f005a-126">В обычном выполнении этот cmdlet не возвращает никакого значения для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="f005a-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="f005a-127">Если задан параметр PassThru, то после успешного выполнения cmdlet напишет значение в конвейер.</span><span class="sxs-lookup"><span data-stu-id="f005a-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="f005a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f005a-128">-ResourceGroupName</span></span>
<span data-ttu-id="f005a-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f005a-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="f005a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f005a-130">-ResourceId</span></span>
<span data-ttu-id="f005a-131">ИД ресурса StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f005a-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="f005a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f005a-132">-Confirm</span></span>
<span data-ttu-id="f005a-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f005a-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f005a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f005a-134">-WhatIf</span></span>
<span data-ttu-id="f005a-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f005a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f005a-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f005a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f005a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f005a-137">CommonParameters</span></span>
<span data-ttu-id="f005a-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f005a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f005a-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f005a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f005a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f005a-140">INPUTS</span></span>

### <span data-ttu-id="f005a-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f005a-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="f005a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f005a-142">System.String</span></span>

### <span data-ttu-id="f005a-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f005a-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f005a-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f005a-144">OUTPUTS</span></span>

### <span data-ttu-id="f005a-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="f005a-145">System.Object</span></span>
## <span data-ttu-id="f005a-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f005a-146">NOTES</span></span>

## <span data-ttu-id="f005a-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f005a-147">RELATED LINKS</span></span>
