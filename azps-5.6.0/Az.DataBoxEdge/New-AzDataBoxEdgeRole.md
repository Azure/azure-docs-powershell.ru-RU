---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: 0158116440ae7ffc1638ce08c6561e80ca034ae8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978616"
---
# <span data-ttu-id="4366f-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="4366f-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="4366f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4366f-102">SYNOPSIS</span></span>
<span data-ttu-id="4366f-103">Создает новую роль для устройства.</span><span class="sxs-lookup"><span data-stu-id="4366f-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="4366f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4366f-104">SYNTAX</span></span>

### <span data-ttu-id="4366f-105">ConnectionStringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4366f-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4366f-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="4366f-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4366f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4366f-107">DESCRIPTION</span></span>
<span data-ttu-id="4366f-108">Для **устройства Edge data Box** создается новая роль.</span><span class="sxs-lookup"><span data-stu-id="4366f-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="4366f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4366f-109">EXAMPLES</span></span>

### <span data-ttu-id="4366f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4366f-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="4366f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4366f-111">PARAMETERS</span></span>

### <span data-ttu-id="4366f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4366f-112">-AsJob</span></span>
<span data-ttu-id="4366f-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4366f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4366f-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="4366f-114">-ConnectionString</span></span>
<span data-ttu-id="4366f-115">Предоставление строк подключения</span><span class="sxs-lookup"><span data-stu-id="4366f-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="4366f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4366f-116">-DefaultProfile</span></span>
<span data-ttu-id="4366f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4366f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4366f-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4366f-118">-DeviceName</span></span>
<span data-ttu-id="4366f-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="4366f-119">Device Name</span></span>

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

### <span data-ttu-id="4366f-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="4366f-120">-DeviceProperty</span></span>
<span data-ttu-id="4366f-121">Предоставление свойств устройства</span><span class="sxs-lookup"><span data-stu-id="4366f-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="4366f-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="4366f-122">-EncryptionKey</span></span>
<span data-ttu-id="4366f-123">Ключ шифрования устройства Edge</span><span class="sxs-lookup"><span data-stu-id="4366f-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="4366f-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="4366f-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="4366f-125">Клавиша IOT-доступа устройства</span><span class="sxs-lookup"><span data-stu-id="4366f-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="4366f-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="4366f-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="4366f-127">Укажийте строку подключения устройства IOT</span><span class="sxs-lookup"><span data-stu-id="4366f-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="4366f-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="4366f-128">-IotDeviceId</span></span>
<span data-ttu-id="4366f-129">ИД устройства IOT</span><span class="sxs-lookup"><span data-stu-id="4366f-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="4366f-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="4366f-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="4366f-131">Клавиша доступа устройства Iot Edge</span><span class="sxs-lookup"><span data-stu-id="4366f-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="4366f-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="4366f-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="4366f-133">Укайте строку подключения устройства Edge</span><span class="sxs-lookup"><span data-stu-id="4366f-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="4366f-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="4366f-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="4366f-135">Id of the Iot Edge Device</span><span class="sxs-lookup"><span data-stu-id="4366f-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="4366f-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="4366f-136">-IotHostHub</span></span>
<span data-ttu-id="4366f-137">Адрес Hosthub</span><span class="sxs-lookup"><span data-stu-id="4366f-137">Hosthub address</span></span>

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

### <span data-ttu-id="4366f-138">-Name</span><span class="sxs-lookup"><span data-stu-id="4366f-138">-Name</span></span>
<span data-ttu-id="4366f-139">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="4366f-139">Resource Name</span></span>

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

### <span data-ttu-id="4366f-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="4366f-140">-Platform</span></span>
<span data-ttu-id="4366f-141">Предоформим платформу (например, Linux)</span><span class="sxs-lookup"><span data-stu-id="4366f-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="4366f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4366f-142">-ResourceGroupName</span></span>
<span data-ttu-id="4366f-143">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4366f-143">Resource Group Name</span></span>

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

### <span data-ttu-id="4366f-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="4366f-144">-RoleStatus</span></span>
<span data-ttu-id="4366f-145">Включить или отключить состояние</span><span class="sxs-lookup"><span data-stu-id="4366f-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="4366f-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4366f-146">-Confirm</span></span>
<span data-ttu-id="4366f-147">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4366f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4366f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4366f-148">-WhatIf</span></span>
<span data-ttu-id="4366f-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4366f-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4366f-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4366f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4366f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4366f-151">CommonParameters</span></span>
<span data-ttu-id="4366f-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4366f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4366f-153">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4366f-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4366f-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4366f-154">INPUTS</span></span>

### <span data-ttu-id="4366f-155">Нет</span><span class="sxs-lookup"><span data-stu-id="4366f-155">None</span></span>

## <span data-ttu-id="4366f-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4366f-156">OUTPUTS</span></span>

### <span data-ttu-id="4366f-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="4366f-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="4366f-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4366f-158">NOTES</span></span>

## <span data-ttu-id="4366f-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4366f-159">RELATED LINKS</span></span>
