---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: b045fc775c16df71cce05d08ca8fe8a23e10c039
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907582"
---
# <span data-ttu-id="220d9-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="220d9-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="220d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="220d9-102">SYNOPSIS</span></span>
<span data-ttu-id="220d9-103">Эта команда удалит указанную службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="220d9-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="220d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="220d9-104">SYNTAX</span></span>

### <span data-ttu-id="220d9-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="220d9-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="220d9-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="220d9-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="220d9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="220d9-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="220d9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="220d9-108">DESCRIPTION</span></span>
<span data-ttu-id="220d9-109">Эта команда удалит указанную службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="220d9-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="220d9-110">Службу синхронизации хранилища можно удалить только в том случае, если все содержащиеся в ней группы синхронизации и зарегистрированные серверы будут удалены.</span><span class="sxs-lookup"><span data-stu-id="220d9-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="220d9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="220d9-111">EXAMPLES</span></span>

### <span data-ttu-id="220d9-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="220d9-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="220d9-113">Эта команда удалит службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="220d9-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="220d9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="220d9-114">PARAMETERS</span></span>

### <span data-ttu-id="220d9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="220d9-115">-AsJob</span></span>
<span data-ttu-id="220d9-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="220d9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="220d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="220d9-117">-DefaultProfile</span></span>
<span data-ttu-id="220d9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="220d9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="220d9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="220d9-119">-Force</span></span>
<span data-ttu-id="220d9-120">Укажите, чтобы пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="220d9-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="220d9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="220d9-121">-InputObject</span></span>
<span data-ttu-id="220d9-122">Входной объект StorageSyncService, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="220d9-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="220d9-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="220d9-123">-Name</span></span>
<span data-ttu-id="220d9-124">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="220d9-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="220d9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="220d9-125">-PassThru</span></span>
<span data-ttu-id="220d9-126">При нормальном выполнении этот командлет не возвращает значение в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="220d9-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="220d9-127">Если вы предоставляете параметр PassThru, командлет запишет значение в конвейер после успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="220d9-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="220d9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="220d9-128">-ResourceGroupName</span></span>
<span data-ttu-id="220d9-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="220d9-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="220d9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="220d9-130">-ResourceId</span></span>
<span data-ttu-id="220d9-131">Идентификатор ресурса StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="220d9-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="220d9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="220d9-132">-Confirm</span></span>
<span data-ttu-id="220d9-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="220d9-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="220d9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="220d9-134">-WhatIf</span></span>
<span data-ttu-id="220d9-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="220d9-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="220d9-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="220d9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="220d9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="220d9-137">CommonParameters</span></span>
<span data-ttu-id="220d9-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="220d9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="220d9-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="220d9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="220d9-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="220d9-140">INPUTS</span></span>

### <span data-ttu-id="220d9-141">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="220d9-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="220d9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="220d9-142">System.String</span></span>

### <span data-ttu-id="220d9-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="220d9-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="220d9-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="220d9-144">OUTPUTS</span></span>

### <span data-ttu-id="220d9-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="220d9-145">System.Object</span></span>
## <span data-ttu-id="220d9-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="220d9-146">NOTES</span></span>

## <span data-ttu-id="220d9-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="220d9-147">RELATED LINKS</span></span>
