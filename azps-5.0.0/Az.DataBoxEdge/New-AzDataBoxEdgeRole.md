---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: aa44399adcfd5e39d956215b7ca824e5ef9abd60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314279"
---
# <span data-ttu-id="47943-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="47943-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="47943-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47943-102">SYNOPSIS</span></span>
<span data-ttu-id="47943-103">Создание новой роли для устройства</span><span class="sxs-lookup"><span data-stu-id="47943-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="47943-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47943-104">SYNTAX</span></span>

### <span data-ttu-id="47943-105">ConnectionStringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="47943-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47943-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="47943-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47943-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47943-107">DESCRIPTION</span></span>
<span data-ttu-id="47943-108">Командлет **New-AzDataBoxEdgeRole** создает новую роль для устройства с полем данных EDGE.</span><span class="sxs-lookup"><span data-stu-id="47943-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="47943-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47943-109">EXAMPLES</span></span>

### <span data-ttu-id="47943-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="47943-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="47943-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47943-111">PARAMETERS</span></span>

### <span data-ttu-id="47943-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47943-112">-AsJob</span></span>
<span data-ttu-id="47943-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="47943-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47943-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="47943-114">-ConnectionString</span></span>
<span data-ttu-id="47943-115">Предоставление строк подключения</span><span class="sxs-lookup"><span data-stu-id="47943-115">To Provide Connection Strings</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47943-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47943-116">-DefaultProfile</span></span>
<span data-ttu-id="47943-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47943-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47943-118">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="47943-118">-DeviceName</span></span>
<span data-ttu-id="47943-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="47943-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47943-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="47943-120">-DeviceProperty</span></span>
<span data-ttu-id="47943-121">Предоставление свойств устройства</span><span class="sxs-lookup"><span data-stu-id="47943-121">To Provide Device Properties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IotParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47943-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="47943-122">-EncryptionKey</span></span>
<span data-ttu-id="47943-123">Ключ шифрования на пограничном устройстве</span><span class="sxs-lookup"><span data-stu-id="47943-123">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47943-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="47943-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="47943-125">Клавиша доступа для устройства IOT</span><span class="sxs-lookup"><span data-stu-id="47943-125">Iot Device Access Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47943-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="47943-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="47943-127">Укажите строку подключения для устройства IOT</span><span class="sxs-lookup"><span data-stu-id="47943-127">Please provide connection string of IOT Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47943-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="47943-128">-IotDeviceId</span></span>
<span data-ttu-id="47943-129">Код устройства для устройства IOT</span><span class="sxs-lookup"><span data-stu-id="47943-129">Device Id of the Iot Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47943-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="47943-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="47943-131">Клавиша доступа для устройства с EDGE в Интернет вещей</span><span class="sxs-lookup"><span data-stu-id="47943-131">Access key of the Iot Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47943-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="47943-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="47943-133">Укажите строку соединения с краевым устройством</span><span class="sxs-lookup"><span data-stu-id="47943-133">Please provide connection string of Edge Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47943-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="47943-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="47943-135">Идентификатор устройства EDGE в Интернет вещей</span><span class="sxs-lookup"><span data-stu-id="47943-135">Id of the Iot Edge Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47943-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="47943-136">-IotHostHub</span></span>
<span data-ttu-id="47943-137">Hosthub адрес</span><span class="sxs-lookup"><span data-stu-id="47943-137">Hosthub address</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47943-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="47943-138">-Name</span></span>
<span data-ttu-id="47943-139">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="47943-139">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47943-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="47943-140">-Platform</span></span>
<span data-ttu-id="47943-141">Предоставление платформы для ex: Linux</span><span class="sxs-lookup"><span data-stu-id="47943-141">Provide the Platform, for ex: Linux</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47943-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47943-142">-ResourceGroupName</span></span>
<span data-ttu-id="47943-143">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="47943-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47943-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="47943-144">-RoleStatus</span></span>
<span data-ttu-id="47943-145">Предоставление статуса включения и отключения</span><span class="sxs-lookup"><span data-stu-id="47943-145">Provide the status enable/disable</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47943-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47943-146">-Confirm</span></span>
<span data-ttu-id="47943-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="47943-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47943-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47943-148">-WhatIf</span></span>
<span data-ttu-id="47943-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="47943-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47943-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="47943-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47943-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47943-151">CommonParameters</span></span>
<span data-ttu-id="47943-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47943-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47943-153">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47943-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47943-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47943-154">INPUTS</span></span>

### <span data-ttu-id="47943-155">Ничего</span><span class="sxs-lookup"><span data-stu-id="47943-155">None</span></span>

## <span data-ttu-id="47943-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47943-156">OUTPUTS</span></span>

### <span data-ttu-id="47943-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="47943-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="47943-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="47943-158">NOTES</span></span>

## <span data-ttu-id="47943-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47943-159">RELATED LINKS</span></span>
