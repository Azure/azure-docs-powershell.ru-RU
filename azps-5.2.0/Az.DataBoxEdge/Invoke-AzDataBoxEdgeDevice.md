---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 29bf8cf612d3569480c62784466879095ebcdb6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408436"
---
# <span data-ttu-id="88737-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="88737-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="88737-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88737-102">SYNOPSIS</span></span>
<span data-ttu-id="88737-103">Вызывает определенные действия на устройстве.</span><span class="sxs-lookup"><span data-stu-id="88737-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="88737-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="88737-104">SYNTAX</span></span>

### <span data-ttu-id="88737-105">InvokeScanForUpdateParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88737-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88737-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88737-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88737-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88737-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88737-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88737-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88737-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="88737-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88737-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="88737-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88737-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88737-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88737-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88737-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88737-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88737-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88737-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88737-114">DESCRIPTION</span></span>
<span data-ttu-id="88737-115">**Cmdlet Invoke-AzDataBoxEdgeDevice** вызывает действия для сканирования, скачивания и установки обновлений на устройстве Edge Data Box.</span><span class="sxs-lookup"><span data-stu-id="88737-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="88737-116">На устройстве ежедневно выполняется автоматическое сканирование, которое можно активировать явным образом с помощью этого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88737-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="88737-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="88737-117">EXAMPLES</span></span>

### <span data-ttu-id="88737-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88737-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="88737-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="88737-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="88737-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="88737-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="88737-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88737-121">PARAMETERS</span></span>

### <span data-ttu-id="88737-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88737-122">-AsJob</span></span>
<span data-ttu-id="88737-123">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="88737-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88737-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88737-124">-DefaultProfile</span></span>
<span data-ttu-id="88737-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88737-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88737-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="88737-126">-DeviceObject</span></span>
<span data-ttu-id="88737-127">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="88737-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88737-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="88737-128">-FetchUpdate</span></span>
<span data-ttu-id="88737-129">Скачивает обновления на устройстве с полем данных или шлюзом.</span><span class="sxs-lookup"><span data-stu-id="88737-129">Downloads the updates on a data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeFetchUpdateParameterSet, InvokeFetchUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88737-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="88737-130">-InstallUpdate</span></span>
<span data-ttu-id="88737-131">Устанавливает обновления на устройстве с полем данных или шлюзом.</span><span class="sxs-lookup"><span data-stu-id="88737-131">Installs the updates on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeInstallUpdatesByResourceIdParameterSet, InvokeInstallUpdateParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88737-132">-Name</span><span class="sxs-lookup"><span data-stu-id="88737-132">-Name</span></span>
<span data-ttu-id="88737-133">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="88737-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88737-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88737-134">-PassThru</span></span>
<span data-ttu-id="88737-135">Возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="88737-135">returns true if successful</span></span>

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

### <span data-ttu-id="88737-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88737-136">-ResourceGroupName</span></span>
<span data-ttu-id="88737-137">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="88737-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88737-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88737-138">-ResourceId</span></span>
<span data-ttu-id="88737-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="88737-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88737-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="88737-140">-ScanForUpdate</span></span>
<span data-ttu-id="88737-141">Проверяет, нет ли обновлений на устройстве с полем данных или шлюзом.</span><span class="sxs-lookup"><span data-stu-id="88737-141">Scans for updates on a data box edge/gateway device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeScanForUpdateByResourceIdParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88737-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88737-142">-Confirm</span></span>
<span data-ttu-id="88737-143">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88737-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88737-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88737-144">-WhatIf</span></span>
<span data-ttu-id="88737-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88737-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88737-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="88737-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88737-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88737-147">CommonParameters</span></span>
<span data-ttu-id="88737-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88737-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88737-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88737-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88737-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88737-150">INPUTS</span></span>

### <span data-ttu-id="88737-151">Нет</span><span class="sxs-lookup"><span data-stu-id="88737-151">None</span></span>

## <span data-ttu-id="88737-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="88737-152">OUTPUTS</span></span>

### <span data-ttu-id="88737-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="88737-153">System.Boolean</span></span>

## <span data-ttu-id="88737-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="88737-154">NOTES</span></span>

## <span data-ttu-id="88737-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88737-155">RELATED LINKS</span></span>
