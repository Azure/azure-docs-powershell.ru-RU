---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: 5116ead7111902b1009517ff42ff6594ac87d8c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728475"
---
# <span data-ttu-id="e1054-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="e1054-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="e1054-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1054-102">SYNOPSIS</span></span>
<span data-ttu-id="e1054-103">Эта команда удалит указанную службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="e1054-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="e1054-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1054-104">SYNTAX</span></span>

### <span data-ttu-id="e1054-105">InputObjectParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e1054-105">InputObjectParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1054-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1054-106">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1054-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1054-107">StringParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1054-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1054-108">DESCRIPTION</span></span>
<span data-ttu-id="e1054-109">Эта команда удалит указанную службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="e1054-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="e1054-110">Службу синхронизации хранилища можно удалить только в том случае, если все содержащиеся в ней группы синхронизации и зарегистрированные серверы будут удалены.</span><span class="sxs-lookup"><span data-stu-id="e1054-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="e1054-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1054-111">EXAMPLES</span></span>

### <span data-ttu-id="e1054-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e1054-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="e1054-113">Эта команда удалит службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="e1054-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="e1054-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1054-114">PARAMETERS</span></span>

### <span data-ttu-id="e1054-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1054-115">-AsJob</span></span>
<span data-ttu-id="e1054-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e1054-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1054-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1054-117">-DefaultProfile</span></span>
<span data-ttu-id="e1054-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1054-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1054-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e1054-119">-Force</span></span>
<span data-ttu-id="e1054-120">Укажите, чтобы пропустить подтверждение этой команды.</span><span class="sxs-lookup"><span data-stu-id="e1054-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="e1054-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1054-121">-InputObject</span></span>
<span data-ttu-id="e1054-122">Входной объект StorageSyncService, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="e1054-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="e1054-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e1054-123">-Name</span></span>
<span data-ttu-id="e1054-124">Имя StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="e1054-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="e1054-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1054-125">-PassThru</span></span>
<span data-ttu-id="e1054-126">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="e1054-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e1054-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1054-127">-ResourceGroupName</span></span>
<span data-ttu-id="e1054-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e1054-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="e1054-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1054-129">-ResourceId</span></span>
<span data-ttu-id="e1054-130">Идентификатор ресурса StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="e1054-130">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="e1054-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1054-131">-Confirm</span></span>
<span data-ttu-id="e1054-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e1054-132">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1054-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1054-133">-WhatIf</span></span>
<span data-ttu-id="e1054-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e1054-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1054-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e1054-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1054-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1054-136">CommonParameters</span></span>
<span data-ttu-id="e1054-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1054-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1054-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1054-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1054-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1054-139">INPUTS</span></span>

### <span data-ttu-id="e1054-140">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="e1054-140">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="e1054-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e1054-141">System.String</span></span>

### <span data-ttu-id="e1054-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e1054-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e1054-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1054-143">OUTPUTS</span></span>

### <span data-ttu-id="e1054-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="e1054-144">System.Object</span></span>
## <span data-ttu-id="e1054-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1054-145">NOTES</span></span>

## <span data-ttu-id="e1054-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1054-146">RELATED LINKS</span></span>
