---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
ms.openlocfilehash: d7e8c65a54adae1de7b7f3ba1ed2d67139638846
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235257"
---
# <span data-ttu-id="b3e63-101">Invoke-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b3e63-101">Invoke-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="b3e63-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3e63-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e63-103">Вызывает определенные действия в контейнере хранилища.</span><span class="sxs-lookup"><span data-stu-id="b3e63-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="b3e63-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3e63-104">SYNTAX</span></span>

### <span data-ttu-id="b3e63-105">InvokeByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3e63-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3e63-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3e63-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3e63-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3e63-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3e63-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3e63-108">DESCRIPTION</span></span>
<span data-ttu-id="b3e63-109">Командлет **Invoke-AzStackEdgeStorageContainer** вызывает действия для обновления данных в контейнере хранилища на пограничном устройстве стека.</span><span class="sxs-lookup"><span data-stu-id="b3e63-109">The **Invoke-AzStackEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Stack Edge device.</span></span> 

## <span data-ttu-id="b3e63-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3e63-110">EXAMPLES</span></span>

### <span data-ttu-id="b3e63-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b3e63-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="b3e63-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b3e63-112">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzStackEdgeStorageContainer
```

## <span data-ttu-id="b3e63-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3e63-113">PARAMETERS</span></span>

### <span data-ttu-id="b3e63-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3e63-114">-AsJob</span></span>
<span data-ttu-id="b3e63-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b3e63-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3e63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e63-116">-DefaultProfile</span></span>
<span data-ttu-id="b3e63-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3e63-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3e63-118">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="b3e63-118">-DeviceName</span></span>
<span data-ttu-id="b3e63-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="b3e63-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e63-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b3e63-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="b3e63-121">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="b3e63-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e63-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3e63-122">-InputObject</span></span>
<span data-ttu-id="b3e63-123">Предоставить существующий объект EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3e63-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e63-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b3e63-124">-Name</span></span>
<span data-ttu-id="b3e63-125">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="b3e63-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e63-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3e63-126">-PassThru</span></span>
<span data-ttu-id="b3e63-127">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="b3e63-127">returns true if successful</span></span>

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

### <span data-ttu-id="b3e63-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="b3e63-128">-RefreshData</span></span>
<span data-ttu-id="b3e63-129">Обновление метаданных контейнера с использованием данных из облака</span><span class="sxs-lookup"><span data-stu-id="b3e63-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="b3e63-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3e63-130">-ResourceGroupName</span></span>
<span data-ttu-id="b3e63-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b3e63-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e63-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3e63-132">-ResourceId</span></span>
<span data-ttu-id="b3e63-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3e63-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e63-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3e63-134">-Confirm</span></span>
<span data-ttu-id="b3e63-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b3e63-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3e63-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3e63-136">-WhatIf</span></span>
<span data-ttu-id="b3e63-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b3e63-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3e63-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b3e63-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3e63-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e63-139">CommonParameters</span></span>
<span data-ttu-id="b3e63-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3e63-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e63-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3e63-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e63-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3e63-142">INPUTS</span></span>

### <span data-ttu-id="b3e63-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b3e63-143">System.String</span></span>

### <span data-ttu-id="b3e63-144">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b3e63-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="b3e63-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3e63-145">OUTPUTS</span></span>

### <span data-ttu-id="b3e63-146">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b3e63-146">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="b3e63-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3e63-147">NOTES</span></span>

## <span data-ttu-id="b3e63-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3e63-148">RELATED LINKS</span></span>
