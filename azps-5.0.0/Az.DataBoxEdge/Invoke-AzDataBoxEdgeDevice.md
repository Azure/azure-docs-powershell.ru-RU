---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 29bf8cf612d3569480c62784466879095ebcdb6e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314306"
---
# <span data-ttu-id="eed21-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="eed21-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="eed21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eed21-102">SYNOPSIS</span></span>
<span data-ttu-id="eed21-103">Вызывает определенные действия на устройстве.</span><span class="sxs-lookup"><span data-stu-id="eed21-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="eed21-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eed21-104">SYNTAX</span></span>

### <span data-ttu-id="eed21-105">InvokeScanForUpdateParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eed21-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eed21-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed21-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eed21-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed21-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eed21-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed21-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eed21-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed21-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eed21-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed21-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eed21-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed21-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eed21-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed21-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eed21-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed21-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eed21-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eed21-114">DESCRIPTION</span></span>
<span data-ttu-id="eed21-115">Командлет **Invoke-AzDataBoxEdgeDevice** вызывает действия для проверки, скачивания и установки обновлений на пограничном устройстве поля данных.</span><span class="sxs-lookup"><span data-stu-id="eed21-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="eed21-116">Функция автоматического сканирования запускается ежедневно на устройстве, и вы можете выполнить проверку явным образом, запустив этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eed21-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="eed21-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eed21-117">EXAMPLES</span></span>

### <span data-ttu-id="eed21-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eed21-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="eed21-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="eed21-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="eed21-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="eed21-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="eed21-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eed21-121">PARAMETERS</span></span>

### <span data-ttu-id="eed21-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eed21-122">-AsJob</span></span>
<span data-ttu-id="eed21-123">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="eed21-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eed21-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed21-124">-DefaultProfile</span></span>
<span data-ttu-id="eed21-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eed21-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eed21-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="eed21-126">-DeviceObject</span></span>
<span data-ttu-id="eed21-127">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="eed21-127">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="eed21-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="eed21-128">-FetchUpdate</span></span>
<span data-ttu-id="eed21-129">Загружает обновления на пограничном устройстве или шлюзе поля данных</span><span class="sxs-lookup"><span data-stu-id="eed21-129">Downloads the updates on a data box edge/gateway device</span></span>

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

### <span data-ttu-id="eed21-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="eed21-130">-InstallUpdate</span></span>
<span data-ttu-id="eed21-131">Установка обновлений на устройстве или шлюзе поля данных</span><span class="sxs-lookup"><span data-stu-id="eed21-131">Installs the updates on the data box edge/gateway device</span></span>

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

### <span data-ttu-id="eed21-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eed21-132">-Name</span></span>
<span data-ttu-id="eed21-133">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="eed21-133">Device Name</span></span>

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

### <span data-ttu-id="eed21-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eed21-134">-PassThru</span></span>
<span data-ttu-id="eed21-135">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="eed21-135">returns true if successful</span></span>

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

### <span data-ttu-id="eed21-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eed21-136">-ResourceGroupName</span></span>
<span data-ttu-id="eed21-137">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="eed21-137">Resource Group Name</span></span>

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

### <span data-ttu-id="eed21-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eed21-138">-ResourceId</span></span>
<span data-ttu-id="eed21-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="eed21-139">Azure ResourceId</span></span>

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

### <span data-ttu-id="eed21-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="eed21-140">-ScanForUpdate</span></span>
<span data-ttu-id="eed21-141">Поиск обновлений на пограничном устройстве или шлюзе поля данных.</span><span class="sxs-lookup"><span data-stu-id="eed21-141">Scans for updates on a data box edge/gateway device.</span></span>

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

### <span data-ttu-id="eed21-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eed21-142">-Confirm</span></span>
<span data-ttu-id="eed21-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eed21-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eed21-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eed21-144">-WhatIf</span></span>
<span data-ttu-id="eed21-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eed21-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eed21-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eed21-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eed21-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed21-147">CommonParameters</span></span>
<span data-ttu-id="eed21-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eed21-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed21-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eed21-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed21-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eed21-150">INPUTS</span></span>

### <span data-ttu-id="eed21-151">Ничего</span><span class="sxs-lookup"><span data-stu-id="eed21-151">None</span></span>

## <span data-ttu-id="eed21-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eed21-152">OUTPUTS</span></span>

### <span data-ttu-id="eed21-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eed21-153">System.Boolean</span></span>

## <span data-ttu-id="eed21-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="eed21-154">NOTES</span></span>

## <span data-ttu-id="eed21-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eed21-155">RELATED LINKS</span></span>
