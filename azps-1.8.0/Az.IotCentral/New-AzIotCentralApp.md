---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 636c40763c69a4c39ca0bbf8b15fe04fad318d84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900402"
---
# <span data-ttu-id="f6ff9-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="f6ff9-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="f6ff9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="f6ff9-103">Создание центра администрирования Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="f6ff9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6ff9-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6ff9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6ff9-105">DESCRIPTION</span></span>
<span data-ttu-id="f6ff9-106">Создает новое приложение центра администрирования Интернет вещей с предоставленными свойствами и метаданными.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="f6ff9-107">Общие сведения о центре Интернета вещей можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="f6ff9-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="f6ff9-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6ff9-108">EXAMPLES</span></span>

### <span data-ttu-id="f6ff9-109">Пример 1. Создайте простое центральное приложение IoT.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="f6ff9-110">Пример вывода:</span><span class="sxs-lookup"><span data-stu-id="f6ff9-110">Example Output:</span></span>

<span data-ttu-id="f6ff9-111">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName имя: MyAppResourceName тип: Microsoft. IoTCentral/IoTApps расположение: westus тег: SKU: Microsoft. Azure., IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: MyAppResourceName поддомен: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6ff9-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="f6ff9-112">Создавайте центральное приложение IoT на стандартной ценовой категории S1 в области группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-112">Create an IoT Central application in the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="f6ff9-113">Пример 2. Создайте простое центральное приложение IoT.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "S1" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="f6ff9-114">Пример вывода:</span><span class="sxs-lookup"><span data-stu-id="f6ff9-114">Example Output:</span></span>

<span data-ttu-id="f6ff9-115">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName имя: MyAppResourceName тип: Microsoft. IoTCentral/IoTApps расположение: westus Tag: SKU: Microsoft. Azure. Commands. IotCentral. Models. ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My My имя домена: PSIotCentralAppSkuInfo Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX MyAppSubdomain: ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6ff9-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="f6ff9-116">Создавайте центральное приложение IoT с помощью стандартной ценовой категории S1 в области "westus" с настраиваемым отображаемым именем на основе шаблона IOTC-Default.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-116">Create an IoT Central application with the standard pricing tier S1 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="f6ff9-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6ff9-117">PARAMETERS</span></span>

### <span data-ttu-id="f6ff9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6ff9-118">-AsJob</span></span>
<span data-ttu-id="f6ff9-119">Запустите командлет как задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="f6ff9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6ff9-120">-DefaultProfile</span></span>
<span data-ttu-id="f6ff9-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6ff9-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f6ff9-122">-DisplayName</span></span>
<span data-ttu-id="f6ff9-123">Настраиваемое отображаемое имя центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="f6ff9-124">По умолчанию — имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-124">Default is resource name.</span></span>

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

### <span data-ttu-id="f6ff9-125">-Location</span><span class="sxs-lookup"><span data-stu-id="f6ff9-125">-Location</span></span>
<span data-ttu-id="f6ff9-126">Расположение центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="f6ff9-127">По умолчанию — расположение целевой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-127">Default is the location of target resource group.</span></span>

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

### <span data-ttu-id="f6ff9-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6ff9-128">-Name</span></span>
<span data-ttu-id="f6ff9-129">Имя ресурса центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="f6ff9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6ff9-130">-ResourceGroupName</span></span>
<span data-ttu-id="f6ff9-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="f6ff9-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="f6ff9-132">-Sku</span></span>
<span data-ttu-id="f6ff9-133">Ценовая категория для приложений центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="f6ff9-134">Значение по умолчанию — S1.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-134">Default value is S1.</span></span>

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

### <span data-ttu-id="f6ff9-135">-Поддомен</span><span class="sxs-lookup"><span data-stu-id="f6ff9-135">-Subdomain</span></span>
<span data-ttu-id="f6ff9-136">Поддомен для URL-адреса центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="f6ff9-137">Каждое приложение должно иметь уникальный поддомен.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-137">Each application must have a unique subdomain.</span></span>

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

### <span data-ttu-id="f6ff9-138">-Тег</span><span class="sxs-lookup"><span data-stu-id="f6ff9-138">-Tag</span></span>
<span data-ttu-id="f6ff9-139">Теги ресурсов центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-139">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="f6ff9-140">-Template</span><span class="sxs-lookup"><span data-stu-id="f6ff9-140">-Template</span></span>
<span data-ttu-id="f6ff9-141">Имя шаблона приложения для центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-141">IoT Central application template name.</span></span>
<span data-ttu-id="f6ff9-142">По умолчанию — это настраиваемое приложение.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-142">Default is a custom application.</span></span>

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

### <span data-ttu-id="f6ff9-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6ff9-143">-Confirm</span></span>
<span data-ttu-id="f6ff9-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6ff9-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6ff9-145">-WhatIf</span></span>
<span data-ttu-id="f6ff9-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6ff9-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6ff9-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6ff9-148">CommonParameters</span></span>
<span data-ttu-id="f6ff9-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6ff9-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6ff9-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6ff9-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6ff9-151">INPUTS</span></span>

### <span data-ttu-id="f6ff9-152">System. String</span><span class="sxs-lookup"><span data-stu-id="f6ff9-152">System.String</span></span>

### <span data-ttu-id="f6ff9-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f6ff9-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f6ff9-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6ff9-154">OUTPUTS</span></span>

### <span data-ttu-id="f6ff9-155">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="f6ff9-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="f6ff9-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6ff9-156">NOTES</span></span>

## <span data-ttu-id="f6ff9-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6ff9-157">RELATED LINKS</span></span>
