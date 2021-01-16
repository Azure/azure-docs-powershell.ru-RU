---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 1be2aa8e198ae096f445b9f1972d1e0b903ae729
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399127"
---
# <span data-ttu-id="78e9e-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="78e9e-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="78e9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="78e9e-103">Создает новое центральное приложение IoT.</span><span class="sxs-lookup"><span data-stu-id="78e9e-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="78e9e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="78e9e-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78e9e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78e9e-105">DESCRIPTION</span></span>
<span data-ttu-id="78e9e-106">Создает новое центральное приложение IoT с предоставленными свойствами и метаданными.</span><span class="sxs-lookup"><span data-stu-id="78e9e-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="78e9e-107">Введение в IoT Central https://docs.microsoft.com/en-us/azure/iot-central/ см. в .</span><span class="sxs-lookup"><span data-stu-id="78e9e-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="78e9e-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="78e9e-108">EXAMPLES</span></span>

### <span data-ttu-id="78e9e-109">Пример 1. Создание простого центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="78e9e-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="78e9e-110">Пример выходных данных:</span><span class="sxs-lookup"><span data-stu-id="78e9e-110">Example Output:</span></span>

<span data-ttu-id="78e9e-111">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX DisplayName : MyAppResourceName Subdomain : MyAppSubdomain Template iotc-default@1.0.0 : SubscriptionId : XXXXXXX-XXXX-XXXX-XXXXX-XXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78e9e-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="78e9e-112">Создайте центральное приложение IoT в стандартном уровне цен ST2 в регионе группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78e9e-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="78e9e-113">Пример 2. Создание простого центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="78e9e-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="78e9e-114">Пример выходных данных:</span><span class="sxs-lookup"><span data-stu-id="78e9e-114">Example Output:</span></span>

<span data-ttu-id="78e9e-115">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain Template iotc-default@1.0.0 : SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXX-XXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78e9e-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="78e9e-116">Создайте центральное приложение IoT со стандартным уровнем цен ST2 в регионе "запад" с настраиваемой отображаемой именем, основанным на шаблоне iotc-default.</span><span class="sxs-lookup"><span data-stu-id="78e9e-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="78e9e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78e9e-117">PARAMETERS</span></span>

### <span data-ttu-id="78e9e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78e9e-118">-AsJob</span></span>
<span data-ttu-id="78e9e-119">Запуск cmdlet в качестве задания в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="78e9e-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="78e9e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78e9e-120">-DefaultProfile</span></span>
<span data-ttu-id="78e9e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78e9e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78e9e-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="78e9e-122">-DisplayName</span></span>
<span data-ttu-id="78e9e-123">Пользовательское отображаемая имя центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="78e9e-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="78e9e-124">Значение по умолчанию — название ресурса.</span><span class="sxs-lookup"><span data-stu-id="78e9e-124">Default is resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e9e-125">-Location</span><span class="sxs-lookup"><span data-stu-id="78e9e-125">-Location</span></span>
<span data-ttu-id="78e9e-126">Расположение центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="78e9e-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="78e9e-127">По умолчанию это расположение целевой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78e9e-127">Default is the location of target resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e9e-128">-Name</span><span class="sxs-lookup"><span data-stu-id="78e9e-128">-Name</span></span>
<span data-ttu-id="78e9e-129">Имя центрального ресурса приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="78e9e-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="78e9e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78e9e-130">-ResourceGroupName</span></span>
<span data-ttu-id="78e9e-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78e9e-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="78e9e-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="78e9e-132">-Sku</span></span>
<span data-ttu-id="78e9e-133">Уровень цен для центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="78e9e-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="78e9e-134">Значение по умолчанию — ST2.</span><span class="sxs-lookup"><span data-stu-id="78e9e-134">Default value is ST2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e9e-135">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="78e9e-135">-Subdomain</span></span>
<span data-ttu-id="78e9e-136">Поддомен для URL-адреса IoT Central.</span><span class="sxs-lookup"><span data-stu-id="78e9e-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="78e9e-137">У каждого приложения должен быть уникальный поддомен.</span><span class="sxs-lookup"><span data-stu-id="78e9e-137">Each application must have a unique subdomain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e9e-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="78e9e-138">-Tag</span></span>
<span data-ttu-id="78e9e-139">Теги ресурсов центрального приложения.</span><span class="sxs-lookup"><span data-stu-id="78e9e-139">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e9e-140">-Template</span><span class="sxs-lookup"><span data-stu-id="78e9e-140">-Template</span></span>
<span data-ttu-id="78e9e-141">Имя шаблона центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="78e9e-141">IoT Central application template name.</span></span>
<span data-ttu-id="78e9e-142">По умолчанию это пользовательское приложение.</span><span class="sxs-lookup"><span data-stu-id="78e9e-142">Default is a custom application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e9e-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78e9e-143">-Confirm</span></span>
<span data-ttu-id="78e9e-144">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78e9e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78e9e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78e9e-145">-WhatIf</span></span>
<span data-ttu-id="78e9e-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78e9e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78e9e-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="78e9e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78e9e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78e9e-148">CommonParameters</span></span>
<span data-ttu-id="78e9e-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78e9e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78e9e-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78e9e-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78e9e-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78e9e-151">INPUTS</span></span>

### <span data-ttu-id="78e9e-152">System.String</span><span class="sxs-lookup"><span data-stu-id="78e9e-152">System.String</span></span>

### <span data-ttu-id="78e9e-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="78e9e-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="78e9e-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="78e9e-154">OUTPUTS</span></span>

### <span data-ttu-id="78e9e-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="78e9e-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="78e9e-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="78e9e-156">NOTES</span></span>

## <span data-ttu-id="78e9e-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78e9e-157">RELATED LINKS</span></span>
