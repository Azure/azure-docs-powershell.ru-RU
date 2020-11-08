---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: f25aeb501ff046a25330ad5db47bbdb06fbe7b35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236559"
---
# <span data-ttu-id="d0947-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d0947-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="d0947-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0947-102">SYNOPSIS</span></span>
<span data-ttu-id="d0947-103">Вызывает определенные действия на устройстве.</span><span class="sxs-lookup"><span data-stu-id="d0947-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="d0947-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0947-104">SYNTAX</span></span>

### <span data-ttu-id="d0947-105">InvokeScanForUpdateParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d0947-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0947-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0947-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0947-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0947-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0947-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0947-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0947-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0947-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0947-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0947-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0947-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0947-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0947-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0947-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0947-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0947-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0947-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0947-114">DESCRIPTION</span></span>
<span data-ttu-id="d0947-115">Командлет **Invoke-AzStackEdgeDevice** вызывает действия для проверки, скачивания и установки обновлений на пограничном устройстве стека.</span><span class="sxs-lookup"><span data-stu-id="d0947-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="d0947-116">Функция автоматического сканирования запускается ежедневно на устройстве, и вы можете выполнить проверку явным образом, запустив этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d0947-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="d0947-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0947-117">EXAMPLES</span></span>

### <span data-ttu-id="d0947-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d0947-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="d0947-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d0947-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="d0947-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d0947-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="d0947-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0947-121">PARAMETERS</span></span>

### <span data-ttu-id="d0947-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0947-122">-AsJob</span></span>
<span data-ttu-id="d0947-123">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d0947-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0947-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0947-124">-DefaultProfile</span></span>
<span data-ttu-id="d0947-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0947-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0947-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="d0947-126">-DeviceObject</span></span>
<span data-ttu-id="d0947-127">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="d0947-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0947-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="d0947-128">-FetchUpdate</span></span>
<span data-ttu-id="d0947-129">Загружает обновления на пограничном устройстве или шлюзе с стеком</span><span class="sxs-lookup"><span data-stu-id="d0947-129">Downloads the updates on a Stack edge/gateway device</span></span>

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

### <span data-ttu-id="d0947-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="d0947-130">-InstallUpdate</span></span>
<span data-ttu-id="d0947-131">Установка обновлений на пограничном устройстве с интерфейсом Edge/Gateway</span><span class="sxs-lookup"><span data-stu-id="d0947-131">Installs the updates on the Stack edge/gateway device</span></span>

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

### <span data-ttu-id="d0947-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d0947-132">-Name</span></span>
<span data-ttu-id="d0947-133">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="d0947-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0947-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0947-134">-PassThru</span></span>
<span data-ttu-id="d0947-135">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="d0947-135">returns true if successful</span></span>

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

### <span data-ttu-id="d0947-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0947-136">-ResourceGroupName</span></span>
<span data-ttu-id="d0947-137">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d0947-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0947-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0947-138">-ResourceId</span></span>
<span data-ttu-id="d0947-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0947-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0947-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="d0947-140">-ScanForUpdate</span></span>
<span data-ttu-id="d0947-141">Проверка наличия обновлений на пограничном устройстве/шлюзе стека.</span><span class="sxs-lookup"><span data-stu-id="d0947-141">Scans for updates on a Stack edge/gateway device.</span></span>

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

### <span data-ttu-id="d0947-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0947-142">-Confirm</span></span>
<span data-ttu-id="d0947-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d0947-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0947-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0947-144">-WhatIf</span></span>
<span data-ttu-id="d0947-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d0947-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0947-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d0947-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0947-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0947-147">CommonParameters</span></span>
<span data-ttu-id="d0947-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0947-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0947-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0947-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0947-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0947-150">INPUTS</span></span>

### <span data-ttu-id="d0947-151">Ничего</span><span class="sxs-lookup"><span data-stu-id="d0947-151">None</span></span>

## <span data-ttu-id="d0947-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0947-152">OUTPUTS</span></span>

### <span data-ttu-id="d0947-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0947-153">System.Boolean</span></span>

## <span data-ttu-id="d0947-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0947-154">NOTES</span></span>

## <span data-ttu-id="d0947-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0947-155">RELATED LINKS</span></span>